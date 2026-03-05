# Agentic RL Analysis

基于论文原文的Agentic Reinforcement Learning研究分析。

---

## 📄 核心文档

### [STATE_OF_THE_ART.md](STATE_OF_THE_ART.md) - 研究现状（基于论文）

**状态**: 基于8篇论文（2025-2026）的Abstract原文  
**核心内容**:
- **4个核心挑战**: 训练稳定性、信用分配、可扩展性、探索效率
- **5个技术趋势**: 异步训练、策略空间探索、零数据训练等
- **8篇已分析论文**: VCPO, ELPO, CM2, Agent World Model, ASTER, Tool-R0, Dr. MAS, SGE

**关键洞察**:
- 异步训练成为标配，但方差控制是核心难题
- 从动作空间探索转向策略空间探索
- 过程奖励重要性提升
- 多智能体系统开始发展

---

## 📚 论文阅读进度

### 已阅读并总结（8篇）

| 论文 | arXiv | 核心挑战 | 关键方法 |
|------|-------|----------|----------|
| **VCPO** | 2602.17616 | 训练稳定性 | 方差控制的异步RL |
| **ELPO** | 2602.09598 | 信用分配 | 错误定位的策略优化 |
| **CM2** | 2602.12268 | 信用分配 | Checklist Rewards |
| **Agent World Model** | 2602.10090 | 可扩展性 | 合成环境生成 |
| **ASTER** | 2602.01204 | 可扩展性 | Interaction-dense冷启动 |
| **Tool-R0** | 2602.21320 | 可扩展性 | 自博弈零数据训练 |
| **Dr. MAS** | 2602.08847 | 训练稳定性 | 多智能体稳定训练 |
| **SGE** | 2603.02045 | 探索效率 | 策略引导探索 |

### 待阅读
- OTB: Optimal Token Baseline
- DART: Disentangled Action Reasoning
- ASTRA: Automated Synthesis of Trajectories
- 早期工作: Tongyi, GLM-5, ABE, GEM

---

## 📁 仓库结构

```
agentic-rl-analysis/
├── STATE_OF_THE_ART.md          # 核心文档：基于论文的研究现状
├── papers/
│   ├── PAPERS_TO_READ.md        # 待阅读论文清单
│   └── paper-summaries-batch1.md # 已阅读论文详细总结
├── INSIGHTS_FROM_PAPERS.md      # 从论文提取的洞察
├── deep-dive/                   # 早期工作深度分析（待更新）
│   └── ...
├── README.md                    # 本文件
└── LICENSE                      # MIT许可证
```

---

## 🎯 核心发现

### 4个核心技术挑战（来自论文）

1. **训练稳定性与方差控制**
   - 异步训练中的重尾重要性权重
   - 多智能体系统中的梯度范数不稳定
   - 代表: VCPO, Dr. MAS

2. **长程任务的信用分配**
   - 首个不可恢复步骤的定位
   - 从稀疏结果到过程评估
   - 代表: ELPO, CM2

3. **环境与数据的可扩展性**
   - 合成环境构建
   - 零数据/自博弈训练
   - 交互质量控制（Interaction Collapse）
   - 代表: Agent World Model, Tool-R0, ASTER

4. **探索效率**
   - 语言动作空间中的有效探索
   - 策略空间vs动作空间
   - 代表: SGE, Tool-R0

---

## 📊 关键数据（来自论文实验）

### 训练效率
- VCPO: 2.5倍速度提升，65% token节省
- Dr. MAS: 消除梯度尖峰

### 任务性能
- ASTER: AIME 2025 90.0%
- CM2: tau-Bench +8, BFCL-V4 +10, ToolSandbox +12
- Tool-R0: 92.5相对改进

### 规模
- Agent World Model: 1,000环境，35工具/环境

---

## 🔑 关键术语

- **TIR**: Tool-Integrated Reasoning
- **Interaction Collapse**: 交互崩溃
- **ESS**: Effective Sample Size
- **Checklist Rewards**: 清单奖励
- **Strategy-Guided Exploration**: 策略引导探索

---

## 📖 阅读建议

1. 先阅读 [STATE_OF_THE_ART.md](STATE_OF_THE_ART.md) 了解全貌
2. 查看 [papers/paper-summaries-batch1.md](papers/paper-summaries-batch1.md) 了解每篇论文细节
3. 参考 [INSIGHTS_FROM_PAPERS.md](INSIGHTS_FROM_PAPERS.md) 看归纳分析

---

## ⚠️ 重要说明

- 所有内容基于论文**Abstract原文**，非主观臆测
- 如需更深入理解，请阅读论文**全文**
- 本仓库持续更新，随着阅读更多论文会调整洞察

---

**Last Updated**: 2026-03-02  
**License**: MIT
