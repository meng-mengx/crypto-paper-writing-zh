---
name: crypto-models-and-proofs
description: 建立与审阅密码学安全模型，设计构造、分析攻击、展开安全证明或简化方案。纯语言润色不使用。
---

# 密码学模型、构造与证明

适用范围见 [crypto-paper-writing 主入口](../../SKILL.md)，按当前密码学问题使用本模块。

按当前缺口读取对应参考及必要依赖，不整份预读所有技术规则：

- 定义与候选算法：读[定义与构造](references/definitions-and-constructions.md)，核对同一对象在模型、算法与实验中的语义。
- 安全证明与概率界：读[证明与概率](references/proofs-and-probability.md)的相关小节；涉及理想功能或交互模拟时读[真实与理想模拟](references/proofs-and-probability.md#真实与理想模拟)，联合隐私或统计误差读[信息论与统计证明](references/proofs-and-probability.md#信息论与统计证明)，选模型和解释检查结果读[模型与工具边界](references/proofs-and-probability.md#模型与工具边界)。交付前沿[证明自审](../../references/revision-checks.md#证明自审)回查实际推导。
- 应用协议或系统：围绕当前要解决的困难，说明方案如何完成目标功能，并找出决定其正确性或安全性的关键关系。例如，若声称撤销成员不能获得新群密钥，追踪其掌握的旧状态与公开更新能否导出新密钥；若声称防重放，从接受条件解释旧消息为何不能在新会话通过。按当前方案展开相关关系，给出对应算法、条件和推导。涉及多阶段协议时，核对阶段间的密钥与状态衔接；不同模型或工具的结果按实际覆盖性质解释。
- 原语如何支撑协议性质：读[协议性质](references/protocol-properties.md)；涉及模型或模拟缺口时再补读前两项。
- 方案简化或压缩：读[方案简化](references/simplification.md)，沿受影响的算法、模型和证明复查。

形式工具可以辅助引理检索、目标检查与证明验证。检索结果须核对变量、前提与依赖版本；目标状态和诊断不等于证明通过。安全游戏、归约与模拟仍须实际推导。

交付本轮需要的具体定义、完整候选算法、实际推导、证明或合法反例；区分已经成立的结果、候选与准确缺口。一条证明路线失败不等于方案不安全。仅审阅时给出位置、依据、影响与具体改法，不擅自修改。

只有缺少相关工作或研究问题尚未收敛时，才按需组合[文献阅读与研究构思](../crypto-literature-and-ideas/SKILL.md)；需要起草或修订论文正文时，按需组合[论文写作与修订](../crypto-manuscript-writing/SKILL.md)。只有结论依赖实测或作者要求实验时，才组合[实验与复现子技能](../crypto-experiments/SKILL.md)，不以跑通程序代替证明。
