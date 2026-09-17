# NAI 多人分区

仅在 NAI 多人、关系动作或串特征任务中读取。以下为原技能的版本相关记录，本次未重新核验当前界面或数量上限。

原稿记录两种组织方式；数量上限按目标版本核对，不将来源中的界面上限与实验数量当作统一保证。

**方式一：角色分区（Character Panels，推荐）**
- 网页界面点击提示框下方 `+ Add Character` 按钮，为每个角色添加独立提示框
- 框的**顺序决定角色在画面中的位置**（从上到下、从左到右），可用上下箭头重排
- **位置指定（Position）**：先关闭「AI's Choice」开关。V4/V4.5 旧版：点角色框内 Position 按钮 → 弹 5×5 网格 → 点格子 → Done；**V5 起 Position UI 重构为自由画布摆放**（不再有网格限制），模型会紧密跟随设置的位置
- **V5 另辟径**：直接在自然语言中描述布局（如 `standing on the left`、`side-by-side`），或两者结合
- 官方提示：位置是"粗略引导/轻微建议"，**不要与框顺序冲突**，并用自然语言强化；V5 测试中最多能同时摆 22 个角色
- **存在任何角色面板时 `|` 语法被禁用**，二者不能混用

**方式二：`|` 分隔（文本提示法）**

```
2girls, 场景/风格/构图 | girl, 角色A全部特征, source#动作 | girl, 角色B全部特征, target#动作
```

规则：
- **数量词放基础段**：`2girls` / `2boys` 写在基础 prompt；每个角色段用单数 `girl` / `boy` / `other`，不带数量
- **角色段只写该角色**：外貌/服装/表情全部放对应角色段，减少信息泄漏（防串角色）
- **互动动作前缀**：`source#`（施加方）/ `target#`（承受方）/ `mutual#`（互相）放在对应角色段；官方注明该前缀**并非总是可靠，但多数情况有帮助**
- **基础段只写场景**：场景/风格/环境不放角色特征，防止模型把特征分错人
- V3 及以下 `|` 是 prompt mixing（提示混合），不能用于多人

官方示例：
```
2girls, indoors, factory, night, fog | girl, purple eyes, short hair, red blouse, target#pointing | girl, very long hair, purple hair, golden shirt, source#pointing at another
```

**SD 和 NAI 括号语法相反**——跨平台必须转换。
