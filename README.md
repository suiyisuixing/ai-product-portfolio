# 魏宇 · AI 产品作品集

西交利物浦大学 · 数据科学与大数据技术本科 · 2028 届

关注 AI 应用体验、需求设计与效果评测。我主导个人项目的产品构思、方案选择、原型制作和问题修复，使用 AI 编程工具辅助实现与调试。

这份作品集展示三个项目的使用问题、关键判断与验证结果。各案例可直接阅读，无需访问私有源码。源码仓库、公开案例和本机体验地址是三件不同的事：本机 `127.0.0.1:8800` / `127.0.0.1:8700` 只在主机启动后可用，**不是**公网演示。

[下载四页作品集 PDF](portfolio/yu-wei-portfolio.pdf)

> PDF 已根据 2026-11-09 已核验案例重建可编辑源（`portfolio/yu-wei-portfolio.source.md`）并重新导出；旧版备份在交付目录。案例正文与截图同步反映真实模型修复结果；不沿用历史 mock 的 4.9s 等旧成绩冒充本轮。

## 项目

| 项目 | 解决的问题 | 主要设计与证据 |
| --- | --- | --- |
| [ClassNote AI](cases/classnote-ai.md) | 课堂录音正常却没有字幕时，如何保留记录并给出下一步操作 | 模型预检、先录后转、状态分离；真实界面与历史恢复记录 |
| [AppliedAI Platform](cases/appliedai-platform.md) | 内部知识库中，怎样限制进入生成上下文的资料，并给出有来源的真实回答 | 中文语义检索、权限对照、本机 Qwen 带引用问答，以及经 ServeTrace 可对上的请求编号 |
| [ServeTrace](cases/servetrace.md) | 模型调用怎样统一鉴权、限流、重试与请求定位 | 管理台凭证与配额、真实模型测试台、Memory 限流（当前环境未开 Redis）及与 AppliedAI 的记录联通 |

## 重点案例：ClassNote AI

学生遇到“没有字幕”时，首先需要确认课堂内容是否仍在保存。我将音频、转写和翻译的状态拆开，提供改选可用模型和先录后转的明确分支，并把模型实际可用性检查放到开课前。

[阅读完整案例与界面](cases/classnote-ai.md)

## 数据与 SQL 项目

[Film Database System](https://github.com/suiyisuixing/film-database-system) 是由课程延展的数据建模与查询项目，包含 PostgreSQL 关系模型、12 条分析查询及数据质量检查设计。可查看 [SQL 查询](https://github.com/suiyisuixing/film-database-system/blob/main/sql/07_analysis_queries.sql) 与 [项目验证状态](https://github.com/suiyisuixing/film-database-system/blob/main/PROJECT_STATUS.md)。

## 阅读这些结果时

案例中同时保留了 2026-11-02 的历史本地记录（含 mock 条件）和 2026-11-09 的真实本机模型验收。两者分开书写，不会把历史 mock 成绩改写成真实模型成绩。量化结果对应具体原型行为，不代表企业部署、商业收益或生产表现。公开材料只含脱敏案例、界面与汇总结果；演示账号和完整调用 Key 不进入本仓库。

最近整理：2026-11-09