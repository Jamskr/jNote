## BOM (Brower Object Model)

浏览器自带的一些全局对象

```
window  // 当前窗口对象
screen  // 屏幕对象
history // 访问历史
location    // 地址栏
localStorage    // 本地存储
sessionStorage  // 会话级存储
```

## DOM (Document Object Model) 文档对象模型

当浏览器加载 `HTML` 后， `<body>` 下所有元素对象构成一个树状结构，每个节点都可以操纵。

结论：DOM 里所有元素都在 `document` 对象下可以找到，进而可以操纵该元素。

## NOTE

- `onclick` 里可以指定一大段代码
- 大多数元素都支持鼠标事件
- 单引号和双引号混用的问题（建议外层使用双引号，内层使用单引号，单个的时候使用单引号，减少敲键盘的次数。。。）
- `onclick` 里可用的上下文参数：`this`, `event`
- 运行时检查错误，不运行就不检查错误