---
title: 配置文件
asref: true
---

配置文件 `Kodama.toml` 可通过 `kodama new config` 创建, 或在 `kodama new site` / `kodama init` 时自动生成.
下面是版本 [](/trees/latest.md) 的完整配置结构.

```toml
[kodama]
trees = "trees"
assets = "assets"
base-url = "/"
themes = []

[toc]
placement = "right"
sticky = true
mobile-sticky = true
max-width = "45ex"

[text]
edit = "[edit]"
toc = "Table of Contents"
references = "References"
backlinks = "Backlinks"

[build]
typst-root = "trees"
short-slug = false
pretty-urls = false
footer-mode = "link"
inline-css = true
asref = false
output = "./publish"
# edit = "https://example.com/repo/edit/main/trees/"

[serve]
edit = "vscode://file/"
output = "./.cache/publish"
command = ["miniserve", "<output>", "--index", "index.html", "--pretty-urls"]
```

- `[kodama]`
  - `trees`: 文档源目录 (存放 `index.md` 和其他节文件).
  - `assets`: 静态资源目录, 每次构建会同步到输出目录下对应子目录.
  - `base-url`: 部署根 URL, 仅 `build` 模式生效; `serve` 模式固定使用 `/`.
  - `themes`: 主题文件路径数组 (相对工作区根目录).

- `[toc]`
  - `placement`: 目录位置, `left` 或 `right`.
  - `sticky`: 桌面端目录是否粘性定位.
  - `mobile-sticky`: 移动端目录是否粘性定位.
  - `max-width`: 目录区域最大宽度.

- `[text]`
  - `edit`: 页面编辑按钮文本.
  - `toc`: 目录标题文本.
  - `references`: 引用区标题文本.
  - `backlinks`: 反链区标题文本.

- `[build]`
  - `typst-root`: Typst project root (默认 `trees`).
  - `short-slug`: 页面内部展示的 slug 是否只保留末段.
  - `pretty-urls`: 是否启用无 `.html` 后缀链接.
  - `footer-mode`: 页脚模式, `link` 或 `embed`.
  - `inline-css`: 是否内联 CSS.
  - `asref`: 全局默认是否按参考页 (`asref`) 渲染.
  - `output`: `build` 输出目录.
  - `edit`: 可选, 部署环境下编辑链接前缀.

- `[serve]`
  - `edit`: 本地编辑器 URL 前缀.
  - `output`: `serve` 输出目录.
  - `command`: 本地服务启动命令, `<output>` 会在运行时替换为输出目录.
