
---
title: 安装
---

目前, 用户可以根据目标设备的架构直接从 [GitHub Release][release] 页面下载二进制文件. 
当 [GitHub Release][release] 页面缺少适合你设备的文件时, 你可以从 [源代码](https://github.com/kokic/kodama) 开始自己构建, 如

```sh
cargo install --git https://github.com/kokic/kodama.git
```

如果希望在 Termux 等 Android 环境中使用, 请下载 `aarch64-unknown-linux-musl`, 或 [克隆][clone] [源代码](https://github.com/kokic/kodama) 至本地后在其目录下执行

```sh
cargo build --release --target=aarch64-unknown-linux-musl
```

[release]: https://github.com/kokic/kodama/releases
[clone]: https://git-scm.com/docs/git-clone

我们建议用户使用最新版本, 即便该版本被标记为 `pre-release`. 在 `1.0` 版本释放前, 每次发布都可能包含破坏性变更, 不过我们会努力使迁移成本尽可能的低.  
