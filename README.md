# 通达信智能体广场（tdx-agent-market）

> 介绍页：<https://agent.fch-nas.cc>

一站式 AI 金融体验平台，内置智能选股、个股诊断、资金风向、技术分析等专业 Agent，覆盖完整投研工作流。

团队由 **股票智能分析系统**（主理人）编排调度五位投资大师，从不同流派视角共同研判个股与组合，最终由主理人按**确定性规则**将各方观点合成为**唯一权威结论**（`strategy_synthesis`）。

## 来源与致谢

- 专家团形态基于 **WorkBuddy 专家团**（团队型智能体）构建。
- 各 Agent 的角色提示词来自通达信智能体广场：<https://agent.tdx.com.cn>。

## 团队成员

| 成员 ID | 名字 | 流派 | 职责 |
|---------|------|------|------|
| tdx-agent-market-team-lead | 股票智能分析系统 | 多策略综合 | 编排调度、严格合成、输出权威结论 |
| warren-buffett | 巴菲特 | 慢慢变富 | 生活化讲透护城河、复利与安全边际，建立长期投资观 |
| peter-lynch | 彼得·林奇 | 成长掘金 | 六类公司分类、PEG、成长性与故事挖掘 |
| benjamin-graham | 格雷厄姆 | 安全边际 | 内在价值、安全边际、财务稳健性分析 |
| william-oneil | 欧奈尔 | 趋势突破 | CANSLIM、技术形态、相对强度与买卖点 |
| john-neff | 约翰·内夫 | 低估值掘金 | 低P/E、股息率、总回报率与逆向挖掘 |

## 快速开始

默认入口 Agent 为 `tdx-agent-market-team-lead`（见 `settings.json`），加载后可直接发起投研提问，例如：

- 请帮我的持仓做一次多策略综合研判，听听五位投资大师怎么看。
- 我想买贵州茅台，请让巴菲特、格雷厄姆、欧奈尔分别从价值、安全边际、技术形态三个角度给出建议。
- 如何用彼得·林奇的 PEG 和约翰·内夫的低市盈率法筛选成长股？

## 项目结构

```
.
├── .codebuddy-plugin/
│   └── plugin.json          # 插件清单：成员、团队信息、快捷提问
├── agents/                  # 各 Agent 的角色定义（Markdown persona）
│   ├── tdx-agent-market-team-lead.md
│   ├── warren-buffett.md
│   ├── peter-lynch.md
│   ├── benjamin-graham.md
│   ├── william-oneil.md
│   └── john-neff.md
├── avatars/                 # 团队与成员头像
├── settings.json            # 默认 Agent 配置
└── README.md
```

## 免责声明

本项目输出的所有研判内容仅供学习与研究参考，不构成任何投资建议。股市有风险，投资需谨慎。
