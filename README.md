# 魏宇 · AI 产品、数据分析与大数据工程作品集

西交利物浦大学 · 数据科学与大数据技术本科（**专业前 10%** · 全英文授课 · 2028 届） · 意向城市：上海（可线下全勤到岗）

[四页作品集 PDF](portfolio/yu-wei-portfolio.pdf) · [Word 版](portfolio/yu-wei-portfolio.docx) · [纯文本版](portfolio/yu-wei-portfolio.source.txt) · [QuantLab 免登录正式站](https://edmund45501.softr.app/about?try=1&lang=zh) · [**全线产品需求文档（PRD 总目录）**](prds/README.md)

| 案例 | 项目归属与角色 | 核心判断与验证结果 | 规格与文档 |
| --- | --- | --- | --- |
| [01 · QuantLab](cases/quantlab.md) | 7 人课程团队（2026.09 至今）· 负责回测与 AI 教练流程、口径核对与评测集 | 双记录复盘中全期与 2025 留出期回撤排序相反（全期 A 48.87% > B 48.49%；留出期 A 17.86% < B 20.10%），重算确认模型未算错并提出双期间并列展示写入 V2 规格；构建 60 题标准答案评测集与自动判分脚本；基于团队汇总的 10 位组外试用反馈落地 4 项流程迭代。 | [QuantLab 全线 PRD](prds/quantlab-prd.md) |
| [02 · ClassNote AI](cases/classnote-ai.md) | 个人项目（2026.05 至今）· macOS 双语课堂工作台（含 Windows 打包配置） | 针对课堂“录音继续但缺模型致字幕全空”故障，确立核心音频保存优先原则，将音频落盘、转写、翻译拆为独立状态提示并上线课前模型预检与先录后转；交付 macOS 安装版（DMG）实测验收，经续录恢复流程找回约 76.8 分钟有效录音（461 分片、0 重复字幕）。 | [ClassNote AI 全线 PRD](prds/classnote-ai-prd.md) |
| [03 · AppliedAI & ServeTrace](cases/appliedai-platform.md) | 个人 AI 产品原型（2026.11）· 知识库权限问答与大模型转发网关 | 对比提示词保密与生成后过滤后选定检索层前置 ACL，在 5 篇分密级演示文档上通过 9 组双身份对照加公开题基线（未授权 0/9、授权 9/9、公开 2/2）；联动 ServeTrace 落地单 Key 限流、`request_id` 耗时拆分与默认脱敏日志规则。 | [AppliedAI & ServeTrace 全线 PRD](prds/appliedai-servetrace-prd.md) |
| [04 · 数据分析与 SQL](cases/data-analysis.md) | 课程与扩展分析项目（个人完成）· 外呼 ROI 测算与 PostgreSQL 建模核验 | 剔除事后泄漏字段 `duration`，扫描外呼成本收益敏感性矩阵定位 0.20 阈值净值反亏边界（-2,800 vs 0.50 下 +11,300）并输出 Top-K 预算名单；设计 4 表关系模式入库 38,006 行数据并隔离 99 条异常关联。 | —（数据分析实践） |
| [05 · 大数据与分布式工程](cases/bigdata-hdfs-spark.md) | 4 人课程小组（CSI205 · 2026.10–11）· 负责 Master 部署、跨机排障与报告主笔 | 在 4 台异构主机搭建 HDFS 3.5.0 + Spark 3.5.9 Standalone（3 Executors 共 6 GiB）关联聚合 462 万条 Parquet 评论（6 轮逐字节一致）；解决 UFW 拦截 TCP 9866 / 7337 超时，对比单机 4 虚机（11.22s）与四物理机无线桥接（36.42s）定位双 `COUNT(DISTINCT)` 行膨胀跨高 RTT 链路的 Shuffle 瓶颈。 | —（分布式工程实践） |

更新日期：2026 年 11 月 23 日
