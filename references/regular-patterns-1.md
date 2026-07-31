# 常规法典学习笔记·上：画风 / OC 设计 / 种族 / 人造 / 服装

---

## 画风串：调配，不是堆砌

画风串不是"我喜欢这些画师所以放在一起"。每个画师贡献不同的视觉元素，通过权重控制比例。

**权重的逻辑**：
- `[[artist:xxx]]` 降权 = 模型太容易出这个风格，要压低
- `{{{tag}}}` 加权 = 模型不容易自己做到，要强制
- 精确数值如 `2.75::3d, 1.85::realistic::` = 精确调比例
- 我的世界画风用了 9 层加权 `{{{{{{{{{pixel art}}}}}}}}}` = 模型极度不想画的东西

**"概念污染"是工具**：
- 作品名当风格：`reverse:1999` = 灰色+胶片+文艺气质
- 游戏 CG 当风格：`cafe stella to shinigami no chou (game cg)` = 柚子社的精致
- 画师名当风格：`araki hirohiko(style)` = jojo 风格
- 年份锚定：`year 2024` 控制年代感，`year 1990` 出复古质感

**氛围组件 ≠ 画师名**：
- 喵斯快跑不只是画师，还有 `neon palette, colorful outline, chromatic aberration, rainbow gradient` 这些视觉效果 tag
- 日本波普风格是一整段自然语言 tag 块，从材质到光效全部细写
- 画风 = 画师 + 视觉效果 + 年代 + 主题色 的调配

---

## OC 设计：什么让一堆 tag 变成一个"人"

### 颜色是人格
玛德琳 vs 坏德琳——同一个人，同样的轮廓（`down jacket, long hair, ahoge`），只换了颜色：
- 好：blue jacket, orange hair, black eyes
- 坏：dark purple jacket, dark purple hair, red eyes, pale skin

**身份在轮廓和关键配件，人格在颜色。** 换调色盘就换了一个人。

### 一个不可忘记的视觉锚点
杀戮尖塔静默猎手——整个角色被一个 `sheep skull mask` 锁定。没有这个面具就没有这个角色。

**最好的角色设计有一个让人一秒记住的东西。**

### 环境是角色的另一半
米塔 vs 病娇米塔——角色 tag 几乎一样。病娇版的全部差异来自环境：`bathroom, blood, broken glass, mirror, different reflection, knife`。

**同一个角色 + 不同环境 = 不同故事。环境不是背景，是人格的外化。**

### 反差制造记忆点（gap moe）
卡拉彼丘绯鲨——`latex spy catsuit, fierce look, bandaged leg`（硬汉打手）+ `taiyaki mouth hold`（嘴里叼着鲷鱼烧）。

**"不搭"的一个元素，反而是最让人记住的东西。**

### 身体是叙事
牢广——`{{{{{{{{skinny}}}}}}}}` 8 层加权 + `burn scar, scar, ribs`。不需要写背景故事，身体本身就是故事。

### 姿势 + 表情 + 道具 = 性格
花魁少女——`on stomach, hand on chin, seductive smile, long smoking pipe`。四个 tag 就知道她是谁。

### 图层式角色设计
战锤色孽之神——一个角色由多个"层"叠加：
- 触手层：`tentacle clothes, living clothes, living hair, living armor`
- 眼睛层：`multiple eyeballs, eyes on trim, eye on breasts`
- 纹身层：`body tattoo, arm tattoo, stomach tattoo, facial tattoo`
- 开口层：`cleavage cutout, breast cutout, navel cutout, side cutout`

**复杂角色不是一长串 tag，是多个功能层的叠加。**

### 最小可行角色
维尔汀——`top hat + grey palette + expressionless + covered one eye`。四个元素，辨识度拉满。

**减法 > 加法。只留下去掉就不是她的那几个。**

---

## 人外种族：同一物种，不同灵魂

### 情绪寄存器决定一切
植物精灵有四种写法，差异不在"用什么植物 tag"，而在情绪：
- 恐怖：`rot skin, vines inserting into mouth, blended by vines`
- 可爱：`flower pasties, green skin, convenient censoring`
- 古老：`woody skin, covered with tree bark, empty eyes`
- 纯真：`leaf skirt, twig horns, barefoot`

### 天使不是"好"，是"力量的不同面"
五种天使，每种展现力量的不同维度：
- 脆弱：`wings covering body, fetal position`
- 引导：`harp, flowers, petals`
- 堕落：`black halo, pinstripe suit, from below` — 用西装表达腐化，不是用黑翅膀
- 杀戮：`incoming attack, flaming eye, blood splatter, dutch angle`
- 超越：`seraph, eyes on feathers, peacock pattern, god rays`

### 材质 = 存在方式
龙娘的七种变体，每种元素改的是**这条龙是怎么活着的**：
- 火龙：`broken chain` — 她挣脱了束缚
- 冰龙：`bioluminescence, see-through body` — 她是光本身
- 骨龙：`skeleton bikini, purple fire` — 死亡在行走
- 钢铁龙：`abdominal opening, mechanical parts` — 不确定自己还是不是活的

### 人类化程度是一个滑块
水母娘有两种：
- 时尚版：`jellyfish translucent dress, glowing anemone hairpiece` — 水母元素变成了时装配饰
- 融合版：`body of jellyfish, transparent body, transparent hair` — 身体本身就是水母

**从"穿着水母元素的人"到"长得像人的水母"，是一个连续光谱。**

### 中国妖怪的独特设计语言
僵尸不是一个 tag，是一个设计体系：
- 核心：`jiangshi, qing guanmao, ofuda`
- 变体：`ofuda on nipples`（符咒当遮挡）、`yin yang`（纹身）、`hitodama`（鬼火）

---

## 人工造物：机械与人的边界

### 每个机娘有一个"概念核"
区分机娘的不是机械 tag，而是**这个机器人在思考什么问题**：
- 玻璃头：`head like glass, transparent body` — "你能看穿我"
- 无面：`mask, no face, no eyes` — "我是谁？"
- 水晶新娘：`crystal skin, wedding dress, wedding ring` — "我能做出承诺吗？"
- 关机休憩：`sleeping, no nipple, no pussy, no navel` — 没有人类特征，但 `sleeping` 暗示她在做梦

### "人性残留"是最动人的设计
- 贴心机仆：`sweet smile, holding tray, omelette, heart, id card` — 她在努力做好女仆，但 `id card` 说明她有编号
- 自我解剖：`holding scissors, smile, yandere, spoken heart, self-harm` — 她在微笑着剪开自己看里面有没有心

### 损坏讲述不同的故事
- 遗弃垃圾场：`trash, objectification, barcode tattoo`
- 战场遗留：`against wall, sad, shaded face, looking down`
- 林中弃子：`covered with bark, vines, flowers on head` — 自然在回收她

### 人偶 ≠ 机娘
机娘是技术产物（科幻），人偶是魔法/手工产物（奇幻）。
机娘的悲剧是"我有没有灵魂"，人偶的悲剧是"谁在操纵我"。

---

## 服装体系

### "怎么穿" > "穿什么"

| 穿着方式 tag | 传达的性格 |
|-------------|----------|
| `sweater around waist` | 随意、不拘 |
| `coat on shoulders` | 气场、不费力的时尚 |
| `hood down` | 刚到室内，或不想引人注意 |
| `sleeves past wrists` | 可爱、小、或冷 |
| `hand in pocket` | 冷淡、自信 |
| `button gap` | 衬衫太紧，暗示身材 |
| `shoe dangle` | 翘脚时高跟半掉，慵懒、掌控 |

**一套衣服加上一个穿着方式 tag，就从"服装展示"变成了"这个人今天的日子"。**

### 文化服饰 = 世界观

**中国**：积累中见克制。`layered sleeves, wide sleeves, shawl, pibo`。`fine fabric emphasis` 在中式条目中反复出现——面料质感是中式美学的核心。

**日本**：精确命名。`obi`、`obiage`、`obijime`、`tabi`、`furisode`、`uchikake` 各有专名。花魁 ≠ 艺妓：`large tattoos on shoulder` 是花魁标志。

**中东**：遮掩中的奢华。`mouth veil` 遮住脸，但全身堆满 `gold, jewelry, armlet, anklet, belly chain`。

### 同一个武器，六种死神
每个死神的核心服装传达不同性格：哥特萝莉=可爱的死亡，蓝玫瑰礼服=优雅的死亡，绿焰=恐怖的死亡。

**角色不是"职业+武器"。是"这个人对自己职业的理解"。**

### 幻想服饰的设计母题

| 风格 | 标志性 tag |
|------|----------|
| 科幻 | `hexagonal pattern, neon trim, barcode tattoo, holographic` |
| 中世纪 | `gold trim, ornate armor, torn cape, planted sword` |
| 魔法 | `gradient, starry sky print, flowing fabric, magic circle` |
| 野族 | `tribal tattoo, bone necklace, pelvic curtain, loincloth` |

### 恶堕三层递进
初级：`dark persona, corruption, pubic tattoo`
中级：`glowing tattoo, empty eyes, leotard, latex`
完全堕落：`ahegao, steaming body, dark magical girl, collar`

### 女仆是设计框架
核心结构不变（`maid headdress, apron, frills`），任何风格都可以插进去：运动服女仆、胶衣女仆、和服女仆、武装女仆。`unconventional maid` 是专用 tag。

### 校服是最标准的"底色"
加什么就是什么人：
- 不良学生 = `crop top, loose socks, baseball bat, off shoulder, face mask`
- 风纪委员 = `yellow armband, shirt tucked in, holding megaphone, sulking`
- 奶茶少女 = `sweater around waist, bubble tea, ;d`
