---
title: 嵌入
---

[嵌入]: ./link-embed.md
[站内引用]: ./link-local.md
[Kodama 程序]: /trees/references/app.md
[配置文件]: /trees/references/config.md

[Markdown]: https://commonmark.org
[Typst]: https://typst.app/docs
[VSCode]: https://code.visualstudio.com/

[嵌入] 是一种特殊的 [Markdown] 链接动作, 用于把目标文档展开到当前位置. 语法是在普通链接的 URL 后追加 `#:embed`, 例如 `[+](./doc.md#:embed)`. [Kodama 程序] 会在编译阶段解析目标文档并内联其内容.

- 相较于 [站内引用], [嵌入] 直接渲染目标文档的内容块.

- 嵌入时可以覆盖显示标题. 如 `[+ 自定义标题](./doc.md#:embed)` 会使用 `自定义标题` 作为嵌入块标题, 生成的目录也遵循此处设置. 

- 嵌入选项由链接文本开头的 `+`, `-`, `.` 控制, 可组合使用:
  - `+`: 开启编号.
  - `-`: 折叠嵌入块.
  - `.`: 不出现在目录中. 
  
  默认无编号、不折叠、出现在目录.

使用 [Markdown] 或 [Typst] 作为源文档时, 以下路径形式都可用于触发嵌入:

- `/trees/path/to/doc.md#:embed`
- `/trees/path/to/doc.typst#:embed`
- `./relative/path/doc.md#:embed`
- `./relative/path/doc.typst#:embed`
- `../parent/path/doc.md#:embed`
- `../parent/path/doc.typst#:embed`

与 [站内引用] 一样, 推荐在路径中保留 `.md` 或 `.typst` 扩展名, 这样通常更利于 [VSCode] 的跳转与补全体验. 
