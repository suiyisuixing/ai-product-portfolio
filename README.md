# 魏宇 · AI 产品、数据分析与大数据工程作品集

西交利物浦大学 · 数据科学与大数据技术本科（**专业前 10%** · 全英文授课 · 2028 届） · 意向城市：上海（每周 5 天线下全勤 · 可连续实习 3–6 个月）

[四页作品集 PDF](portfolio/yu-wei-portfolio.pdf) · [Word 版](portfolio/yu-wei-portfolio.docx) · [纯文本版](portfolio/yu-wei-portfolio.source.txt) · [QuantLab 免登录演示站](https://edmund45501.softr.app/about?try=1&lang=zh) · [**全线产品需求文档（PRD 总目录）**](prds/README.md)

| 案例 | 项目归属与角色 | 核心判断与验证结果 | 规格与文档 |
| --- | --- | --- | --- |
| [01 · QuantLab](cases/quantlab.md) | 7 人团队项目（2026.09 至今）· 产品架构与核心研发负责人（主导引擎、AI 教练、评测与前端改版） | 双记录复盘中全期与 2025 留出期回撤排序相反（全期 A 48.87% > B 48.49%；留出期 A 17.86% < B 20.10%），复算确认引擎无误并输出双期间并列展示 V2 规格；构建 6 类 60 题评测集与 JS 三态判分器（`score.mjs`），在 `deepseek-chat` 上重放 12 道冻结首答（8/12 通过、4/12 失败，捕获 3 例合法 JSON 内科技 ETF 槽位错填与 1 例留出期回撤方向写反）；基于团队汇总的 10 位组外试用反馈上线 4 项交互改动。 | [QuantLab 全线 PRD](prds/quantlab-prd.md) |
| [02 · ClassNote AI](cases/classnote-ai.md) | 个人项目（2026.05 – 2026.11）· macOS 双语课堂工作台（含 Windows 打包配置） | 针对课堂“录音继续但缺模型致字幕全空”异常，确立核心音频保存优先原则，将音频落盘、转写、翻译拆为独立状态提示并上线课前模型预检与先录后转；交付 macOS 安装版（DMG）实测验收，另在一次中断故障中经分片续录恢复找回约 76.8 分钟有效音频（461 分片、0 重复字幕）。 | [ClassNote AI 全线 PRD](prds/classnote-ai-prd.md) |
| [03 · AppliedAI & ServeTrace](cases/appliedai-platform.md) | 个人 AI 平台与 Agent 原型（2026.11）· 知识库权限问答与 OpenAI 兼容网关 | 选定检索层前置 ACL，在 5 篇分密级演示文档双检索路径（`FTS5` + `Chroma`）通过 9 组同题双身份对照（未授权由关闭时 9/9 降至 0/9、授权 9/9、公开对照 2/2）；接入真实 `deepseek-chat`（`temperature=0`，模拟工具沙箱）验证单步工具路由 `10/10` 与两步传值依赖任务 `2/2`；独立实现 ServeTrace 网关（`HTTP 429` + `Retry-After`、`request_id` 耗时拆分、默认不落盘完整提示词）。 | [AppliedAI & ServeTrace 全线 PRD](prds/appliedai-servetrace-prd.md) |
| [04 · 数据分析与 SQL](cases/data-analysis.md) | 个人独立分析与治理项目 · 外呼假设净值比较与 PostgreSQL 建模核验 | 剔除事后泄漏字段 `duration`，在 8,907 条留出集（`ROC-AUC 0.770` / `PR-AUC 0.424`）比较 9 组假设成本与价值净值（8 组以 0.20 较高；成本 100/价值 200 时 0.20 为 -2,800、0.50 为 +11,300）并输出固定产能 Top-K 名单（Top 100/200 命中率 81.0%/74.0%，`6.6x/6.0x Lift`）；设计 4 表 3NF 模式入库 38,006 行干净数据并隔离 99 条异常记录。 | —（数据分析实践） |
| [05 · 大数据与分布式工程](cases/bigdata-hdfs-spark.md) | 4 人小组项目（2026.10–11）· 负责 Master 部署、跨机排障、运行验证与报告主笔 | 在 4 台异构宿主机搭建 HDFS 3.5.0 + Spark 3.5.9 Standalone（3 Executors 共 6 GiB），基于团队清洗关联后的 8 个 Parquet 分片（462.46 万条有效评论、覆盖 137,249 件有评商品）执行聚合，两种部署共 6 份 54 类计数 CSV 与基准 SQL 逐字节一致；记录总耗时中位数（11.22s vs 36.42s）与 Stage 2 三轮均值（2.19s vs 17.91s）。 | —（分布式工程实践） |

更新日期：2026 年 11 月 27 日
