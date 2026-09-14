# 字段字典

## characters
| 字段 | 含义 |
|---|---|
| char_name_zh / char_name_en | 角色中/英文名 |
| work_name_zh / work_name_en | 作品中/英文名 |
| trigger_words | 角色触发词 |
| appearance_prompt | 核心外貌提示词（可能缺失，缺失不代填） |
| source_file / source_sheet / source_row | 来源定位 |

## danbooru_tags
| 字段 | 含义 |
|---|---|
| tag_canonical | 精确/唯一字段，保留下划线，用于提示词与精确检索 |
| tag_display | 展示字段，词汇标签下划线转空格，颜文字保留原样 |
| category | 标签类别（General/Character/Copyright/Meta） |
| popularity | Danbooru 收录量（非 NovelAI 权重） |

## nai_manual_entries
| 字段 | 含义 |
|---|---|
| sheet_name / group_name | 工作表 / 分组 |
| tag_raw | 条目标题（通常为 Tag 列） |
| fields_json | 该行全部列的键值对 |
