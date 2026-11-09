# 魏宇 · AI 产品作品集

西交利物浦大学 · 数据科学与大数据技术本科 · 2028 届

关注 AI 应用体验、需求设计与效果评测。我主导个人项目的产品构思、方案选择、原型制作和问题修复，使用 AI 编程工具辅助实现与调试。

这份作品集展示三个项目的使用问题、关键判断与验证结果。各案例可直接阅读，无需访问私有源码。

[下载四页作品集 PDF](portfolio/yu-wei-portfolio.pdf)

## 项目

| 项目 | 解决的问题 | 主要设计与证据 |
| --- | --- | --- |
| [ClassNote AI](cases/classnote-ai.md) | 课堂录音正常却没有字幕时，如何保留记录并给出下一步操作 | 模型预检、先录后转、状态分离；真实界面与历史恢复记录 |
| [AppliedAI Platform](cases/appliedai-platform.md) | 内部知识库中，怎样限制进入生成上下文的资料 | FTS5 / Chroma 两种检索后端、权限对照、工具调用异常处理 |
| [ServeTrace](cases/servetrace.md) | 模型调用怎样统一鉴权、限流、重试与请求定位 | Memory / Redis 限流、Retry-After、请求级追踪及本地协议测试 |

## 重点案例：ClassNote AI

学生遇到“没有字幕”时，首先需要确认课堂内容是否仍在保存。我将音频、转写和翻译的状态拆开，提供改选可用模型和先录后转的明确分支，并把模型实际可用性检查放到开课前。

[阅读完整案例与界面](cases/classnote-ai.md)

## 数据与 SQL 项目

[Film Database System](https://github.com/suiyisuixing/film-database-system) 是由课程延展的数据建模与查询项目，包含 PostgreSQL 关系模型、12 条分析查询及数据质量检查设计。可查看 [SQL 查询](https://github.com/suiyisuixing/film-database-system/blob/main/sql/07_analysis_queries.sql) 与 [项目验证状态](https://github.com/suiyisuixing/film-database-system/blob/main/PROJECT_STATUS.md)。

## 阅读这些结果时

案例中的量化结果来自保留的历史本地记录，分别说明样本量和模拟条件。它们对应具体原型行为，不代表企业部署、商业收益或真实模型的生产表现。公开材料只含脱敏案例、界面与汇总结果；私有源码和原始记录可在面试中展示。

最近整理：2026-11-09
