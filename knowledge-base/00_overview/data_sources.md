# 数据来源

| 数据域 | 来源文件 | 说明 |
|---|---|---|
| 角色 | `00_input/characters.xlsx` | 角色与作品名、触发词、外貌提示词 |
| Danbooru 标签 | `00_input/danbooru_tags_min1000.xlsx` | 收录量≥1000 的标签及类别 |
| NAI 手册 | `00_input/nai_tag_manual.xlsx` | 多工作表主题化提示词手册 |

- 输入文件为只读冻结源，构建前后均校验 SHA-256 未变。
- 数据集 v1.0.0｜schema v1.0.0，数据库内容签名 `6477e0baa7c416a2…`。

## Danbooru 类别分布
| 类别 | 标签数 |
|---|---|
| General | 7605 |
| Character | 2290 |
| Copyright | 926 |
| Meta | 167 |

> 类别取值按来源原样呈现，不做合并或改写。
