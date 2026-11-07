<div align="center">
  <h1>月薪喵正文配图</h1>
  <p>用月薪喵讲清文章里的步骤、分支与反馈<br>供 AI 助手使用的中文手绘配图技能</p>
  <p>
    <a href="LICENSE"><img src="https://img.shields.io/badge/Skill%20%26%20Docs-MIT-8c6549" alt="技能与文档：MIT 许可"></a>
    <a href="examples/README.md"><img src="https://img.shields.io/badge/Examples-14-d99b52" alt="14 张示例"></a>
    <a href="https://github.com/9Ashwin/monthly-salary-cat-illustrations/stargazers"><img src="https://img.shields.io/github/stars/9Ashwin/monthly-salary-cat-illustrations?style=social" alt="GitHub Stars"></a>
  </p>
  <h3>
    <a href="#install">安装</a> · <a href="#usage">使用</a> · <a href="#examples">示例</a> · <a href="examples/prompts.md">提示词</a> · <a href="NOTICE.md">来源与许可</a>
  </h3>
  <img src="examples/images/02-minimum-loop.png" alt="月薪喵操作内容流程：三类输入经过判断、产出与承接，反馈回到下一轮" width="1000">
</div>

## 这是什么？

`monthly-salary-cat-illustrations` 为中文文章、帖子和知识文档规划、生成或修改正文配图。它将内容关系变成管道、闸门、轨道、抽屉等具象装置，让月薪喵参与判断、分流和交接。

每张图解释一个核心结构，保留必要步骤、分支和反馈。角色以原始月薪喵参考为准，默认输出白底、16:9 横版 PNG。

<a id="install"></a>

## 开始使用

需要 Node.js 22.20 或更新版本，以及支持参考图生成和图片查看的 AI 助手。在目标项目目录运行：

```bash
npx skills add 9Ashwin/monthly-salary-cat-illustrations
```

按提示选择助手和安装范围。默认安装到当前项目；只安装给 Codex 时运行：

```bash
npx skills add 9Ashwin/monthly-salary-cat-illustrations --skill monthly-salary-cat-illustrations -a codex
```

<details>
<summary><strong>全局安装与手动安装</strong></summary>

为 Codex 全局安装，在任意目录运行：

```bash
npx skills add 9Ashwin/monthly-salary-cat-illustrations --skill monthly-salary-cat-illustrations -a codex -g
```

手动安装时，将整个 `skills/monthly-salary-cat-illustrations/` 目录复制到助手支持的技能目录。包内包含入口、参考资料、示例图、许可证和来源说明。更多安装参数见 [skills 安装工具](https://github.com/vercel-labs/skills)。

Node.js 用于运行安装工具，配图 skill 本身没有 Node 运行依赖。仓库另附 `.claude-plugin/` 元数据。

</details>

没有图像工具时，skill 可以提供配图规划和提示词，无法直接生成图片。原宠物素材不随安装包分发；使用时读取[公开原图](skills/monthly-salary-cat-illustrations/references/monthly-salary-cat-ip.md#先看原型)或用户提供的参考，无需安装宠物。

<a id="usage"></a>

## 怎么使用？

生成文章配图：

```text
使用 $monthly-salary-cat-illustrations，为下面的文章生成 3 张正文配图。
把关键步骤、分支和反馈讲清楚，让月薪喵参与判断与操作。

<粘贴文章>
```

先做规划：

```text
使用 $monthly-salary-cat-illustrations，阅读下面的文章，
建议值得配图的位置，说明每张图要解释的关系，先不要生图。

<粘贴文章>
```

修改已有图片：

```text
使用 $monthly-salary-cat-illustrations，将提供图片中的“反馈”改成“回看”，
保留其余文字、角色、动作和构图。
```

更多请求示例见 [examples/prompts.md](examples/prompts.md)。

## 适合画什么？

- **流程与闭环**：输入经过判断变成输出，反馈回到下一轮。
- **分支与承接**：材料按用途分流，读者从内容进入下一步。
- **前后对比**：呈现人工承重与系统承重、断点与修补。
- **方法与观点**：用物件和角色动作解释抽象关系。

生成过程为：读正文 → 提炼关系 → 查看参考 → 单张生成 → 检查保存。助手按 skill 完成关系草案和提示词，每张图独立生成；文字、形象或关系有误时，再做针对性修改。日常使用无需额外脚本或拼装流程。

<a id="examples"></a>

## 14 张配图示例

每张图均由独立 AI 执行者读取本 skill 和正文任务后生成。点击图片可查看原图；对应正文和实际图像提示词见 [examples/prompts.md](examples/prompts.md)，执行与检查记录见 [evals/](evals/README.md)。

| | |
| --- | --- |
| **01 · 两个断点**<br>![两个断点](examples/images/01-two-breakpoints.png) | **02 · 最小闭环**<br>![最小闭环](examples/images/02-minimum-loop.png) |
| **03 · 先判断用途**<br>![先判断用途](examples/images/03-sort-by-purpose.png) | **04 · 一份材料，多种用途**<br>![一份材料，多种用途](examples/images/04-one-source-many-uses.png) |
| **05 · 内容之后要有路**<br>![内容之后要有路](examples/images/05-handoff-path.png) | **06 · 三类信息如何汇合**<br>![三类信息如何汇合](examples/images/06-three-sources.png) |
| **07 · 三种内容的分工**<br>![三种内容的分工](examples/images/07-three-content-jobs.png) | **08 · 把重复回答留下来**<br>![把重复回答留下来](examples/images/08-reusable-toolbox.png) |
| **09 · 三个常见断点**<br>![三个常见断点](examples/images/09-common-pits.png) | **10 · 稳定的输入**<br>![稳定的输入](examples/images/10-information-well.png) |
| **11 · 从素材到判断**<br>![从素材到判断](examples/images/11-idea-press.png) | **12 · 让经验继续生长**<br>![让经验继续生长](examples/images/12-content-fermentation.png) |
| **13 · 让系统承重**<br>![让系统承重](examples/images/13-system-bearing.png) | **14 · 信任来自连续证据**<br>![信任来自连续证据](examples/images/14-trust-bridge.png) |

示例用于展示本轮生成结果。新主题需要重新分析和构图，生成后仍应检查形象、中文和连接关系。

<details>
<summary><strong>仓库目录</strong></summary>

```text
.
├── .claude-plugin/                     # 插件元数据
├── README.md
├── LICENSE
├── NOTICE.md
├── evals/                             # 正文任务与验证记录
├── examples/
│   ├── README.md                      # 示例索引
│   ├── prompts.md                     # 请求与实际生成提示词
│   └── images/                        # 14 张展示图
└── skills/
    └── monthly-salary-cat-illustrations/
        ├── SKILL.md                   # 技能入口
        ├── LICENSE
        ├── NOTICE.md
        ├── agents/openai.yaml
        ├── references/                # 风格、角色、构图、模板、检查
        └── assets/
            └── examples/              # 同一组示例，随技能安装
```

</details>

## 来源与许可

配图工作流与资料组织改编自 Ian 的 [Ian Xiaohei Illustrations](https://github.com/helloianneo/ian-xiaohei-illustrations)。角色参考为 xiaoyyy 发布的 [monthly-salary-cat-fix](https://codex-pets.net/#/pets/monthly-salary-cat-fix)。公开角色包提供 WebP 精灵图，本项目未取得作者的 SVG 原稿。

技能文本与文档采用 [MIT 许可](LICENSE)，第三方角色和原始素材的权利不随仓库重新授权。完整署名与生成示例说明见 [NOTICE.md](NOTICE.md)。
