# 文献库使用规则

`03_Literature` 保存文献及阅读笔记，按资料类型存放，按主题组织浏览。

## 1. 核心规则

1. **文献只存一份**：论文、书籍、报告分别存入 `01–03`，每篇文献一个文件夹。
2. **文献信息跟文献走**：标题、作者、年份、来源、阅读状态等在文献目录的 `metadata.yaml` 中统一维护；`notes.md` 保存阅读笔记。
3. **主题关系在 Topic 中维护**：每个主题一个页面，用关联文献表格维护文献链接、关联原因、在本主题中的作用和推荐阅读顺序。同一文献可以关联多个主题，也可以暂不归类。
4. **各类型维护自己的索引**：`01–03` 各有一个 `index.md`，汇总本类型的文献和未归类文献，展示字段按资料类型设置。文献信息从 `metadata.yaml` 汇总，主题关联从 Topic 汇总，不重复手工维护。
5. **命名规则**：文献文件夹使用 `年份_简短标题_来源缩写`，例如 `2017_AttentionIsAllYouNeed_NeurIPS`。来源缩写可省略；标题避免空格和特殊字符，重名时补充关键词。文件夹名称同时作为文献 ID，建立引用后尽量保持稳定。
6. **PDF 文件命名**：论文使用 `paper.pdf`，书籍使用 `book.pdf`，报告使用 `report.pdf`，文件名无需重复文献标题。
7. **链接规则**：Markdown 内部链接使用相对路径，以当前文件所在目录为起点。例如，Topic 中引用文献笔记：
```markdown
[Attention Is All You Need](../01_Papers/2017_AttentionIsAllYouNeed_NeurIPS/notes.md)
```
移动或重命名文献目录时，同步更新相关引用。

**属于文献的信息跟文献走，属于文献与主题关系的信息放在 Topic 中。**

## 2. 目录结构

```text
03_Literature/
├── README.md
├── 01_Papers/                   # 论文、预印本
│   ├── index.md                 # 论文索引
│   └── 2017_AttentionIsAllYouNeed_NeurIPS/
│       ├── paper.pdf            # 论文原文
│       ├── metadata.yaml        # 文献自身信息
│       └── notes.md             # 阅读笔记
├── 02_Books/                    # 书籍
│   └── index.md                 # 书籍索引
├── 03_Reports/                  # 报告
│   └── index.md                 # 报告索引
└── 04_Topics/                   # 主题页面与关联文献表格
```

索引入口：[论文](01_Papers/index.md) · [书籍](02_Books/index.md) · [报告](03_Reports/index.md) · [主题目录](04_Topics/)

