# CHANGELOG

所有显著变更都将记录在此文件中。

格式基于 [Keep a Changelog](https://keepachangelog.com/zh-CN/1.0.0/)。

---

## [Unreleased]

### 变更

- 方法论升级为四阶段「需求、意图、规格、实现」：手册 `intro/workflow.md` 重命名为 `intro/layer.md`；教程 `metaphysics/intro/` 七篇按新框架重写（哲学阐述与数学表达合并为意图、新增语言无关的规格、代码实现改称实现），`README`、`CONTRIBUTING`、`AGENTS` 同步改名；档案仓 `README`、`CONTRIBUTING` 与三篇档案重写；`meta-journal-to-profile` 技能同步改名
- 案例集结构迁移：`index.md`、`category/`、`ontology/` 整体移入 `metaphysics/`
- 案例集与论文按学术规范改写：案例集长文补摘要与章节编号、改正式语体；论文四篇统一摘要、编号章节与结论，中文引号统一「」
- 手册 `intro/layer.md` 内容按四阶段重写（不再保留旧四步表述）；札记《从哲学到代码》的编译链、五分支映射表与边界条目对齐新框架；洞察 `index.md` 的方法表述同步改称
- 领域长名正式定为 `meta-engineering`：语境、章程、规格、日志、图书馆、路线图、教程七个仓库的英文名由 `-of-philosophy` 改为 `-of-meta-engineering`
- README 补「定位：哲学的实现」——哲学是理论，元工程把哲学命题落成可运行的体系；删去与改写后的命名规则
- 实验室子模块改名：`examples/default` → `examples/quanttide-meta-lab`（仓 quanttide-laboratory-of-philosophy → quanttide-meta-lab）


### 新增

- 教程仓新增 `intro/layer.md`《四个阶段》；`intro/index.md` 按最新主题重写为四阶段摘要（丢弃学科清单与文章导航），`README` 目录同步
- 章程仓新增 `index.md`《量潮元工程章程》：四阶段的概念、工作流与验收标准，哲学五大分支与形而上学、本体论、范畴论的主要功能
- 规格仓新增 `intro/layer.md`：四阶段的定义；`intro/ontology.md` 移至 `ontology/index.md`
- 图书馆 `pr4xis.md` 补「替代方案」：按功能拆分的替代品（范畴论 Rust 原语、OWL/RDF 本体推理、知识图谱层）与替代边界——完整组合（范畴论形式化 + 本体组合 + Rust 编译期证明）无直接对等物
- `data/report` 新增 retrospective 报告：qtcloud-work CLI 分析线复盘——主线论点（被删的分析与它诊断的平台患同一种病：点可靠、边断裂）、方法有效域（命题 vs 困惑）与三条因果处方，含 2026-10-05 设计偏差反思；同日删除 `data/profile/qtcloud-work-cli/` 档案——分析未解除读者困惑，教训收入本报告
- 补齐 `data/`：新增归档（archive）、宣传册（brochure）、历史（history）、洞察（insight）、档案（profile）、报告（report）；`data/intention` 由普通目录改为独立子模块（quanttide-intention-of-meta-engineering）
- 补齐 `docs/`：新增札记（essay）、案例集（gallery）、手册（handbook）
- `apps/` 新增量潮云（`apps/qtcloud` → qtcloud）与量潮咨询云（`apps/qtconsult` → qtconsult）
- `packages/` 新增元工程工具箱（`packages/quanttide-meta-toolkit` → quanttide-meta-toolkit）
- 注册子模块：`docs/bylaw`（量潮元工程章程，quanttide-bylaw-of-philosophy）
