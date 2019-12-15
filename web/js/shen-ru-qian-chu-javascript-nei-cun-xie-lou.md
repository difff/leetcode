# 深入浅出JavaScript内存泄露

## 背景

我们的在线可视化编辑器，用户频繁反馈出现崩溃。

## 定位

### Vue组件内存泄露

我们封装了一个Vue组件叫xx-monaco-editor（基于微软的moncao编辑器）。 在beforeDestroy钩子事件中，我们释放了monaco。`this.editor && this.editor.dispose();`。 但检查内存泄露时，发现monaco对象中的\_editor实例未被释放。

```text
  data: function () {
    return {
      editor: null,
      // others
    }
  }
```

改成：

```text
  data: function () {
    this.editor = null;
    return {
      // others
    }
  }
```

monaco基本被释放了（仍有一小部分未被释放）。

初步判断：beforeDestroy的时机不对，因为父组件先调用子组件的dispose\(\)，而父组件还在监听了子组件editor的数据，因此子组件无法完全释放。那把子组件的dispose\(\)放在destoryed中调用呢？ 测试发现，还是这样。这就得从Vue的源码说起了。

[source](https://github.com/haibazhang/lib/blob/master/src/web/js/深入浅出JavaScript内存泄露.md) \| [edit-online](https://github.com/haibazhang/lib/edit/master/src/web/js/深入浅出JavaScript内存泄露.md)

