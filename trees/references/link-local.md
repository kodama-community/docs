
---
title: 站内引用
---

[站内引用]: ./link-local.md
[Kodama 程序]: /trees/references/app.md
[配置文件]: /trees/references/config.md

[Markdown]: https://commonmark.org
[typst]: https://typst.app/docs
[vscode]: https://code.visualstudio.com/
[title]: https://developer.mozilla.org/en-US/docs/Web/HTML/Reference/Global_attributes/title

[站内引用] 或称内部链接, 是一种特殊的 [Markdown] 链接, 也是构造双链文档的基本手段. [Kodama 程序] 会在编译阶段解析 [站内引用] 所指向文档的标题和 `slug` [^slug] 信息. 

- 当 [站内引用] 的文字部分为空时, 即 `[](./doc.md)` 这种情况, [Kodama 程序] 会使用所指向文档的标题作为此链接的文字部分. 

- 当 [站内引用] 的文字部分不为空时, 链接的显示文本即为此文字部分. 而所指向文档的标题会作为链接元素的 [title] 属性, 在指针悬停时可见. 
  
  - 当所指向文档的标题包含特殊内容 (如 KaTeX 代码) 时, 这些特殊内容往往不适合在悬停处展示. 此时所指向文档设置的 `page-title` 会作为实际的悬停展示标题. 

- 考虑一个文档 $A$, 此文档包含一个 [站内引用] 指向文档 $B$, 记为 $A \to B$. 对于通常的网页来说, 查看文档 $A$ 时访问文档 $B$ 是轻而易举的; 但查看文档 $B$ 时就难以知道文档 $A$ 的存在. 为此 [Kodama 程序] 会为每个文档页面都生成反向链接并放置于页面底部, 这就提供了路径 $B \to A$. 

- 当文档 $A$ 内包含大量 [站内引用] 指向文档 $B_1, B_2, B_3, \cdots$ 时, 将这些链接信息从文档中的不同位置整理到一个集中区域, 是完全有必要的. 为此, 用户可以在所需文档的元数据部分添加 `asref: true`, 这将使得此文档被认为是一条参考, 并收集在页面底部的 `References` 位置. 

  - 如果文档的元数据 `taxon` 内容以 `reference` 或者 `参考` 开头, 则此文档也会被认为是一条参考. 
  
  - 用户也可以直接在 [配置文件] 的 `[build]` 处将 `asref = false` 改为 `asref = true`. 这将使得所有的文档都被认为是参考. 

使用 [Markdown] 作为文档格式写作时, 以下链接会被识别为 [站内引用]: 

- `/trees/path/to/doc.md`
- `/trees/path/to/doc.typst`
- `./relative/path/doc.md`
- `./relative/path/doc.typst`
- `../parent/path/doc.md`
- `../parent/path/doc.typst`

诸如此类的链接可以最大程度地配合 [VSCode] 编辑器的跳转功能, 以便获得最佳的编辑体验. 路径 `/path/to/doc.md` 目前虽然也是合法的, 但编辑器往往无法确定目标文件位置, 我们不建议使用. 

[^slug]: 简单的说, `slug` 可以认为就是文档的唯一标识符. 
