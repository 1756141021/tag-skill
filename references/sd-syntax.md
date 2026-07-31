# SD 进阶 Prompt 语法速查

## AND — 同时生成多概念
```
(sun AND moon AND stars)
```
所有概念同时渲染在画面中。用于需要多个元素共存的场景。

## [word1|word2|word3] — 交替提示（Alternating）
```
[cat|dog|bird]
```
每一步采样轮流切换概念，产出三者的**融合体**——不是拼接，是混血。
**创作应用**：`[jellyfish|lantern|raindrop]` = 同时具有水母、灯笼、雨滴特征的新生物。

## [from:to:step] — 步数切换（Prompt Editing）
```
[painting:photograph:0.3]
```
前 30% 步数用第一个概念构图，之后切换到第二个概念细化。
- 前期步数影响**整体构图和大结构**
- 后期步数影响**细节和质感**
- 建议切换点 0.2-0.5
**创作应用**：`[underwater:dreamscape:0.3]` = 用水下物理感打底，再叠梦境质感。

## BREAK — 硬分隔 / 区域分割
```
prompt for region 1 BREAK prompt for region 2 BREAK prompt for region 3
```
配合 Regional Prompter 插件可把画面分成行/列区域，每区域独立控制 prompt。
- 比 AND 更强的概念隔离
- Divide Ratio 控制区域大小（如 1,1,1 等分 / 2,1,1 首区加倍）
- ADDBASE = 基础 prompt（全局生效）

## (word1|word2) — 管道切换（Pipe）
```
Portrait of (Stallone|Statham|DiCaprio)
```
逐步切换内容，括号内局部混合。效果类似交替提示但写法不同。

## OR — 随机选择
```
(red OR blue OR green) dress
```
每次生成随机选一个概念。用于批量出变体。

## 分隔符强度梯度
`,`（逗号）< `.`（句号）< `BREAK`
- **逗号**：软连接，元素之间保持关联
- **句号**：硬切，阻止前面的 token 污染后面
- **BREAK**：最硬的切割，区域级隔离

## 权重语法补充
- `(word:1.3)` = 精确权重
- `[word:0.3]` = 弱化（有地板效应，不会完全消失）
- `\/` = 转义符，需要字面括号时使用
