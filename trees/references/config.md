
---
title: 配置文件
asref: true
index: [](./index.md)
---

配置文件 `Kodama.toml` 目前可通过 `kodama new c` 单独创建, 或者在新建 [Kodama][app] 站点时自动生成. 配置文件通常包含以下内容:  

```toml
[kodama]
trees = "trees" 
assets = "assets"
base-url = "/"

[build]
typst-root = "./"
short-slug = false
pretty-urls = false
footer-mode = "link"
inline-css = false
output = "./publish"

[serve]
edit = "vscode://file/"
output = "./.cache/publish"
```

### `[kodama]`

- `trees` 用于指定文档目录, 即 `index.md` 等文件所在的文件夹.
- `assets` 用于指定资源目录, 如图片、字体等文件. `assets` 会在每次构建时自动同步到 `publish/<assets>`.
- `base-url` 用于指定部署到的域名根路径. 

### `[build]`

- `typst-root` 用于指定 Typst 构建时的根路径, 见 [project root](https://typst.app/docs/reference/syntax/#project-root).
- `short-slug` 开启后网页中每个 [节][section] 的 `slug` 只展示最后一部分.
- `pretty-urls` 开启后网页中每个内部链接将去除 `.html` 后缀.
- `footer-mode` 用于指定 [节][section] 的页脚部分是否嵌入关联或被关联 [节][section] 的正文. 值只能是 `link` 或 `embed`. 
- `inline-css` 开启后将内联 `main.css` 等 [CSS][css] 文件. 
- `output` 用于指定 `build` 模式下的网站输出路径.


### `[serve]`

- `edit` 用于指定 `serve` 模式下用于跳转到编辑器的 url 前缀. 
- `output` 用于指定 `serve` 模式下的网站输出路径.

[app]: /references/app.md
[section]: /references/section.md

[css]: https://developer.mozilla.org/en-US/docs/Web/CSS