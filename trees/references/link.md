
---
title: 链接
asref: true
index: [](./index.md)
---

[Kodama 程序][app] 中的 [链接][link] 语法与 [Markdown][markdown-in-mdn] 链接语法一致, 但前者会依据链接前缀区分一个链接是外部或者内部的, 因为内部链接在 [Kodama 程序][app] 当中确实是一种特殊的存在, 它自动地将链接到的 [节][section] 和被链接的 [节][section] 关联起来. 除非特别强调, 否则我们所说的 [链接][link] 都是指内部链接. 

这种关联指的是, 如果 [节][section] $A$ 链接了 [节][section] $B$, 那么我们不止可以从 $A$ 所在的页面跳转到 $B$, 也应当有一种方式可以让我们从 $B$ 回到 $A$, 这个流程在如今通常被称为双向连接. 对于使用 [Kodama 程序][app] 的用户来说, 这种双向连接应当是自动生成. 

[app]: /references/app.md
[link]: /references/link.md
[section]: /references/section.md

[markdown-in-mdn]: https://developer.mozilla.org/en-US/docs/MDN/Writing_guidelines/Howto/Markdown_in_MDN
