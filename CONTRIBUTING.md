# 贡献指南

本仓是容器仓：自身只有 `README.md` 与这份指南，全部内容都在 22 个子仓里，本仓只追踪指针。所以贡献的第一步不是写文件，而是判断内容该落哪个子仓。

## 一、五类子模块

| 轴 | 数量 | 回答什么 | 内容 |
|----|------|----------|------|
| `data/` | 11 | 元工程现在知道什么、定过什么 | 记忆与数据资产 |
| `docs/` | 6 | 外人该读到什么 | 对外交付的成稿文档 |
| `apps/` | 3 | 这套东西怎么跑起来 | 可运行应用 |
| `packages/` | 1 | 哪些能力可复用 | 被 `apps/` 引用的库 |
| `examples/` | 1 | 想法能不能成立 | 实验场，验完即弃 |

## 二、`data/` 十一个仓的关系

这是本仓最需要说清的一层。它们不是十一个平级目录，而是一条流水线加若干旁支。

**时间线（唯一事实源，只追加）**

- `journal/` 按 `<域>/<YYYY-MM-DD>.md` 记当天发生了什么。它是所有下游蒸馏的原料，本身不做提炼。

**四层认知（从原料蒸馏而来，各答一类问题）**

- `insight/` 认知命题：机制与规律，按哲学分支（`aesthetics`、`epistemology`、`ethics`、`logic`、`metaphysics`）归档
- `intention/` 意图对齐：人和 AI 之间「要做什么、为什么这么定」
- `roadmap/` 方向与决策：下一步做什么、按什么顺序
- `report/` 阶段复盘：一条工作线当时的判断、依据、适用范围。**它不承担规范职责**——要变成规矩进章程或规格，要变成做法进手册

**沉淀终点**

- `profile/` 稳定档案：一件事怎么被拆开，四阶段固定顺序（需求 → 意图 → 规格 → 实现），按域分档，含 `ontology/`、`category/`、`intro/` 三类子结构。凡是跨时间仍成立的结论，最终落到这里

**旁支**

- `context/` 语境：分层草稿箱，`essay`、`handbook`、`history`、`insight`、`intention`、`library`、`profile`、`report`、`roadmap`、`tutorial` 各层在此先成形
- `history/` 沿革：这条线是怎么走到今天的
- `library/` 文献与素材：外部材料的存放处
- `brochure/` 宣传册：对外口径
- `archive/` 归档：退役内容的终点，只进不出

**一句话概括这条链**：`journal` 记事实 → 蒸馏成 `insight` / `intention` / `roadmap` / `report` → 稳定下来进 `profile`；`context` 是成稿前的落点，`archive` 是退役后的落点。

## 三、`context/` 与 `docs/` 是草稿箱与正式仓

最容易混的一对：同一批层名（`essay`、`handbook`、`tutorial`、`history`……）两边都有。分工不是内容不同，而是阶段不同。

1. **草稿箱**：稿件写进 `data/context/` 的对应层，并**就地把原稿改成成稿**——文件名与位置不动，放进去的应该是能直接读的成稿，不是素材堆。
2. **审核**：由创始人（iGuo）逐篇过，逐篇说「通过」或指出要改哪里。
3. **移入正式仓**：**全部通过之后**，才移到 `docs/` 的对应仓（如论文入 `docs/essay/`，手册入 `docs/handbook/`），草稿箱侧删除、不留副本。

不抢跑：整理好 ≠ 通过。移完逐条校对正文里的相对链接。

`docs/` 六个仓各管一类交付物：`bylaw/` 章程与制度、`specification/` 规格、`handbook/` 做法、`essay/` 文章、`tutorial/` 教学、`gallery/` 案例集。

## 四、`apps/`、`packages/`、`examples/` 与内容仓的依赖方向

- `apps/qtcloud`（量潮云，当前发布包 `studio`）、`apps/qtcloud-meta`（量潮元云，当前发布包 `cli`）、`apps/qtconsult`（咨询云）读 `data/` 与 `docs/` 里的规格来跑——**代码依赖文档，文档不依赖代码**。
- `packages/quanttide-meta-toolkit` 被 `apps/` 引用，反过来不引用 `apps/`。
- `examples/quanttide-meta-lab` 可以依赖以上任何一层，但不被任何一层依赖。
- 内容仓（`data/`、`docs/`）的正文里不写代码仓的路径与文件引用；需要指向实现，就指向规格。

## 五、新内容往哪放（四条判据）

1. 今天发生的事 → `journal/`
2. 想通了、且跨时间稳定 → `profile/`；还只是命题 → `insight/`；引出选择 → `roadmap/`；阶段复盘 → `report/`
3. 成篇材料 → `data/context/` 的对应层；已通过审核的终稿 → `docs/` 的对应仓
4. 退役不再维护 → `archive/`

判据之外还有一道上游判断来自本仓 `README.md`：只讲命题本身归哲学，讲命题如何落成结构、规则与工具才归元工程。回溯不到命题的规范，要么命题缺失，要么这条规范尚无依据。

## 六、维护规则

1. **先子仓、后指针**：改动在子仓提交推送成功之后，才回本仓 `git add <子模块路径>` 更新指针；子仓推不上去时指针不落地——宁可不更新，不留悬空指针。上推顺序是子仓 → `quanttide-meta` → 根仓 `quanttide`，每级核对本地 HEAD 与远端一致。
2. **移动不留副本**：凡从一处移到另一处，来源侧删除。同一内容任何时刻只有一个真源，两处并存就是两个真源。
3. **各自的仓规自己写**：`data/journal/CONTRIBUTING.md` 管日志命名与补记；`data/profile/CONTRIBUTING.md` 管档案四阶段；`data/report/CONTRIBUTING.md` 管报告三段。本文件只指路，不复制正文。
4. **日志已迁出**：`data/context/` 自 2026-10-19 起不再收日志，元工程日志统一在 `data/journal/`。
5. **版本与发布**：各子仓自带 `CHANGELOG.md` + 语义化版本 + `vX.Y.Z` tag；多包应用按包打 scope（如 `cli/v0.1.0-alpha.1`、`studio/v0.1.0-alpha.1`）。**本仓本身不打 tag**，只追踪指针。
6. **构建**：内容仓以纯 Markdown 为主，目前只有 `docs/tutorial/` 配了 `myst.yml`。没有构建配置的仓不必补 `_toc.yml`——根仓 `CONTRIBUTING.md` 里那套 Jupyter Book 指令在本仓不适用。
7. **提交**：`docs:` / `feat:` / `chore:` 前缀加中文说明，只提交本次相关路径，动手前后各核一次 `git status` 与 `git diff`，提交即推。

## 七、网络

本机 https 走代理经常失败，git 一律用 SSH：`git@github.com:quanttide/<repo>.git`。子模块 HEAD 常处分离头指针状态，推送用 `git push origin HEAD:main`。
