# 知识库总览

本知识库由三份冻结输入表构建，经提取→清洗→数据库→文档四阶段生成。

- 数据集 v1.0.0｜schema v1.0.0
- 数据库内容签名：`6477e0baa7c416a2…`

## 三大数据域
1. **角色**（characters，共 8906）：中/英角色名、作品名、触发词、核心外貌提示词。
2. **Danbooru 标签**（danbooru_tags，共 10988）：canonical（精确/唯一）、display（展示）、类别、热度。
3. **NAI 手册**（nai_manual_entries，共 332）：按工作表与分组组织的主题化提示词知识。

## 使用约定
- 提示词引用与精确检索使用 `tag_canonical`（保留下划线）。
- 展示用 `tag_display`（词汇标签下划线转空格；颜文字/符号保留原样）。
- 一切数值/字段均可回溯到来源文件·工作表·行号，详见[来源可追溯性](../05_reference/source_traceability.md)。

## 相关
- [数据来源](data_sources.md)
- [局限与免责](limitations.md)
- [已知数据问题](known_data_issues.md)
