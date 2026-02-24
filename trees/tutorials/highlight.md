
---
title: 代码高亮
---

[Kodama 程序][app] 本身并未提供代码高亮支持, 但用户想要为其配置一些主流的高亮工具也不是一件难事. 我们以 [highlight.js][hljs] 为例. 在工作区根目录新建 `import-style.html`, 内容如下: 

[.import-style.html](../examples/highlight.js.md#:embed)

随后重新编译即可. 我们还额外设置了一些样式, 用于调整浏览器明暗主题下的代码高亮行为. 

[app]: /references/app.md

[hljs]: https://highlightjs.org
