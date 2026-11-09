# 来源与许可

本 skill 的文本与文档采用 [MIT 许可](LICENSE)。

## 配图工作流与资料组织

工作流与资料组织改编自 Ian 的 [Ian Xiaohei Illustrations](https://github.com/helloianneo/ian-xiaohei-illustrations)，参考版本为 [`8961915`](https://github.com/helloianneo/ian-xiaohei-illustrations/tree/8961915fcdbca57f288ec52b173056501d8a87f2)。原 MIT 版权声明已保留在同目录 [LICENSE](LICENSE) 中。

早期示例生成时使用过上游图片作为结构参考；这些图片现不随 skill 分发，实际提示词保留在[示例文档](https://github.com/9Ashwin/monthly-salary-cat-illustrations/blob/main/examples/prompts.md)中。

## 角色与生成示例

角色参考为 xiaoyyy 发布的 [monthly-salary-cat-fix](https://codex-pets.net/#/pets/monthly-salary-cat-fix)。[完整原始 WebP 精灵图](https://codex-pets.net/assets/pets/v/1784284488125/monthly-salary-cat-fix/spritesheet.webp) 不随技能分发，也不默认下载。本项目未取得作者的 SVG 原稿。原包未附独立许可文件，本 skill 的 MIT 许可仅适用于技能文本与文档。

`assets/character-reference/` 仅内置 4 张独立的 192×208 PNG，按原始网格裁取，保留原像素，没有缩放、重绘或重新生成角色。行列均从 0 起算：

| 图片 | 原始位置 |
| --- | --- |
| [front.png](assets/character-reference/front.png) | 第 3 行，第 0 列 |
| [side.png](assets/character-reference/side.png) | 第 1 行，第 0 列 |
| [gesture.png](assets/character-reference/gesture.png) | 第 2 行，第 0 列 |
| [working.png](assets/character-reference/working.png) | 第 6 行，第 0 列 |

默认只查看、传入 `front.png`，按当前姿态最多再加一张，不批量读取全部角色图。正常使用无需额外下载或安装宠物；需要其他原始动作时可从上述公开来源取得。

`assets/examples/` 中的 14 张 JPEG 是本项目原始生成 PNG 的缩小预览，最长边为 960 像素，不是原作者发布的宠物动作帧。[仓库示例目录](https://github.com/9Ashwin/monthly-salary-cat-illustrations/tree/main/examples/images)提供最长边 1280 像素、质量参数 80 的 JPEG 展示图；[固定历史提交](https://github.com/9Ashwin/monthly-salary-cat-illustrations/tree/76efeff45dc4338d24e7197fbc4baa3f84395f4a/examples/images)保留原始 PNG。两组 JPEG 均由原图缩小、转码得到，没有重新生图。MIT 许可不授予对第三方角色、名称或原始素材的权利，示例不表示原作者授权或背书。

完整来源记录见[项目 NOTICE](https://github.com/9Ashwin/monthly-salary-cat-illustrations/blob/main/NOTICE.md)，实际生成提示词见[示例文档](https://github.com/9Ashwin/monthly-salary-cat-illustrations/blob/main/examples/prompts.md)。
