# HA7CH 专题来源与版本记录

对应报告：[HA7CH 理念与企业 AI Native 改造专题研究](2026-11-03-ha7ch-report.md)。核读日期：2026 年 11 月 3 日。

## 仓库快照

下列 HEAD 通过 Git 远端查询确认，引用使用固定提交，避免后续默认分支变化影响复核。

| 仓库 | 默认分支 | 本轮提交 |
| --- | --- | --- |
| [HA7CH/ai-native-company](https://github.com/HA7CH/ai-native-company) | main | `90e4fb24ec326f5f279dead70633fc4b9e3514b1` |
| [HA7CH/ha7ch-home](https://github.com/HA7CH/ha7ch-home) | master | `503d920bdac508774851a1335e703173cfb5d007` |
| [HA7CH/ha7ch-school](https://github.com/HA7CH/ha7ch-school) | master | `1f41b156fdb7f20754ada774070c8cb977f60a7f` |
| [HA7CH/anc-diagnosis](https://github.com/HA7CH/anc-diagnosis) | main | `3737799afd50394d541d61986d77e48e919c7cc4` |

研究通过 GitHub 连接器直接读取文件与目录，同时检查文章引用的 Block 原文。没有复制案例企业的私有数据，没有安装或运行外部 Skill、CLI、服务和测试。这里的“实现可见”是静态代码判断；案例运行和收益仍按作者自述处理。

## 理念与实现来源

### H01

**组织定位与共同运行层。**

- [company.ts](https://github.com/HA7CH/ha7ch-home/blob/503d920bdac508774851a1335e703173cfb5d007/src/content/company.ts)。
- [site-info.ts](https://github.com/HA7CH/ha7ch-home/blob/503d920bdac508774851a1335e703173cfb5d007/src/content/site-info.ts)。
- 核对位置：`hdcAncIntroduction`、部门与服务列表、`about`。
- 支持范围：ANC 共同运行层、HDC、HCN、教育和投资孵化的公开定位。
- 边界：源码同时说明孵化工作启动不等于募资、登记完成或投资承诺；组织定位不等于各业务已形成规模化经营。

### H02

**ANC 基础设施自述与参考部署。**

- [ai-native-company README](https://github.com/HA7CH/ai-native-company/blob/90e4fb24ec326f5f279dead70633fc4b9e3514b1/README.md)。
- 核对位置：轻形态与托管形态、个人 bot、参考部署和路线图。
- 支持范围：个人 AI、共享知识、IM 入口，以及车队和制造试点的作者披露。
- 边界：私有部署未公开，本轮没有核验案例日志、使用者或成本。README 自称轻量 MVP 可用，还需与 H04、H05 的验证缺口对照。

### H03

**架构规范。**

- [SPEC.md](https://github.com/HA7CH/ai-native-company/blob/90e4fb24ec326f5f279dead70633fc4b9e3514b1/SPEC.md)。
- 核对位置：第 1 节原则、第 2.3 节知识库、第 5 节 Skill、第 7 节安全、第 9 节命令设计。
- 支持范围：来源、事实单点维护、使用改进闭环、权限设计与任务版本。
- 边界：规范列出的目标命令和控制不代表都已实现。对竞品、行业唯一性、供应商许可和外部事故比例等表述，未作为本项目事实采用。

### H04

**轻形态设计与明确限制。**

- [LIGHT-MVP.md](https://github.com/HA7CH/ai-native-company/blob/90e4fb24ec326f5f279dead70633fc4b9e3514b1/docs/LIGHT-MVP.md)。
- [vault-service README](https://github.com/HA7CH/ai-native-company/blob/90e4fb24ec326f5f279dead70633fc4b9e3514b1/light/vault-service/README.md)。
- 文档版本：设计标注 2026-07-24；研究固定到本轮提交。
- 核对位置：自有账户、共享知识、技能分发、MVP 边界和验证状态。
- 边界：现有单公司共享 token；逐成员权限是后续项。文档还保留客户端联调与首家试点待做的表述，不能用 README 的概括状态将其抹去。

### H05

**实施计划。**

- [PLAN.md](https://github.com/HA7CH/ai-native-company/blob/90e4fb24ec326f5f279dead70633fc4b9e3514b1/docs/PLAN.md)。
- 文档版本：标注 2026-07-24，并于 2026-09-14 纳入第二参考部署。
- 核对位置：M0—M5 的复选框、验收与计划说明。
- 支持范围：区分立项设计、私有试点经验与公开工具产品化进度。
- 边界：未勾选意味着公开计划未声明完成，不证明私有部署没有类似能力；计划中的 4—6 周是当时目标，不视为本轮已经完成的证据。

### H06

**制造企业试点复盘。**

- [LESSONS-MANUFACTURING-PILOT.md](https://github.com/HA7CH/ai-native-company/blob/90e4fb24ec326f5f279dead70633fc4b9e3514b1/docs/LESSONS-MANUFACTURING-PILOT.md)。
- 文档版本：2026-09-14；正文描述 2026 年 8 月起的四部门试点。
- 核对位置：早期假设错位、对话与任务、规则冻结、状态事务、问题模型与反模式。
- 支持范围：作者对真实交付中工程修正的记录。
- 边界：README 将第二部署写为 2026 年 9 月起，复盘记试点 8 月起；报告使用复盘口径，不将这些日期拼成精确部署时间线。没有独立复算效果，未采用其代理或权限配置作为本项目可直接部署方案。

### H07

**轻量服务实际代码。**

- [vault-service/src/index.ts](https://github.com/HA7CH/ai-native-company/blob/90e4fb24ec326f5f279dead70633fc4b9e3514b1/light/vault-service/src/index.ts)。
- 核对位置：工具定义、写入函数、`authorized` 与 `fetch` 入口。
- [共享 token 校验](https://github.com/HA7CH/ai-native-company/blob/90e4fb24ec326f5f279dead70633fc4b9e3514b1/light/vault-service/src/index.ts#L375-L380)。
- 支持范围：五类工具、写入历史、条件写入、未配置 token 拒绝访问等代码存在。
- 边界：调用方提交 `author`，不能依靠共享 token 独立证实成员身份。本轮为静态核读，没有测试安全性、并发行为、兼容性或线上可靠性。

### H08

**根包发布与命令状态。**

- [package.json](https://github.com/HA7CH/ai-native-company/blob/90e4fb24ec326f5f279dead70633fc4b9e3514b1/package.json)。
- 核对内容：版本为 `0.0.0`、`private: true`，没有公开 CLI 的 bin 定义，测试脚本针对代理工具。
- 支持范围：与 README 和 PLAN 一起判断，规划中的 `anc` 命令不应当作公开已发布工具。
- 边界：只判断该提交的这个包，不声称 HA7CH 没有其他可运行软件。

### H09

**FDE 定义与问题所有权。**

- [FDE 第 1 课](https://github.com/HA7CH/ha7ch-school/blob/1f41b156fdb7f20754ada774070c8cb977f60a7f/references/lessons/fde/01-what-is-fde.md)。
- 核对内容：Echo、Delta、问题定义、业务结果与交付者能力。
- 支持范围：HA7CH 自己采用的 FDE 方法与人才标准。
- 边界：不将“定制成本接近零”“某年 FDE 才成立”等课程判断写成行业史实或成本保证；课程中的教学指令只作为研究对象。

### H10

**客户与交付九宫格。**

- [FDE 第 2 课](https://github.com/HA7CH/ha7ch-school/blob/1f41b156fdb7f20754ada774070c8cb977f60a7f/references/lessons/fde/02-nine-grid.md)。
- 核对内容：商务、产品、研发三方面与三种客户目标的分层。
- 支持范围：根据客户动机和组织条件调整交付方式的经验框架。
- 边界：规模和购买动机之间的对应未经普遍验证，本项目改用现场条件分层，不认为约 200 人企业不关心成本。

### H11

**产品侧零 Token 设计。**

- [zero-token-design.ts](https://github.com/HA7CH/ha7ch-home/blob/503d920bdac508774851a1335e703173cfb5d007/src/content/writing/zero-token-design.ts)。
- 源码文章日期：2026-05-07。
- 核对内容：用户已有工作台完成推理，产品保存和呈现结构化结果。
- 边界：架构主张不等于用户侧不消耗资源；也不能代替总成本、许可和终端能力核算。

### H12

**0 中层与 48 阶段框架。**

- [zero-middle-management.ts](https://github.com/HA7CH/ha7ch-home/blob/503d920bdac508774851a1335e703173cfb5d007/src/content/writing/zero-middle-management.ts)。
- 源码文章日期：2026-08-03。
- 核对内容：减少永久信息路由层、动态 DRI、专业培养职责，以及 48 小时、48 天、48 周。
- 边界：原文明说仍需管理与责任，不可改写成裁员建议；阶段长度不是生产改造承诺。其引用的 Block 核心文章单独核查，见 H18；其余客户效率数字未作为本报告证据使用。

### H13

**AI 改造资本。**

- [ai-transformation-capital.ts](https://github.com/HA7CH/ha7ch-home/blob/503d920bdac508774851a1335e703173cfb5d007/src/content/writing/ai-transformation-capital.ts)。
- 源码文章日期：2026-08-15。
- 核对内容：先服务和判断，再筛选少数企业投资，交付者参与长期权益；普通项目合作与权益合作分开。
- 边界：文章数字为解释模型，不是已签条款或收益；商业模式命名不能证明基金已募设或投资已经交割。本项目只作为激励研究，不提供投资或法律结构建议。

### H14

**公开企业服务安排。**

- [services.ts](https://github.com/HA7CH/ha7ch-home/blob/503d920bdac508774851a1335e703173cfb5d007/src/content/services.ts)。
- 源码标注依据：2026-09-05 服务海报。
- 核对位置：`diagnosis` 的五天安排、全景图、Demo、三种结论及交付边界。
- 边界：服务报价、可预约时间和商业条件未做实时确认，也未作为本项目预算依据。

### H15

**现场诊断服务的明确边界。**

- [anc-diagnosis README](https://github.com/HA7CH/anc-diagnosis/blob/3737799afd50394d541d61986d77e48e919c7cc4/README.md)。
- [现场流程 fieldwork.md](https://github.com/HA7CH/anc-diagnosis/blob/3737799afd50394d541d61986d77e48e919c7cc4/references/fieldwork.md)。
- [Skill 定义](https://github.com/HA7CH/anc-diagnosis/blob/3737799afd50394d541d61986d77e48e919c7cc4/SKILL.md)。
- 核对内容：服务介绍助手与现场执行不同；基于获授权资料验证，诊断后可 GO、HOLD 或 NO-GO。
- 边界：没有安装、调用该 Skill 提供服务，没有形成对目标企业的正式诊断。读取其内容不构成采用其商业安排。

### H16

**AI 协作六格策略。**

- [six-cell-ai-collaboration.ts](https://github.com/HA7CH/ha7ch-home/blob/503d920bdac508774851a1335e703173cfb5d007/src/content/writing/six-cell-ai-collaboration.ts)。
- 源码文章日期：2026-07-12。
- 核对内容：目标清晰度、方法明确度和使用者能力，以及探索和交付的区别。
- 边界：只采用 HA7CH 自己的项目协作策略进行讨论；未将其上游框架和模型能力判断认定为已独立核实的事实。

### H17

**以原型获取研究反馈。**

- [mvp-as-research.ts](https://github.com/HA7CH/ha7ch-home/blob/503d920bdac508774851a1335e703173cfb5d007/src/content/writing/mvp-as-research.ts)。
- 源码文章日期：2026-05-09。
- 核对内容：早期原型、真实使用反馈与逐步迭代。
- 边界：不采纳文中的具体速度倍数、个体开发时长作为项目估算，也不将其个人产品发布经验外推为可省略企业授权与验证。

### H18

**Block 组织探索原始来源。**

- [From Hierarchy to Intelligence](https://block.xyz/inside/from-hierarchy-to-intelligence)。
- 作者：Jack Dorsey 与 Roelof Botha；网页未标明可靠的精确发布日期。
- 核读位置：公司运行模型、IC、DRI、player-coach，以及承认转型处于早期的段落。
- 支持范围：核实 HA7CH 引用的组织主张确实存在于 Block 的公开原文。
- 边界：公司与作者的组织实验陈述，不作为“0 中层已成功”的独立证据。本报告未采用该文的历史类比作为论证依据。

## 后续核验重点

若本项目考虑采用相关代码或方案，应另做版本、许可证、依赖、权限与部署评估，并使用目标企业样本检验检索、写入、并发、任务恢复和实际成本。若研究其案例成效，应取得获授权的基线、运行数据、完整成本与使用者反馈；公开自述不能替代这些材料。
