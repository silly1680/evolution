---
name: Auto Evolution Agent
slug: auto-evolution-agent
version: 1.0.0
description: MSOP 能力自进化引擎——自动扫描 GitHub Trending 与 ClawHub，发现并吞噬新能力，通过评分、沙盒验证、Skill 生成全自动化完成 AI Agent 的能力进化闭环
homepage: https://github.com/silly1680/auto-evolution-agent
changelog: "Initial release: full MSOP pipeline with scan, evaluate, approve, sandbox-test, skill-generate, deploy, observe, retire-check lifecycle"
metadata:
  emoji: "🧬"
  requires:
    bins:
      - node
      - git
    os:
      - linux
      - darwin
      - win32
---

# Auto Evolution Agent 🧬

MSOP（Multi-agent Self-Organizing Protocol）能力自进化引擎——让 AI Agent 自动获取新能力。

## 核心能力

本技能实现了完整的 **15 步 MSOP 进化闭环**：

```
SCAN → GAP_ANALYSIS → TARGET_SELECTION → EVALUATION
→ APPROVAL(Anti-Poison) → FETCH → SANDBOX_TEST
→ CAPABILITY_EXTRACTION → DNA_ENCODING → COMPOSITION
→ SKILL_GENERATION → DEPLOY → OBSERVE → VALUE_UPDATE → RETIRE_CHECK
```

### 三大进化模式

| 模式 | 扫描间隔 | 自动通过阈值 | 风险容忍 | 适用场景 |
|------|---------|-------------|---------|---------|
| `safe` | 48h | ≥8分 | 极低 | 生产环境 |
| `balanced` | 24h | ≥7分 | 中等 | 日常积累 |
| `aggressive` | 12h | ≥6分 | 高 | 快速扩张 |

### 三大进化阶段

- **Phase 1 基础建设期**：构建 browser/coding/memory 核心基座
- **Phase 2 专项深化期**：深化 trading/vision/AI-ML 垂直领域
- **Phase 3 系统融合期**：多能力融合为端到端 workflow

## 使用方式

### 快速开始

```bash
node auto-evolution-agent.js status
```

### 运行完整进化周期

```bash
node auto-evolution-agent.js run-cycle
```

### 查看能力注册表

```bash
node auto-evolution-agent.js status
```

### 执行淘汰检查

```bash
node auto-evolution-agent.js retire-check
```

### 自我反思报告

```bash
node auto-evolution-agent.js reflect
```

### 注册新能力

```bash
node auto-evolution-agent.js deploy <id> <name> <dna> <score> <source>
```

## 评分公式（MSOP）

```
Score = Innovation × 0.35 + Integration × 0.25 + GapMatch × 0.2 + Popularity × 0.1 − Risk × 0.3
```

**价值评分**：`ValueScore = Usage × 0.4 + SuccessRate × 0.3 + Efficiency × 0.3`

## 淘汰规则

能力满足以下**全部三个条件**时被淘汰：
- `value_score < 3`
- `usage_count < 5`
- `success_rate < 60%`

## 配置说明

```javascript
// 可通过修改 auto-evolution-agent.js 中的 CONFIG 调整
const CONFIG = {
  scan_interval: 24 * 3600,        // 扫描间隔（秒）
  max_repo_per_cycle: 5,            // 每轮最多处理
  auto_approve_threshold: 7,        // 自动通过阈值
  sandbox_required: true,           // 沙盒验证
  retention_days: 30,               // 日志保留
  evolution_mode: 'balanced',       // safe | balanced | aggressive
};
```

## 安全机制

- **Anti-Poison 检测**：恶意代码模式识别、虚假功能检测
- **沙盒隔离测试**：静态分析 + 运行时检测
- **审批路由**：≥7分自动通过、5-7分人工审批、<5分直接丢弃

## 数据存储

```
evolve/
├── capability-registry.json    # 能力注册表
├── observation-log.json         # 调用观察日志
├── evolution-strategy.json      # 进化策略配置
├── msop-state.json              # 状态机状态
├── candidates/                  # 候选列表
├── skills/                      # 生成的 Skill
└── sandbox/                     # 沙盒测试区
```

## 评分记录

| 指标 | 值 |
|------|-----|
| MSOP评分 | 8.5 |
| DNA | evolution, autonomous, agentic, self-improving, skill-generation |
| 模式 | balanced |
| 来源 | MSOP 原生构建 |
