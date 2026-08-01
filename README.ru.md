# TAG

[简体中文](README.md) | [English](README.en.md) | [한국어](README.ko.md) | [Русский](README.ru.md)

Skill для создания промптов для генерации изображений с помощью ИИ. Он создаёт промпты для разных моделей с учётом требований к персонажу, действию, композиции, окружению и стилю.

Если проект вам понравился, поставьте ему звезду.

## Установка

Этот skill не требует дополнительных зависимостей. Достаточно клонировать репозиторий в соответствующий каталог skills.

### Claude Code

Windows CMD:

```cmd
git clone https://github.com/1756141021/tag-skill "%USERPROFILE%\.claude\skills\tag"
```

macOS / Linux:

```bash
git clone https://github.com/1756141021/tag-skill ~/.claude/skills/tag
```

После установки Claude сможет вызывать skill автоматически по запросу, а вы сможете запустить его вручную командой `/tag`. Если каталог `.claude/skills` впервые был создан после запуска текущей сессии Claude Code, перезапустите Claude Code.

### Pi

Windows CMD:

```cmd
git clone https://github.com/1756141021/tag-skill "%USERPROFILE%\.pi\agent\skills\tag"
```

macOS / Linux:

```bash
git clone https://github.com/1756141021/tag-skill ~/.pi/agent/skills/tag
```

После установки Pi сможет загружать skill автоматически по запросу, а вы сможете запустить его вручную командой `/skill:tag`.

## Дополнительные материалы для персонализации

При необходимости пользователь может создать в `references/` следующие файлы. Они хранят индивидуальные творческие предпочтения пользователя и не являются обязательными для работы skill.

- **Библиотека внешности OC** (`oc-library.md`): хранит для каждого персонажа цвет волос, цвет глаз, причёску, телосложение, видовые особенности и другие заметные черты. После указания персонажа skill извлекает эти признаки и вписывает их в промпт с учётом пути взгляда по кадру, а не копирует шаблон целиком.
- **Контекст творчества** (`context-anchor.md`): хранит творческие принципы, языковые привычки и договорённости о терминах, которые нужно использовать в дальнейшем.
- **Журнал использованных стихотворных строк** (`used-poems.md`): записывает дату использования, источник строки и краткое описание изображения, чтобы одна и та же строка не повторялась в короткий срок.

Если библиотеки OC нет или в ней отсутствует нужный персонаж, просто укажите внешность персонажа прямо в запросе.

## Источник и благодарности

Методика этого skill создана на основе кодекса TAG автора **戒红所** (`red_relief_reformatory`) и дополнена авторским пониманием промптов и небольшими творческими находками. Здесь указан источник исходной методики.

![Автор исходной методики: 戒红所](assets/source-author.png)

В этом репозитории творческий опыт из кодекса оформлен в рабочий процесс skill и правила вывода для разных платформ.

Первоначальная дистилляция этого skill была выполнена в период Opus 4.6 с помощью Opus 4.6. Из-за ограничений модели и способа систематизации того времени её результат может уступать результату повторной дистилляции с помощью Fable или другой современной модели.

## Поддерживаемые форматы

### Stable Diffusion（SD）

Использует описания действий на естественном английском языке вместе с Danbooru TAG, а также синтаксис весов A1111, например `(tag:1.3)`, `[tag]` и `BREAK`.

### NovelAI（NAI）

Использует описания действий на естественном английском языке вместе с Danbooru TAG и преобразует их в синтаксис весов NovelAI, например `{tag}`, `1.2::tag::` и `[tag]`.

### Anima

Использует **SD TAG + описание на естественном языке**. Естественный язык отвечает за действия, позы, взаимодействие персонажей и пространственные отношения, а SD TAG отвечает за внешность, одежду, сцену и визуальные эффекты.

### Krea 2

Использует **только естественный язык на китайском** для подробного описания объекта, действия, позы, композиции, окружения, освещения и визуального стиля. Danbooru TAG и синтаксис весов не используются.

> Anima и Krea 2 пока не исследовались специально. Этот раздел фиксирует только текущие договорённости о формате вывода и не означает, что особенности моделей прошли систематическую проверку или оптимизацию.

## Результаты

Во всех четырёх примерах внешность персонажа сначала восстановили по референсному изображению. Затем skill свободно разработал действие, композицию, сцену и цветовую схему, сохранив узнаваемые черты персонажа.

### 1. Аметист и чернильные крылья

<img src="examples/01-violet-crystal.png" alt="Черноволосая девушка в короне держит аметист, а за её спиной раскрываются чернильные крылья" width="480">

<details>
<summary>Показать промпт</summary>

```text
A crowned black-haired girl crushes a violet crystal between her palms, and its light erupts into two enormous ink-black wings as her hair lashes outward,
1.5::shattering violet crystal, black liquid wings bursting from her back, overwhelming magical pressure, figure filling the frame::, {{ink black, paper white, electric violet and smoke gray theme}}, 1girl, solo, pale skin, very long black hair, straight bangs, glowing purple eyes, silver crystal crown, cold focused expression, ornate white ceremonial dress, high ruffled collar, puff sleeves, fitted black waist, silver jewelry, hands together, violet flame, crystal fragments, sweeping hair, black ink splashes, floating dark petals, stark white background, strong symmetrical composition, monochrome with selective purple, rough ink texture, high-contrast anime illustration, -2::text, logo, watermark::
```

</details>

### 2. Разворот на льду

<img src="examples/02-ice-skater.png" alt="Светловолосая девушка с ушками животного быстро разворачивается на крытом катке" width="480">

<details>
<summary>Показать промпт</summary>

```text
A blonde animal-eared girl carves a sharp turn across an indoor ice rink, extending one arm as her long braid, teal ribbons, and a fan of ice spray sweep behind her,
1.45::one-foot skating turn, body leaning into the curve, clean extended pose, explosive ice spray::, {{cream white, deep teal, ice blue and pale gold theme}}, 1girl, solo, blonde hair, very long hair, thick side braid, long sidelocks, animal ears, cream inner ear fur, aqua eyes, white pupils, blue stitch marks across nose bridge, small pout, teal maid headband, teal neck bow, gemstone brooch, teal and white skating dress, fitted bodice, frilled collar, layered skirt, white tights, teal ice skates, indoor ice rink, curved skate marks, glossy ice reflections, floating ice particles, overhead spotlights, blurred railing, dynamic anime illustration
```

</details>

### 3. Выход под красным занавесом

<img src="examples/03-crimson-curtain-maid.png" alt="Демоническая горничная с кошачьими ушками раздвигает красный театральный занавес" width="480">

<details>
<summary>Показать промпт</summary>

```text
A cat-eared demon maid throws open two heavy crimson curtains and steps onto the stage, her long twintails, ribbons, and layered skirt flaring outward in the sudden light,
1.45::both hands pulling the curtains apart, dramatic entrance, strong forward step, clean flowing silhouette::, {{charcoal black, porcelain white, crimson red and icy blue theme}}, 1girl, solo, petite, dark purple hair, very long twintails, curled hair ends, red inner hair, blunt bangs, gray eyes, blush, black cat ears, pink inner ears, blue flower hair ornament, black and red hair ribbons, white maid headband, black choker, black and white maid dress, corset bodice, puff sleeves, long black gloves, layered frilled skirt, white thighhighs, garter straps, black shoes, small white bat wings, black spade-tipped tail, red tail bow, crimson theater curtains, wooden stage, warm footlights, dark simple background, dynamic anime illustration
```

</details>

### 4. Дуньхуанские летящие рукава

<img src="examples/04-dunhuang-hanfu.png" alt="Женщина с волосами цвета бургундского вина в ханьфу в стиле Дуньхуана, прозрачный рукав и красные ленты проносятся перед объективом" width="480">

<details>
<summary>Показать промпт</summary>

```text
A burgundy-haired woman twists toward the viewer, lifting a translucent sleeve across her mouth as her braid and red ribbons sweep past the lens,
1.5::close-up, figure filling the frame, strong body twist, flowing sleeve in foreground::, {{cinnabar red, azurite blue, ivory and antique gold theme}}, 1girl, solo, burgundy hair, very long loose braid, asymmetric bangs, hair behind ear, yellow eyes, white pupils, tsurime, 1.3::red eyeshadow::, skin fang, black stud earrings, flat chest, intense gaze, Dunhuang-inspired hanfu, translucent wide sleeves, red cross-collar bodice, deep blue embroidered skirt, gold jewelry, red flying ribbons, tilted composition, slight low angle, luminous silk, dark simple background
```

</details>

## Структура файлов

```text
tag/
├─ assets/                  # Изображения-источники
├─ examples/                # Результаты
├─ LICENSE                  # MIT License
├─ SKILL.md                 # Правила и рабочий процесс skill
├─ README.md                # README на китайском
├─ README.en.md             # README на английском
├─ README.ko.md             # README на корейском
├─ README.ru.md             # README на русском
└─ references/              # Справочные материалы по общей методике и синтаксису
```

## Лицензия

Этот репозиторий распространяется по лицензии [MIT License](LICENSE). Права на исходный кодекс и оригинальные материалы автора исходной методики принадлежат первоначальному автору.
