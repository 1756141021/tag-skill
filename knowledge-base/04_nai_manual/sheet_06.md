---
doc_type: nai_manual_sheet
dataset_version: 1.0.0
schema_version: 1.0.0
database_content_signature: 6477e0baa7c416a2a5f2bca0272f1223a6f33aceeb20a29bb621e3c1ccd96c32
sheet_name: 线稿决策
record_count: 26
source_files:
- 00_input/nai_tag_manual.xlsx
---

# NAI 手册 · 线稿决策

> 来源：00_input/nai_tag_manual.xlsx · 工作表「线稿决策」｜共 26 条｜数据集 v1.0.0

### 分组：▸ 问一：有没有独立线稿

- **lineart**  <sub>行 4</sub>
  - 中文含义：有线稿（通用）
  - 四问对应：问一
  - 识别方法：有清晰的线条划出轮廓
  - 常见搭配：cel shading / anime
- **outlined**  <sub>行 5</sub>
  - 中文含义：有轮廓线
  - 四问对应：问一
  - 识别方法：所有物体有清楚边框
  - 常见搭配：thick outlines / bold
- **no lineart**  <sub>行 6</sub>
  - 中文含义：无线稿
  - 四问对应：问一
  - 识别方法：靠颜色对比区分边界
  - 常见搭配：painterly / no outline
- **no outline**  <sub>行 7</sub>
  - 中文含义：无轮廓线
  - 四问对应：问一
  - 识别方法：完全无线条，颜色融合
  - 常见搭配：soft shading / painterly
- **color-defined edges**  <sub>行 8</sub>
  - 中文含义：颜色定义边缘
  - 四问对应：问一
  - 识别方法：边界靠颜色过渡区分
  - 常见搭配：painterly / impressionist
### 分组：▸ 问二：外轮廓vs内部线粗细

- **thick outlines**  <sub>行 10</sub>
  - 中文含义：厚重轮廓线
  - 四问对应：问二
  - 识别方法：外边缘线明显粗且深
  - 常见搭配：bold lineart / anime
- **bold outline**  <sub>行 11</sub>
  - 中文含义：粗轮廓（强调版）
  - 四问对应：问二
  - 识别方法：外轮廓极粗，视觉冲击强
  - 常见搭配：comic / western cartoon
- **heavy lineart**  <sub>行 12</sub>
  - 中文含义：重线稿
  - 四问对应：问二
  - 识别方法：整体线条都粗而深
  - 常见搭配：manga / retro anime
- **thin lines**  <sub>行 13</sub>
  - 中文含义：细线稿
  - 四问对应：问二
  - 识别方法：线条纤细，几乎可见边界
  - 常见搭配：delicate / shoujo
- **fine lines**  <sub>行 14</sub>
  - 中文含义：精细线
  - 四问对应：问二
  - 识别方法：线条极细极均匀
  - 常见搭配：mechanical / technical
- **delicate lineart**  <sub>行 15</sub>
  - 中文含义：精致线稿
  - 四问对应：问二
  - 识别方法：细腻，内外等粗
  - 常见搭配：shoujo manga / elegant
- **uniform line weight**  <sub>行 16</sub>
  - 中文含义：等粗线稿
  - 四问对应：问二
  - 识别方法：内外线条粗细相同
  - 常见搭配：shounen style
- **variable line weight**  <sub>行 17</sub>
  - 中文含义：粗细变化线
  - 四问对应：问二
  - 识别方法：线条有粗有细，有压感
  - 常见搭配：ink / traditional
### 分组：▸ 问三：线条颜色

- **black lineart**  <sub>行 19</sub>
  - 中文含义：黑色线稿
  - 四问对应：问三
  - 识别方法：纯黑色线条
  - 常见搭配：默认，不需要特别写
- **colored lineart**  <sub>行 20</sub>
  - 中文含义：有色线稿
  - 四问对应：问三
  - 识别方法：线条带颜色（非纯黑）
  - 常见搭配：彩色线稿风格
- **color-matched lines**  <sub>行 21</sub>
  - 中文含义：颜色匹配线
  - 四问对应：问三
  - 识别方法：线条颜色与区域颜色相近
  - 常见搭配：法式BD漫画风
- **multicolored lineart**  <sub>行 22</sub>
  - 中文含义：多色线稿
  - 四问对应：问三
  - 识别方法：不同区域线条不同颜色
  - 常见搭配：特定画师风格
- **white outline**  <sub>行 23</sub>
  - 中文含义：白色轮廓
  - 四问对应：问三
  - 识别方法：深色背景上用白线
  - 常见搭配：暗调风格/夜晚场景
- **glowing outline**  <sub>行 24</sub>
  - 中文含义：发光轮廓
  - 四问对应：问三
  - 识别方法：线条有光晕效果
  - 常见搭配：幻想/魔法/赛博
### 分组：▸ 问四：线条质感（硬/抖）

- **clean lines**  <sub>行 26</sub>
  - 中文含义：干净线条
  - 四问对应：问四
  - 识别方法：流畅，无抖动，无杂线
  - 常见搭配：商业插画/标准动漫
- **smooth lines**  <sub>行 27</sub>
  - 中文含义：顺滑线条
  - 四问对应：问四
  - 识别方法：极度流畅均匀
  - 常见搭配：CG/数字插画
- **tapered lines**  <sub>行 28</sub>
  - 中文含义：末端收尖的线
  - 四问对应：问四
  - 识别方法：线条末端有收笔尖角
  - 常见搭配：很多日系画师特征
- **sketchy**  <sub>行 29</sub>
  - 中文含义：草稿感线条
  - 四问对应：问四
  - 识别方法：有手绘抖动感，线条不精确
  - 常见搭配：概念草图/casual风
- **rough lines**  <sub>行 30</sub>
  - 中文含义：粗糙线条
  - 四问对应：问四
  - 识别方法：线条有明显不规则感
  - 常见搭配：手作/raw风格
- **hand-drawn feel**  <sub>行 31</sub>
  - 中文含义：手绘感
  - 四问对应：问四
  - 识别方法：有手的温度，不追求完美
  - 常见搭配：indie插画/zine风格
- **scratchy lines**  <sub>行 32</sub>
  - 中文含义：划痕感线条
  - 四问对应：问四
  - 识别方法：线条有短促叠加感
  - 常见搭配：蚀刻版画/素描
