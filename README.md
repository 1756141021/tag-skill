# TAG

[简体中文](README.md) | [English](README.en.md) | [한국어](README.ko.md) | [Русский](README.ru.md)

用于创作 AI 绘画提示词的 skill。根据角色、动作、构图、环境和风格要求，生成适合不同图像模型的提示词。

喜欢可以点点星星

## 安装

本 skill 不需要安装额外依赖，只需将仓库克隆到对应的 skills 目录。

### Claude Code

Windows CMD：

```cmd
git clone https://github.com/1756141021/tag-skill "%USERPROFILE%\.claude\skills\tag"
```

macOS / Linux：

```bash
git clone https://github.com/1756141021/tag-skill ~/.claude/skills/tag
```

安装后可以让 Claude 根据请求自动调用，也可以输入 `/tag` 手动调用。如果 `.claude/skills` 是在当前 Claude Code 会话启动后首次创建的，请重启 Claude Code。

### Pi

Windows CMD：

```cmd
git clone https://github.com/1756141021/tag-skill "%USERPROFILE%\.pi\agent\skills\tag"
```

macOS / Linux：

```bash
git clone https://github.com/1756141021/tag-skill ~/.pi/agent/skills/tag
```

安装后可以让 Pi 根据请求自动加载，也可以输入 `/skill:tag` 手动调用。

## 可选个性化资料

使用者可以在 `references/` 中按需建立以下文件。它们用于保存个人创作偏好，不是 skill 运行的必需项。

- **OC 外貌库**（`oc-library.md`）：按角色名保存发色、瞳色、发型、体型、种族特征等可见外貌。指定角色后，skill 会提取这些特征并按画面视线路径融入提示词，不会整段照搬模板。
- **创作上下文**（`context-anchor.md`）：保存希望长期沿用的创作口径、语言习惯和词汇约定。
- **已用诗句记录**（`used-poems.md`）：记录使用日期、诗句出处和画面简述，用于减少短期内重复使用同一句诗。

没有 OC 库或库中不存在指定角色时，直接在请求中提供角色外貌即可。

## 来源与致谢

本 skill 的创作方法蒸馏自所长 **戒红所**（`red_relief_reformatory`）的 TAG 法典并加入了作者的些许promot理解与小巧思，在此标注原始方法来源。

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

## 创作结果

以下四组结果均先从参考图片反推角色外貌，再由 skill 在保留角色辨识特征的基础上自由设计动作、构图、场景和色彩方案。

### 1. 紫水晶与墨色双翼

<img src="examples/01-violet-crystal.png" alt="黑发王冠少女捧着紫水晶，墨色双翼在身后展开" width="480">

<details>
<summary>查看提示词</summary>

```text
A crowned black-haired girl crushes a violet crystal between her palms, and its light erupts into two enormous ink-black wings as her hair lashes outward,
1.5::shattering violet crystal, black liquid wings bursting from her back, overwhelming magical pressure, figure filling the frame::, {{ink black, paper white, electric violet and smoke gray theme}}, 1girl, solo, pale skin, very long black hair, straight bangs, glowing purple eyes, silver crystal crown, cold focused expression, ornate white ceremonial dress, high ruffled collar, puff sleeves, fitted black waist, silver jewelry, hands together, violet flame, crystal fragments, sweeping hair, black ink splashes, floating dark petals, stark white background, strong symmetrical composition, monochrome with selective purple, rough ink texture, high-contrast anime illustration, -2::text, logo, watermark::
```

</details>

### 2. 冰上转身

<img src="examples/02-ice-skater.png" alt="金发兽耳少女在室内冰面高速转身" width="480">

<details>
<summary>查看提示词</summary>

```text
A blonde animal-eared girl carves a sharp turn across an indoor ice rink, extending one arm as her long braid, teal ribbons, and a fan of ice spray sweep behind her,
1.45::one-foot skating turn, body leaning into the curve, clean extended pose, explosive ice spray::, {{cream white, deep teal, ice blue and pale gold theme}}, 1girl, solo, blonde hair, very long hair, thick side braid, long sidelocks, animal ears, cream inner ear fur, aqua eyes, white pupils, blue stitch marks across nose bridge, small pout, teal maid headband, teal neck bow, gemstone brooch, teal and white skating dress, fitted bodice, frilled collar, layered skirt, white tights, teal ice skates, indoor ice rink, curved skate marks, glossy ice reflections, floating ice particles, overhead spotlights, blurred railing, dynamic anime illustration
```

</details>

### 3. 红幕登场

<img src="examples/03-crimson-curtain-maid.png" alt="猫耳恶魔女仆拉开红色舞台帷幕" width="480">

<details>
<summary>查看提示词</summary>

```text
A cat-eared demon maid throws open two heavy crimson curtains and steps onto the stage, her long twintails, ribbons, and layered skirt flaring outward in the sudden light,
1.45::both hands pulling the curtains apart, dramatic entrance, strong forward step, clean flowing silhouette::, {{charcoal black, porcelain white, crimson red and icy blue theme}}, 1girl, solo, petite, dark purple hair, very long twintails, curled hair ends, red inner hair, blunt bangs, gray eyes, blush, black cat ears, pink inner ears, blue flower hair ornament, black and red hair ribbons, white maid headband, black choker, black and white maid dress, corset bodice, puff sleeves, long black gloves, layered frilled skirt, white thighhighs, garter straps, black shoes, small white bat wings, black spade-tipped tail, red tail bow, crimson theater curtains, wooden stage, warm footlights, dark simple background, dynamic anime illustration
```

</details>

### 4. 敦煌飞袖

<img src="examples/04-dunhuang-hanfu.png" alt="酒红发女性身着敦煌风汉服，透明衣袖与红色飘带掠过镜头" width="480">

<details>
<summary>查看提示词</summary>

```text
A burgundy-haired woman twists toward the viewer, lifting a translucent sleeve across her mouth as her braid and red ribbons sweep past the lens,
1.5::close-up, figure filling the frame, strong body twist, flowing sleeve in foreground::, {{cinnabar red, azurite blue, ivory and antique gold theme}}, 1girl, solo, burgundy hair, very long loose braid, asymmetric bangs, hair behind ear, yellow eyes, white pupils, tsurime, 1.3::red eyeshadow::, skin fang, black stud earrings, flat chest, intense gaze, Dunhuang-inspired hanfu, translucent wide sleeves, red cross-collar bodice, deep blue embroidered skirt, gold jewelry, red flying ribbons, tilted composition, slight low angle, luminous silk, dark simple background
```

</details>

## 文件结构

```text
tag/
├─ assets/                  # 来源图片
├─ examples/                # 创作结果
├─ LICENSE                  # MIT License
├─ SKILL.md                 # Skill 规则与工作流程
├─ README.md                # 中文项目与格式说明
├─ README.en.md             # English README
├─ README.ko.md             # 한국어 README
├─ README.ru.md             # Русский README
└─ references/              # 通用创作方法与语法参考
```

## License

本仓库采用 [MIT License](LICENSE)。来源法典及来源作者原有内容的权利归原作者所有。
