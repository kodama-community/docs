
---
title: 编译参数
asref: true
---

```plain
  -b, --base <BASE>                Base URL or publish URL (e.g. https://www.example.com/) [default: /]
  -o, --output <OUTPUT>            Path to output directory [default: ./publish]
      --assets <ASSETS>            Path to assets directory relative to the output directory [default: ./assets]
  -r, --root <ROOT>                Configures the project root (for absolute paths) [default: ./]
  -d, --disable-pretty-urls        Disable pretty urls (`/page` to `/page.html`)
  -s, --short-slug                 Hide parents part in slug (e.g. `tutorials/install` to `install`)
  -f, --footer-mode <FOOTER_MODE>  Specify the inline mode for the footer sections [default: link] [possible values: link, embed]
      --disable-export-css         Disable exporting the `*.css` file to the output directory
      --edit <EDIT>                Display URL redirect links prepared for the editor (e.g. `vscode://file:`)
  -h, --help                       Print help
```

- 一旦使用了 `--edit`, 则每次编译前都会在终端打印像是下面的内容, 用于通知用户此时生成的页面中包含用户设备的路径信息. 以一种醒目的方式强调此事完全必要, 因为像这样的路径中很有可能包含设备上的用户名或者其他不应该透露的信息. 

  ```plain
  [vscode://file:] EDIT MODE IS ENABLE. Please note that your disk file path information will be included in the pages!
  ```
