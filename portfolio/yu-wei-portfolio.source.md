# 魏宇 · AI 产品作品集

西交利物浦大学 · 数据科学与大数据技术本科 · 2028 届 · 更新 2026-11-09（Asia/Shanghai）

关注 AI 应用体验、需求设计与效果评测。本人主导个人项目的产品构思、方案选择、原型制作和问题修复，使用 AI 编程工具辅助实现与调试。

公开材料：https://github.com/suiyisuixing/ai-product-portfolio  
本 PDF 由 `portfolio/yu-wei-portfolio.source.html` 结构化排版导出（5 页）。不沿用历史 mock 的 4.9s 冒充本轮成绩。

## 三个 AI 产品案例

| 项目 | 解决的问题 | 主要证据 |
|---|---|---|
| ClassNote AI | 课堂录音正常却没有字幕时，如何保留记录并给出下一步 | 模型预检、先录后转、状态分离；真实界面 |
| AppliedAI Platform | 内部知识库中限制进入生成上下文的资料，并给出有来源的真实回答 | 中文语义检索、权限对照、本机 Qwen 带引用问答 |
| ServeTrace | 模型调用统一鉴权、限流、重试与请求定位 | 管理台凭证与配额、真实模型测试台、与 AppliedAI 联通 |

## ClassNote AI

学生遇到“没有字幕”时，先确认课堂内容是否仍在保存。将音频、转写、翻译状态拆开，提供改选可用模型与先录后转分支。界面见图：`assets/classnote-model-manager.jpg`。

## AppliedAI Platform

首要目标：未授权片段不能进入生成上下文。嵌入：`BAAI/bge-small-zh-v1.5`（512）。本机模型 `qwen3.5-27b-q5_k_m` @ 8081。2026-11-09 Phase1 验收含「芦潮港灯塔-7719」「桂花糯米-42」；本轮 verify 约 9.8s 量级。截图：`appliedai-login.png`（登录页）、`appliedai-cited-answer.png`、`appliedai-library.png`、`appliedai-acl-guest.png`、`appliedai-gateway-cited-answer.png`。

限制：非生产；Redis 真实限流本环境外部阻塞。

## ServeTrace

管理台 8700；上游 http→8081；限流实际 memory。截图：`servetrace-keys-masked.png`（无完整 Key）、`servetrace-playground.png`（掩码占位）、`servetrace-logs.png`（请求记录页）、`servetrace-overview.png`。

## 数据分析与 SQL 项目（原版保留）

### 银行营销分析
UCI Bank Marketing 45,211 条；阈值 0.50→TP201/FP88；0.20→TP469/FP497；新增组正例占比≈39.6%。无实际投放结果。

### Film Database System
PostgreSQL 影片/人物/角色/评分模型；12 条分析查询。https://github.com/suiyisuixing/film-database-system

### QuantLab 历史数据功能
ENT207 团队：6 只 ETF、1,416 共同观测；收益/回撤/费用比较。模拟收益非实际业绩。
