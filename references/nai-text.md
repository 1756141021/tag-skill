# NAI 画面内文字

仅在用户确实需要文字或修正文字时读取；未要求时不主动添加。以下引号法及 Text: 的区别是原稿经验，不代表所有版本的统一保证。

NAI V5 能渲染**可读文字**（英/日/中均可，中文经实战验证；短句可靠，长段会糊）。**官方文档的 `Text: ` 语法实测会把 "Text:" 字样本身渲染进画面，不要使用**；实战首选**引号法**：
- 用英文双引号把文字直接写在自然语言里并放在对应位置，如：`the words "博士的宠物" written on her left thigh`
- 搭配 tag：`text, english text`（英文）/ `speech bubble`（头顶气泡）/ `body writing`（身上写字）
- **位置固定在自然语言里写死（双维描述）**：身体部位 + 画面构图部位，如 `on her left thigh, at the lower right of the frame`、`inside a speech bubble above her head, in the upper center of the image`；多段文字各带完整位置描述（气泡台词 + 身上小字）
- 符号可混排：♡、…、！等均能渲染
- NSFW 常用：`body writing` + 引号文字写大腿/小腹，如 `the words "DOCTOR'S PET" written on her thigh`
