# 2D 素材资源网站

这份笔记用于整理《灰烬之境》MVP 阶段可用的素材来源。当前只是个人验证和原型开发，优先级是快速找到“动作顺”的素材，而不是一开始就完全匹配最终美术风格。如果以后要发布，再逐个资源重新确认许可证。

## 推荐使用顺序

1. 先用现成的顺滑 spritesheet 验证移动手感。
2. 在 Godot 里验证跑、跳、攻击、受击、帧冻结等基础体验。
3. 手感成立后，再替换或重绘成“灰化者”的正式外观。
4. image2 / 图像生成更适合做概念图、背景、特效参考，不适合直接生成最终跑步帧动画。

## 网站列表

| 网站 | 适合找什么 | 许可证注意点 | 推荐搜索关键词 |
|---|---|---|---|
| [OpenGameArt](https://opengameart.org/) | 2D 角色帧动画、特效、tileset、音乐、音效 | 每个资源的许可证都不同。优先选 `CC0` 或宽松署名许可证。以后发布时要谨慎使用 `CC-BY-SA` 和 `GPL`。 | `side scroller character`, `platformer hero`, `animated character`, `slash spritesheet`, `dark fantasy`, `knight run` |
| [Kenney Assets](https://kenney.nl/assets) | 干净稳定的原型素材、UI、tiles、简单平台跳跃素材包 | Kenney 游戏素材通常是 `CC0`，不强制署名。缺点是风格偏明亮、玩具感，不太贴暗黑灰烬风格。 | `platformer`, `character`, `tiles`, `graveyard`, `UI`, `input prompts` |
| [Universal LPC Spritesheet Generator](https://liberatedpixelcup.github.io/Universal-LPC-Spritesheet-Character-Generator/) | 一致性很好的角色 spritesheet，可组合身体、衣服、武器等部件 | 不同部件可能是混合许可证。如果认真使用，要保留生成器给出的 credits。更偏 RPG 角色，不是纯横版动作角色。 | 在生成器里找 hood、cloak、leather、sword、dark palette 等部件 |
| [Universal LPC GitHub](https://github.com/LiberatedPixelCup/Universal-LPC-Spritesheet-Character-Generator) | LPC 资源的源码、credits、许可证细节 | 仓库代码是 GPL-3.0；美术资源有独立 credits / licenses。重点看 `CREDITS.csv` 和生成后的署名信息。 | 在仓库里搜 `credits`, `license`, `spritesheets` |
| [itch.io 免费 2D Sprites](https://itch.io/game-assets/free/tag-2d/tag-sprites) | 大量免费角色包、像素角色、怪物、特效 | `Free` 不等于开源，也不等于可商用。每个资源页都要单独看 License。个人玩和原型验证一般够用。 | 标签：`2D`, `Sprites`, `Characters`, `Animation`, `Platformer`, `Fantasy`, `Gothic`, `Pixel Art` |
| [Godot Asset Library](https://godotengine.org/asset-library/asset) | Godot 模板、工具、demo、动画和控制器示例 | 每个 asset 页面会列许可证。它更适合找 Godot 实现参考，不是主要美术资源站。 | 筛选：Godot `4.6`、`2D Tools`、`Templates`、`Demos`、许可证 `MIT` 或 `CC0` |

## 许可证速记

- 原型阶段最省心：`CC0`、`MIT`、`Unlicense`。
- 通常可以用但要署名：`CC-BY`、`OGA-BY`。
- 发布前要谨慎：`CC-BY-SA`、`GPL`、`LGPL`。
- 尽量避免作为项目长期资源：非商业、禁止演绎、不清楚的自定义许可证。

## 当前 MVP 的素材方向

当前 demo 阶段优先找“动作自然”的侧面角色跑步动画，不要先追求完全符合“灰化者”的外观。好的占位动画能更快暴露移动、镜头、攻击节奏、打击反馈是否成立。

第一阶段理想目标：

```text
一个侧视角角色。
包含 idle、run、jump、attack、hurt、death 动作。
优先 PNG spritesheet。
优先透明背景。
每帧尺寸一致，脚底基准线一致。
许可证优先 CC0；个人验证阶段可以先用个人免费素材。
```

## 关于 image2 / 图像生成

图像生成仍然有用，但不建议直接拿来生成最终连续帧动画。

适合用来做：

- 角色概念图。
- 单张强 pose。
- 背景氛围图。
- UI 草图。
- 攻击特效概念。
- 基于现成顺滑动画的换皮参考。

不适合直接做：

- 16 帧跑步循环。
- 需要脚底接地点稳定的动作。
- 连招动画。
- 剑长、披风、身体比例必须逐帧一致的动作。
- 任何强依赖帧间连续性的动画。
