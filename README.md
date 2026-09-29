# economist-vocab-log

> 经济学人阅读与生词本 · 《经济学人》原文归档 + 生词本沉淀：文章按期存放，生词按「单词｜词性｜中文意思｜查询日期」记录，每次更新一个 commit。

> 一个纯内容仓库：**经济学人原文归档 + 生词本沉淀**。不放程序、不放脚本，只放读过的文章和记下的词。

---

## 这个仓库是做什么的

读外刊这件事，难点从来不是"拿到文章"，而是"读过的东西留不下来"：文章散落在桌面、下载目录、聊天记录里，几周后想找某一期就找不回；生词当时查了、当时懂了，但没有落到一个地方，下次遇到还是不认识。

所以这个仓库只承担两件事：

1. **原文归档** —— 每期读过的《经济学人》文章按时间存进来，形成一条"我读过什么"的时间线。
2. **生词沉淀** —— 阅读时查到的词记进生词本，形成一份"我积累过什么"的词表。

配合 git 版本历史，每一次更新都是一个 commit，随时能回溯"哪天读了哪几篇、新增了哪些词"，也方便在不同设备之间同步。

## 目录结构

```
economist-vocab-log/
├── README.md              本说明
├── 经济学人原文/           文章归档：按 年/月 存放
│   └── 2026/09/           命名建议：YYYY-MM-DD_标题.docx
└── 生词本/
    └── 单词本.docx        生词表（单词 | 词性 | 中文意思 | 查询日期）
```

## 文章索引（在线阅读）

在线阅读入口：**<https://xuan250.github.io/economist-vocab-log/>**（本文件就是它的首页）。下表链接直接在浏览器内嵌打开，不会触发下载，也不走 GitHub 文件页那套容易报错的 pdf.js。

| 日期 | 标题 | 在线阅读（Pages） | 备用（jsDelivr） |
|------|------|------------------|------------------|
| 2026-09-20 | How a Skateboarder Sees Los Angeles | [打开](https://xuan250.github.io/economist-vocab-log/%E7%BB%8F%E6%B5%8E%E5%AD%A6%E4%BA%BA%E5%8E%9F%E6%96%87/2026/09/2026-09-20_How%20a%20Skateboarder%20Sees%20LosAngele.pdf) | [打开](https://cdn.jsdelivr.net/gh/xuan250/economist-vocab-log@main/%E7%BB%8F%E6%B5%8E%E5%AD%A6%E4%BA%BA%E5%8E%9F%E6%96%87/2026/09/2026-09-20_How%20a%20Skateboarder%20Sees%20LosAngele.pdf) |
| 2026-09-26 | When America walks away | [打开](https://xuan250.github.io/economist-vocab-log/%E7%BB%8F%E6%B5%8E%E5%AD%A6%E4%BA%BA%E5%8E%9F%E6%96%87/2026/09/2026-09-26_When%20America%20walks%20away%20For%20decades%20America%20has%20enjoyed%20hegemony%20over%20the%20Middle.pdf) | [打开](https://cdn.jsdelivr.net/gh/xuan250/economist-vocab-log@main/%E7%BB%8F%E6%B5%8E%E5%AD%A6%E4%BA%BA%E5%8E%9F%E6%96%87/2026/09/2026-09-26_When%20America%20walks%20away%20For%20decades%20America%20has%20enjoyed%20hegemony%20over%20the%20Middle.pdf) |

约定：

- 新增文章后在上表加一行（日期 + 标题 + 两个链接），否则 Pages 首页点不到它——Pages 不提供目录浏览，只渲染 README。
- `github.io` 打不开时用备用列；jsDelivr 域名还可换 `fastly.jsdelivr.net` / `gcore.jsdelivr.net` / `testingcf.jsdelivr.net`。
- 刚推上去的文件在 jsDelivr 上可能有缓存延迟，需要时访问 `purge.jsdelivr.net` 加同样路径刷新。

## 更新方式

**文章**：读完一期，把文章文件放进 `经济学人原文/年/月/`，命名 `YYYY-MM-DD_标题.docx`。

**生词**：打开 `生词本/单词本.docx`，在表格末尾追加一行，填四列：

| 单词 | 词性 | 中文意思 | 查询日期 |
|------|------|----------|----------|
| lucrative | adj. | 获利丰厚的（a lucrative business） | 2026-09-29 |

约定：

- **同一单词重复查到不重复记录**，避免词表里堆满重复项。
- 中文意思尽量带一个原文里的短语或例句，只抄释义过两周就想不起语境。
- 文档一律用 `.docx`，不产出 `.doc` / `.pdf` 等其他格式。
- 不提交账号、密码等任何敏感信息。

**提交**：

```bash
git add -A
git commit -m "update: 2026-09-29 期 + 5 个生词"
```

## 说明

- 生词本沿用"生词卡片"的经典思路：词性 + 释义 + 例句 + 日期，四个字段就是间隔复习时需要的全部线索。日期字段的作用是标记"这个词是哪天遇到的"，便于日后判断该不该重学。
- 抓取文章的桌面工具在另一个仓库，本仓库**不依赖任何程序**：纯手工放文件、纯手工记词也能正常运转。

## 更新记录

- 2026-09-29 初始化仓库，同步生词本；移除所有脚本，仓库精简为「README + 经济学人原文 + 生词本」三部分。
- 2026-09-29 仓库定名 `economist-vocab-log`，推送到 GitHub（xuan250/economist-vocab-log）。
- 2026-09-29 新增「文章索引」：开启 GitHub Pages 后，通过 README 里的绝对链接在浏览器内嵌阅读 PDF（Pages 无目录浏览，必须靠索引）。
