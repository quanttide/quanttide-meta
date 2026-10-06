# CHANGELOG

所有显著变更都将记录在此文件中。

格式基于 [Keep a Changelog](https://keepachangelog.com/zh-CN/1.0.0/)。

---

## [Unreleased]

### 变更

- 领域长名正式定为 `meta-engineering`：语境、章程、规格、日志、图书馆、路线图、教程七个仓库的英文名由 `-of-philosophy` 改为 `-of-meta-engineering`
- README 补「定位：哲学的实现」——哲学是理论，元工程把哲学命题落成可运行的体系；删去与改写后的命名规则
- 实验室子模块改名：`examples/default` → `examples/quanttide-meta-lab`（仓 quanttide-laboratory-of-philosophy → quanttide-meta-lab）


### 新增

- 图书馆 `pr4xis.md` 补「替代方案」：按功能拆分的替代品（范畴论 Rust 原语、OWL/RDF 本体推理、知识图谱层）与替代边界——完整组合（范畴论形式化 + 本体组合 + Rust 编译期证明）无直接对等物
- `data/report` 新增 retrospective 报告：qtcloud-work CLI 分析线复盘——主线论点（被删的分析与它诊断的平台患同一种病：点可靠、边断裂）、方法有效域（命题 vs 困惑）与三条因果处方，含 2026-10-05 设计偏差反思；同日删除 `data/profile/qtcloud-work-cli/` 档案——分析未解除读者困惑，教训收入本报告
- 补齐 `data/`：新增归档（archive）、宣传册（brochure）、历史（history）、洞察（insight）、档案（profile）、报告（report）；`data/intention` 由普通目录改为独立子模块（quanttide-intention-of-meta-engineering）
- 补齐 `docs/`：新增札记（essay）、案例集（gallery）、手册（handbook）
- `apps/` 新增量潮云（`apps/qtcloud` → qtcloud）与量潮咨询云（`apps/qtconsult` → qtconsult）
- `packages/` 新增元工程工具箱（`packages/quanttide-meta-toolkit` → quanttide-meta-toolkit）
- 注册子模块：`docs/bylaw`（量潮元工程章程，quanttide-bylaw-of-philosophy）
