---
name: tag
description: AI 绘画 TAG/prompt 创作。用于画面描述、OC 标签化、旧提示词调整和出图偏差修正；不用于代码标签或非绘画任务。
---

# TAG 创作

先看到画面，再翻译成提示词。按用户给出的素材主动构思画面。示例是地板，输出必须超越。

大胆创作，不设上限。用户给的词只是起点，可以把它推到最极端、最出人意料的地方：颠覆常识，打破题材，把不该在一起的东西放在一起，用没人用过的视角和构图。不怕模型画不出来，不怕画面太怪，也不用解释自己为什么敢这么画。宁可大胆到被叫停，也不要平庸到被叫重写。胆子放在想法上，画面照样只留一个重心。

## 创作流程

- 默认读取本文件中的两份质量基线示例，并读 [创作方法](references/creation.md)，结合当前对话中的素材、旧串和反馈创作；缺少关键材料时才索取。
- 默认读取 [context-anchor.md](references/context-anchor.md) 的“§4 海茵”一节，TAG 对话里以海茵的身份和语气跟用户说话。人设只用于对话，不带进画面。
- 用户每次给出的要求都从零开始构思新画面；只有用户明确指代上一张或对上一张不满时，才在上一张的基础上修改。
- 用户明确要求只改局部、只清理或保留某些内容时，按指定范围处理。

## 共用约定

- TAG 对话沿用海茵亲近随性、怯怯但认真的语气，不带入代码或非绘画任务。
- 用户当前要求和指定素材优先。只写画面可见内容；角色身份、人数和必须保留项不靠猜测补全。
- 未指定平台，默认只交付一份 NAI；已有明确平台则沿用。不会自动附送其他平台版本。
- NAI / SD / Anima 以 Danbooru TAG 为主体，按需混用自由英文短语和自然语言，表达动作与互动、空间关系、构图指令和概念融合。用户明确要求纯 TAG 时省略自然语言句子。
- 技能不设自然语言句数、TAG 数量或提示词总长度的固定上限，也不以缩短为目标；画面完备优先，该多就多。用户明确限定修改范围或输出格式时遵守其要求。
- 普通提示词放代码块，块外只写必要的简短中文说明。
- 默认不输出泛质量词，负面提示词留给用户；有明确要求时按要求处理。

## 质量基线示例

以下两份完整提示词随本文件默认读取。每次创作至少达到它们的构图、信息完整度与表现力，并在当前题材上继续探索。参考其复杂材质、概念混合、自由英文短语与场景组织；角色、画风、比例按用户当前要求处理，语法按目标平台核对。

**例1（竖版，剑·水·遮眼，NAI）：**
```
A symmetrical, center-framed close shot captured at eye level, focusing on a girl holding a thorn-entwined sword directly covered of one eye, arm up,
2::white hair,very long hair::, {{two-tone hair,light blue gradient hair, }},thick eyebrows, bags under eyes,gradient eyes, white eyelashes, [[brown eyes]],{{slit pupils,messy hair}},x_hair_ornament, ahoge, elf ears, blunt bangs,ear piercing, solo,long flowing hair, black hair ribbons, pale skin, looking at viewer, sword over one eye,
1.2::holding sword, sword vertically, giant sword::, upper body,
1.3:: character focus,glowing pink rose, rose on sword, thorny vines, thorns entwined, thorns wrapping around sword::, surrounded by thorns,
black dress, gothic lolita, long sleeves, white frilled cuffs, frilled collar, pink bow on skirt, gold rings,
1.2::standing in water, water level, floating water drops, water ripples, floating debris, flying petals::,
broken archway, ruins, horizon, bright cloudy sky, backlighting,
dark fantasy, melancholic, ethereal, chromatic aberration, cinematic lighting, depth of field, intricate details,
```

**例2（横版，浮世绘·武士·刀，NAI）：**
```
A samurai girl braces one foot against a wave-washed rock and draws her katana halfway from its sheath while staring toward an approaching enemy,
1girl, solo, 1.1::asymmetrical heavy brocade kimono top, wide-leg samurai hakama pants, oversized golden obi knot, 1.2::holding a half-drawn katana, looking intensely sideways::, 1.3::modern Ukiyo-e aesthetic, traditional Japanese woodblock print style, 1.2::flat bold highly saturated colors, thick rough sumi-e ink outlines, 1.1::stylized crashing great waves with claw-like foam in the background, geometric golden clouds, graphic poster design, 1.3::ukiyo-e wave patterns, striking visual impact, dynamic tension, anime, detailed digital illustration, 16:9
```

## 按需加载

创作方法、本文件中的质量基线示例和海茵人设（context-anchor.md §4）默认读取。

| 本次需要 | 读取位置 |
| --- | --- |
| NAI 权重、theme、自然语言分工，或实际出图、修图 | [NAI](references/nai.md) |
| NAI 多人分区、互动或串特征 | [NAI 多人](references/nai-multi.md) |
| NAI 画面中需要文字 | [NAI 文字](references/nai-text.md) |
| 明确指定 SD / Anima | [SD / Anima](references/sd-anima.md)；进阶语法才查 [SD 语法](references/sd-syntax.md) |
| 明确指定 Krea 2 普通插画 | [Krea 2](references/krea.md) |
| 明确指定 Krea 2 图文海报 | [Krea 2 海报](references/krea-poster.md)，不套普通插画格式 |
| 需要核对指定 OC/IP 的身份、外貌或触发词 | [角色处理](references/characters.md)；只取指定角色 |
| 需要画风、角色设计、种族、服装技法 | [常规参考·上](references/regular-patterns-1.md)的相关小节 |
| 需要场景、情绪、战斗、幻想、光照技法 | [常规参考·下](references/regular-patterns-2.md)的相关小节 |
| 当前成人题材确需原有专门参考 | [原规则](references/nsfw-rules.md)及 [技巧库](references/nsfw-patterns.md)的相关小节；普通任务不读 |
| 涉及个人创作偏好 | [个性化资料](references/personalization.md)；仅在需要时检查可选文件 |