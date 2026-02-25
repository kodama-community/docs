
---
title: 写作
---

[Markdown]: https://commonmark.org
[Typst]: https://typst.app/docs
[Tinymist]: https://github.com/Myriad-Dreamin/tinymist

在使用 [Typst] 文档写作时, 请务必导入 `_lib/kodama.typ` 并 `#show: kodama`. 这段代码将保证 [Typst] 文档转换为网页后, 其公式内容能够正确显示. 除此之外, 这段代码也会改善 [Tinymist] 等本地预览工具的使用体验. 

> [!IMPORTANT]
> 对于 `trees` 文件夹内的 [Typst] 文件, 需要遵循以下后缀规范: 
> - 如果其属于库文件. 即, 不直接产生具体文档, 请使用 `.typ` 作为文件后缀. 
> - 而对于包含内容的 [Typst] 文档, 请统一使用 `.typst` 后缀. 
> 
