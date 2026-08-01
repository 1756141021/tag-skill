# TAG

[简体中文](README.md) | [English](README.en.md) | [한국어](README.ko.md) | [Русский](README.ru.md)

AI 그림 프롬프트를 작성하기 위한 skill입니다. 캐릭터, 동작, 구도, 환경, 스타일 요구 사항을 바탕으로 다양한 이미지 모델에 맞는 프롬프트를 생성합니다.

마음에 드셨다면 이 저장소에 Star를 눌러 주세요.

## 설치

이 skill은 별도의 의존성을 설치할 필요가 없습니다. 저장소를 해당 skills 디렉터리에 클론하기만 하면 됩니다.

### Claude Code

Windows CMD:

```cmd
git clone https://github.com/1756141021/tag-skill "%USERPROFILE%\.claude\skills\tag"
```

macOS / Linux:

```bash
git clone https://github.com/1756141021/tag-skill ~/.claude/skills/tag
```

설치가 끝나면 Claude가 요청에 따라 자동으로 호출하게 할 수도 있고, `/tag`를 입력해 수동으로 호출할 수도 있습니다. `.claude/skills`가 현재 Claude Code 세션을 시작한 뒤 처음 만들어졌다면 Claude Code를 다시 시작하세요.

### Pi

Windows CMD:

```cmd
git clone https://github.com/1756141021/tag-skill "%USERPROFILE%\.pi\agent\skills\tag"
```

macOS / Linux:

```bash
git clone https://github.com/1756141021/tag-skill ~/.pi/agent/skills/tag
```

설치가 끝나면 Pi가 요청에 따라 자동으로 로드하게 할 수도 있고, `/skill:tag`를 입력해 수동으로 로드할 수도 있습니다.

## 선택적 개인화 자료

사용자는 필요에 따라 `references/`에 다음 파일을 만들 수 있습니다. 이 파일들은 개인 창작 선호도를 저장하며, skill 실행에 필수는 아닙니다.

- **OC 외형 라이브러리** (`oc-library.md`): 캐릭터 이름별로 머리카락 색, 눈동자 색, 헤어스타일, 체형, 종족 특징 등 눈에 보이는 외형을 저장합니다. 캐릭터를 지정하면 skill이 이러한 특징을 추출해 화면의 시선 흐름에 맞춰 프롬프트에 녹여 내며, 템플릿 전체를 그대로 복사하지 않습니다.
- **창작 컨텍스트** (`context-anchor.md`): 장기적으로 유지하고 싶은 창작 방향, 언어 습관, 용어 규칙을 저장합니다.
- **사용한 시구 기록** (`used-poems.md`): 사용 날짜, 시구 출처, 장면 요약을 기록해 짧은 기간에 같은 시구를 반복 사용하는 일을 줄입니다.

OC 라이브러리가 없거나 라이브러리에 지정한 캐릭터가 없을 때는 요청에 캐릭터 외형을 직접 적으면 됩니다.

## 출처 및 감사의 말

이 skill의 창작 방법은 **戒红所** (`red_relief_reformatory`)의 TAG 법전을 바탕으로 증류했으며, 작성자만의 프롬프트 해석과 작은 아이디어를 더했습니다. 여기에서 원래 방법의 출처를 밝힙니다.

![출처 저자: 戒红所](assets/source-author.png)

이 저장소는 법전에 담긴 창작 경험을 실행 가능한 skill 작업 흐름과 플랫폼별 출력 규칙으로 정리했습니다.

이 skill의 초기 증류는 Opus 4.6 시기에 Opus 4.6을 사용해 진행했습니다. 당시 모델 성능과 정리 방식의 한계로, 현재 Fable이나 다른 모델로 다시 증류한 결과보다 품질이 낮을 수 있습니다.

## 지원 형식

### Stable Diffusion（SD）

영어 자연어 동작 설명에 Danbooru TAG를 함께 사용하며, `(tag:1.3)`, `[tag]`, `BREAK`와 같은 A1111 가중치 문법을 사용합니다.

### NovelAI（NAI）

영어 자연어 동작 설명에 Danbooru TAG를 함께 사용하며, `{tag}`, `1.2::tag::`, `[tag]`와 같은 NovelAI 가중치 문법으로 변환합니다.

### Anima

**SD TAG + 자연어 설명**을 사용합니다. 자연어는 동작, 자세, 인물 간 상호작용과 공간 관계를 담당하고, SD TAG는 외모, 의상, 장면과 화면 효과를 담당합니다.

### Krea 2

**중국어 자연어만** 사용해 주요 대상, 동작, 자세, 구도, 환경, 조명과 화면 스타일을 자세히 설명하며, Danbooru TAG나 가중치 문법은 사용하지 않습니다.

> 현재 Anima와 Krea 2는 별도로 연구하지 않았습니다. 위 내용은 현 단계에서 정한 출력 형식만 기록한 것이며, 모델 특성에 맞춘 체계적인 검증이나 최적화가 완료되었다는 뜻은 아닙니다.

## 창작 결과

다음 네 가지 결과는 모두 먼저 참고 이미지에서 캐릭터 외형을 역추론한 뒤, 캐릭터를 알아볼 수 있는 특징은 유지하면서 skill이 동작, 구도, 장면과 색상 구성을 자유롭게 설계했습니다.

### 1. 자수정과 먹빛의 두 날개

<img src="examples/01-violet-crystal.png" alt="검은 머리와 왕관을 쓴 소녀가 자수정을 들고 있고, 먹빛 날개가 뒤에서 펼쳐지는 모습" width="480">

<details>
<summary>프롬프트 보기</summary>

```text
A crowned black-haired girl crushes a violet crystal between her palms, and its light erupts into two enormous ink-black wings as her hair lashes outward,
1.5::shattering violet crystal, black liquid wings bursting from her back, overwhelming magical pressure, figure filling the frame::, {{ink black, paper white, electric violet and smoke gray theme}}, 1girl, solo, pale skin, very long black hair, straight bangs, glowing purple eyes, silver crystal crown, cold focused expression, ornate white ceremonial dress, high ruffled collar, puff sleeves, fitted black waist, silver jewelry, hands together, violet flame, crystal fragments, sweeping hair, black ink splashes, floating dark petals, stark white background, strong symmetrical composition, monochrome with selective purple, rough ink texture, high-contrast anime illustration, -2::text, logo, watermark::
```

</details>

### 2. 빙판 위의 턴

<img src="examples/02-ice-skater.png" alt="동물 귀를 가진 금발 소녀가 실내 빙판에서 빠르게 방향을 전환하는 모습" width="480">

<details>
<summary>프롬프트 보기</summary>

```text
A blonde animal-eared girl carves a sharp turn across an indoor ice rink, extending one arm as her long braid, teal ribbons, and a fan of ice spray sweep behind her,
1.45::one-foot skating turn, body leaning into the curve, clean extended pose, explosive ice spray::, {{cream white, deep teal, ice blue and pale gold theme}}, 1girl, solo, blonde hair, very long hair, thick side braid, long sidelocks, animal ears, cream inner ear fur, aqua eyes, white pupils, blue stitch marks across nose bridge, small pout, teal maid headband, teal neck bow, gemstone brooch, teal and white skating dress, fitted bodice, frilled collar, layered skirt, white tights, teal ice skates, indoor ice rink, curved skate marks, glossy ice reflections, floating ice particles, overhead spotlights, blurred railing, dynamic anime illustration
```

</details>

### 3. 붉은 막을 열고 등장

<img src="examples/03-crimson-curtain-maid.png" alt="고양이 귀를 가진 악마 메이드가 붉은 무대 커튼을 여는 모습" width="480">

<details>
<summary>프롬프트 보기</summary>

```text
A cat-eared demon maid throws open two heavy crimson curtains and steps onto the stage, her long twintails, ribbons, and layered skirt flaring outward in the sudden light,
1.45::both hands pulling the curtains apart, dramatic entrance, strong forward step, clean flowing silhouette::, {{charcoal black, porcelain white, crimson red and icy blue theme}}, 1girl, solo, petite, dark purple hair, very long twintails, curled hair ends, red inner hair, blunt bangs, gray eyes, blush, black cat ears, pink inner ears, blue flower hair ornament, black and red hair ribbons, white maid headband, black choker, black and white maid dress, corset bodice, puff sleeves, long black gloves, layered frilled skirt, white thighhighs, garter straps, black shoes, small white bat wings, black spade-tipped tail, red tail bow, crimson theater curtains, wooden stage, warm footlights, dark simple background, dynamic anime illustration
```

</details>

### 4. 둔황풍으로 흩날리는 소매

<img src="examples/04-dunhuang-hanfu.png" alt="버건디색 머리의 여성이 둔황풍 한푸를 입고 투명한 소매와 붉은 리본이 렌즈를 스쳐 지나가는 모습" width="480">

<details>
<summary>프롬프트 보기</summary>

```text
A burgundy-haired woman twists toward the viewer, lifting a translucent sleeve across her mouth as her braid and red ribbons sweep past the lens,
1.5::close-up, figure filling the frame, strong body twist, flowing sleeve in foreground::, {{cinnabar red, azurite blue, ivory and antique gold theme}}, 1girl, solo, burgundy hair, very long loose braid, asymmetric bangs, hair behind ear, yellow eyes, white pupils, tsurime, 1.3::red eyeshadow::, skin fang, black stud earrings, flat chest, intense gaze, Dunhuang-inspired hanfu, translucent wide sleeves, red cross-collar bodice, deep blue embroidered skirt, gold jewelry, red flying ribbons, tilted composition, slight low angle, luminous silk, dark simple background
```

</details>

## 파일 구조

```text
tag/
├─ assets/                  # 출처 이미지
├─ examples/                # 창작 결과
├─ LICENSE                  # MIT License
├─ SKILL.md                 # Skill 규칙과 작업 흐름
├─ README.md                # 중국어 README
├─ README.en.md             # 영어 README
├─ README.ko.md             # 한국어 README
├─ README.ru.md             # 러시아어 README
└─ references/              # 일반 창작 방법과 문법 참고 자료
```

## 라이선스

이 저장소는 [MIT License](LICENSE)를 적용합니다. 출처가 된 법전과 원저자가 작성한 기존 콘텐츠의 권리는 원저자에게 있습니다.
