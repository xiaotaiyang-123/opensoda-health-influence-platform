开源项目健康诊断与影响力分析平台

项目概述
基于OpenDigger开源数据集，构建一个可量化的开源项目健康度评估与开发者影响力分析平台。项目融合数据可视化、图算法与自然语言交互，为开源社区治理提供数据支持。

 核心功能
项目健康度多维度诊断- 融合活跃度、社区互动、代码质量等指标
2.开发者/项目影响力排名 - 基于协作网络的量化影响力评估
3.自然语言数据查询 - 通过SQLBot实现免SQL数据探索
4.智能知识问答 - MaxKB集成解答指标定义与算法原理

  技术栈
- 后端框*: Django + Django REST Framework
- 数据源: OpenDigger数据集 (`o300_metrics.json`)
- 图计算: EasyGraph (PageRank变体算法)
- 可视化: DataEase BI工具
- AI交互: SQLBot (自然语言转SQL) + MaxKB (知识问答)
- 任务调度: APScheduler
- 数据库: PostgreSQL (生产) / SQLite (开发)

 项目架构
 用户 → DataEase可视化 ← Django API ← 数据处理层 ← OpenDigger数据
↓ ↓ ↓
SQLBot查询 MaxKB知识库 EasyGraph图计算
