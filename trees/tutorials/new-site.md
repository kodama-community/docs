---
title: 新建站点
---

用户在 [安装](./install.md) 后, 可以执行 `kodama -V` 或 `kodama --version` 检查是否安装成功.

要创建一个新的 Kodama 站点, 请执行:

```sh
kodama new site <PATH>
```

用户可以在该目录的 `trees/` 下进行 [Markdown][cmark] 或 [Typst][typst] [写作]. 

首次使用 `serve` 前, 建议检查 [配置文件][config] 中 `[serve]` 的 `command`. 默认命令依赖 [miniserve][miniserve], 你可以安装它, 或改为当前设备可用的本地服务命令. 例如:

```toml
command = ["python", "-m", "http.server", "-d", "<output>"]
```

如果用户需要生成 [VSCode 风格的 snippets 文件][vscode-snippets], 进而借助其 [][section] 代码补全功能 [^editor], 可在 Kodama 站点文件夹内执行

```sh
kodama snip --section
```

除此之外, `kodama snip` 也可以用于生成 $\KaTeX$ 宏补全文件和 `inline-section` 可用代码片段. 

```sh
$ kodama snip --help

Generate VSCode style snippets file

Usage: kodama snip [OPTIONS]

Options:
  -c, --config <CONFIG>  Path to the configuration file (e.g., "Kodama.toml") [default: ./Kodama.toml]
      --katex            Generate `.vscode/katex.code-snippets`
      --section          Generate `.vscode/section.code-snippets`
      --inline-section   Generate `.vscode/inline-section.code-snippets`
  -h, --help             Print help
```

[^editor]: [Snippets 补全功能][vscode-snippets] 在非 [VSCode][vscode] 的编辑器上是否可用需要自行探索. 

[config]: /trees/references/config.md
[section]: /trees/references/section.md
[写作]: /trees/tutorials/writing.md

[cmark]: https://commonmark.org
[typst]: https://typst.app/docs
[miniserve]: https://github.com/svenstaro/miniserve
[vscode]: https://code.visualstudio.com/
[vscode-snippets]: https://code.visualstudio.com/docs/editing/userdefinedsnippets
