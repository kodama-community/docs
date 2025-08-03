
---
title: 开始
---

用户在 [安装](./install.md) 后可以通过执行 `kodama -V` 或 `kodama --version` 以检查是否 [安装](./install.md) 成功. 

要创建一个新的 kodama 网站, 请执行

```sh
kodama new site <PATH>
```

用户可以在此目录的 `trees/` 文件夹下进行 [Markdown][cmark] 或 [Typst][typst] 写作. 

首次使用 `serve` 功能前, 用户应该检查 [配置文件](../references/config.md) 中 `[serve]` 字典的 `command` 键, 默认值调用了 [miniserve][miniserve] 程序, 因此用户可以选择安装 [miniserve][miniserve] 或者将其修改为其他可用的本地服务器. 如安装了 [python][python] 的用户可以将其替换为

```toml
command = ["python", "-m", "http.server", "-d", "<output>"]
```

[cmark]: https://commonmark.org
[typst]: https://typst.app/docs
[miniserve]: https://github.com/svenstaro/miniserve
[python]: https://www.python.org
