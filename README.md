# TAG

用于创作 AI 绘画提示词的 skill。根据角色、动作、构图、环境和风格要求，生成适合不同图像模型的提示词。

## 来源与致谢

本 skill 的创作方法蒸馏自所长 **戒红所**（`red_relief_reformatory`）的 TAG 法典，在此标注原始方法来源。

![来源作者：戒红所](assets/source-author.png)

本仓库将法典中的创作经验整理为可执行的 skill 工作流程和平台输出规则。

本 skill 的初版蒸馏完成于 Opus 4.6 时期，并使用 Opus 4.6 执行。受当时模型能力和整理方式限制，其蒸馏效果可能不如当前使用 Fable 或其他模型重新蒸馏的结果。

## 支持格式

### Stable Diffusion（SD）

使用英文自然语言动作描述配合 Danbooru TAG，并采用 A1111 权重语法，例如 `(tag:1.3)`、`[tag]` 和 `BREAK`。

### NovelAI（NAI）

使用英文自然语言动作描述配合 Danbooru TAG，并转换为 NovelAI 权重语法，例如 `{tag}`、`1.2::tag::` 和 `[tag]`。

### Anima

使用 **SD TAG + 自然语言描述**。自然语言负责动作、姿势、人物互动和空间关系，SD TAG 负责外貌、服装、场景与画面效果。

### Krea 2

使用 **全中文自然语言**，完整描述主体、动作、姿势、构图、环境、光线和画面风格，不使用 Danbooru TAG 或权重语法。

> 目前尚未对 Anima 和 Krea 2 进行专门研究。以上内容只记录现阶段约定的输出格式，不代表针对模型特性完成了系统验证或优化。

## 文件结构

```text
tag/
├─ assets/                  # 来源图片
├─ LICENSE                  # MIT License
├─ SKILL.md                 # Skill 规则与工作流程
├─ README.md                # 项目与格式说明
└─ references/              # 通用创作方法与语法参考
```

## License

本仓库采用 [MIT License](LICENSE)。来源法典及来源作者原有内容的权利归原作者所有。
