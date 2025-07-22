
---
title: 节
asref: true
index: [](./index.md)
---

[节][section] 是 [Kodama 写作][app] 中的基本概念. 每个 [节][section] 都将被处理为一个 [HTML][html] 文件. 其 [定义](https://github.com/kokic/kodama/blob/main/src/compiler/section.rs) 如下

```rs
pub struct Section {
    pub metadata: EntryMetaData,
    pub children: SectionContents,
    pub option: SectionOption,
    pub references: HashSet<Slug>,
}
```

[app]: /references/app.md
[section]: /references/section.md

[html]: https://developer.mozilla.org/en-US/docs/Web/HTML
