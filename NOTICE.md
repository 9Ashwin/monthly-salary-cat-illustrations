# 来源与许可

本项目的 skill 文本与文档采用 [MIT 许可](LICENSE)。第三方角色、原始素材和生成示例的来源及许可范围如下。

## 配图工作流与资料组织

工作流与参考资料组织改编自 Ian 的 [Ian Xiaohei Illustrations](https://github.com/helloianneo/ian-xiaohei-illustrations)，参考版本为 [`8961915`](https://github.com/helloianneo/ian-xiaohei-illustrations/tree/8961915fcdbca57f288ec52b173056501d8a87f2)。原项目采用 MIT 许可，`Copyright (c) 2026 Ian` 已保留在本仓库 [LICENSE](LICENSE) 中。

本项目调整了角色、配色、提示词和检查规则。早期示例生成时使用过上游图片作为结构参考；这些图片现不随仓库分发，实际生成提示词仍保留在 [examples/prompts.md](examples/prompts.md) 中。

## 月薪喵角色

角色参考为 xiaoyyy 发布的 [monthly-salary-cat-fix](https://codex-pets.net/#/pets/monthly-salary-cat-fix)。[原始精灵图](https://codex-pets.net/assets/pets/v/1784284488125/monthly-salary-cat-fix/spritesheet.webp) 是 1536×2288 的 WebP 栅格图。2026-11-07 核对的下载包包含 `pet.json` 和 `spritesheet.webp`，本项目未取得作者的 SVG 原稿。

发布者身份不代表原角色版权归属。原始素材的再分发许可尚未确认，因此仓库不包含原图、完整动作帧或描摹版；使用时读取公开源或用户提供的参考。MIT 许可不授予对月薪喵角色、名称或第三方原始素材的权利。

## 生成示例

[examples/images/](examples/images/) 与 [skill 内的示例目录](skills/monthly-salary-cat-illustrations/assets/examples/) 保存同一组 14 张 PNG 配图。每张图均由独立 AI 执行者读取 skill 和正文任务后生成，实际提示词见 [examples/prompts.md](examples/prompts.md)，验证方法与记录见 [evals/README.md](evals/README.md)。

这些图片是新场景的生成示例，不是原作者发布的宠物动作帧或 SVG 原稿。示例中的第三方角色不因仓库开源而被重新授权，示例也不表示原作者授权或背书。本项目与原角色作者、宠物发布者及 OpenAI 无官方关联。

## 目录组织

`skills/<skill-name>/` 与 `.claude-plugin/` 的目录组织参考 [smallnest/goal-workflow](https://github.com/smallnest/goal-workflow)，未复制其技能内容或工作流脚本。
