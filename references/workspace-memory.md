# 工作区记忆规范

## 原则

长期信息来自工作区文件，不来自模型的永久记忆。每次任务只读取相关文件；不要把未确认的推断写进稳定配置。

## 初始化

当工作区没有 `.xiaohongshu-ops/` 时，从 `assets/workspace-template/` 创建以下结构：

```text
.xiaohongshu-ops/
|-- account-profile.md
|-- brand-style.md
|-- content-pillars.md
|-- operating-rules.md
|-- benchmark-index.md
|-- idea-backlog.md
|-- published-content.csv
|-- benchmarks/
`-- outputs/
    |-- analyses/
    |-- plans/
    |-- drafts/
    `-- reviews/
```

只复制账号配置与记录模板，不修改 Skill 安装目录中的原始模板。`benchmark-account-template.md` 是新建单个对标账号档案时使用的母版，不把它登记成真实账号。

## 文件职责

- `account-profile.md`：账号目标、受众、人设、核心承诺、差异化、产品与限制。
- `brand-style.md`：标题、正文、封面、图片、色彩、排版和禁用项。
- `content-pillars.md`：栏目定义、比例、内容目的和边界。
- `operating-rules.md`：发布节奏、确认节点、数据与原创规则。
- `benchmark-index.md`：多个对标账号的索引、材料状态及档案链接。
- `benchmarks/`：每个账号单独一个 Markdown 档案。
- `idea-backlog.md`：候选选题、状态、所属栏目、来源机制和相似选题。
- `published-content.csv`：实际发布记录与真实表现数据。
- `outputs/`：带日期的重要报告、计划、成稿和复盘。

## 读写规则

1. 任务开始先读 `account-profile.md` 和与任务直接相关的文件。
2. 普通产出可直接保存到 `outputs/`；聊天中同时提供摘要与文件路径。
3. 定位、人设、栏目或品牌风格变更属于稳定配置变更，先展示新旧差异并获得确认。
4. 用户明确修正某项信息时，以最新确认内容为准，并在文件的“更新时间/变更记录”中登记。
5. 推断和待验证假设进入报告或实验清单，不进入已确认事实字段。
6. 删除或替换历史记录前先确认；优先追加状态或归档，保持可追溯性。
7. 生成新选题前搜索 `idea-backlog.md` 与 `published-content.csv`，标记相似项并更换角度。

## 多对标账号命名

账号档案使用 `benchmarks/平台账号名或短标识.md`。重名时追加稳定短标识。索引至少记录：账号、链接、领域、材料类型、样本数、采集日期、数据是否由用户提供、档案路径。

## CSV 约定

`published-content.csv` 保存 UTF-8，保留表头。未知值留空，不使用 `0` 代替未知。新指标需要新增列时，先保持旧列含义不变。
