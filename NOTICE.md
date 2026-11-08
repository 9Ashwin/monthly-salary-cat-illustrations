# 来源与许可

本项目的 skill 文本与文档采用 [MIT 许可](LICENSE)。第三方角色、原始素材和生成示例的来源及许可范围如下。

## 配图工作流与资料组织

工作流与参考资料组织改编自 Ian 的 [Ian Xiaohei Illustrations](https://github.com/helloianneo/ian-xiaohei-illustrations)，参考版本为 [`8961915`](https://github.com/helloianneo/ian-xiaohei-illustrations/tree/8961915fcdbca57f288ec52b173056501d8a87f2)。原项目采用 MIT 许可，`Copyright (c) 2026 Ian` 已保留在本仓库 [LICENSE](LICENSE) 中。

本项目调整了角色、配色、提示词和检查规则。早期示例生成时使用过上游图片作为结构参考；这些图片现不随仓库分发，实际生成提示词仍保留在 [examples/prompts.md](examples/prompts.md) 中。

## 月薪喵角色

角色参考为 xiaoyyy 发布的 [monthly-salary-cat-fix](https://codex-pets.net/#/pets/monthly-salary-cat-fix)。[原始精灵图](https://codex-pets.net/assets/pets/v/1784284488125/monthly-salary-cat-fix/spritesheet.webp) 是 1536×2288 的 WebP 栅格图，不随技能分发，也不默认下载。2026-11-07 核对的下载包包含 `pet.json` 和 `spritesheet.webp`，本项目未取得作者的 SVG 原稿。

技能仅内置以下 4 张独立的 192×208 PNG，按原始精灵图网格裁取，保留原像素，没有缩放、重绘或重新生成角色。行列均从 0 起算：

| 图片 | 原始位置 |
| --- | --- |
| [front.png](skills/monthly-salary-cat-illustrations/assets/character-reference/front.png) | 第 3 行，第 0 列 |
| [side.png](skills/monthly-salary-cat-illustrations/assets/character-reference/side.png) | 第 1 行，第 0 列 |
| [gesture.png](skills/monthly-salary-cat-illustrations/assets/character-reference/gesture.png) | 第 2 行，第 0 列 |
| [working.png](skills/monthly-salary-cat-illustrations/assets/character-reference/working.png) | 第 6 行，第 0 列 |

默认只查看、传入 `front.png`，按当前姿态最多再加一张，不批量读取全部角色图。需要其他原始动作时可从上述公开来源取得。

原包未附独立许可文件，发布者身份不代表原角色版权归属。本项目的 MIT 许可适用于技能文本与文档，不授予对月薪喵角色、名称或原始素材的权利。

## 生成示例

[examples/images/](examples/images/) 保存 14 张高清 PNG；[skill 内的示例目录](skills/monthly-salary-cat-illustrations/assets/examples/) 保存由这些原图缩小、转码得到的 JPEG 预览，最长边为 960 像素。两处对应相同的示例内容，文件格式与字节内容不同。高清图由独立 AI 执行者读取 skill 和正文任务后生成，实际提示词见 [examples/prompts.md](examples/prompts.md)，验证方法与记录见 [evals/README.md](evals/README.md)。

这些图片是新场景的生成示例，不是原作者发布的宠物动作帧或 SVG 原稿。示例中的第三方角色不因仓库开源而被重新授权，示例也不表示原作者授权或背书。本项目与原角色作者、宠物发布者及 OpenAI 无官方关联。

## 目录组织

`skills/<skill-name>/` 与 `.claude-plugin/` 的目录组织参考 [smallnest/goal-workflow](https://github.com/smallnest/goal-workflow)，未复制其技能内容或工作流脚本。
