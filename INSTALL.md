# 给 Agent 的安装说明

在用户要求安装本技能时执行。仓库为 `https://github.com/9Ashwin/monthly-salary-cat-illustrations`，只安装其中的 `skills/monthly-salary-cat-illustrations/`。

## 选择安装位置

用户明确指定目标 Agent 时按其要求安装；否则识别当前对话所在的 Agent，以宿主配置或已知技能目录为准，不根据电脑上安装了哪些应用来猜。遵循用户指定的安装范围；未指定时，skills CLI 使用当前项目，WorkBuddy 使用其用户配置目录。没有项目目录时，CLI 可使用用户级安装。

| 当前 Agent | 安装方式 | 项目级目录 | 用户级目录 |
| --- | --- | --- | --- |
| Codex | skills CLI，`--agent codex` | `.agents/skills/` | `~/.agents/skills/` |
| Claude Code | skills CLI，`--agent claude-code` | `.claude/skills/` | `~/.claude/skills/` |
| CodeBuddy | skills CLI，`--agent codebuddy` | `.codebuddy/skills/` | `~/.codebuddy/skills/` |
| WorkBuddy | 直接复制技能目录 | 以宿主项目配置为准 | `$WORKBUDDY_CONFIG_DIR/skills/`，默认 `~/.workbuddy/skills/` |
| 其他 Agent | 使用其支持的 CLI 目标或直接复制 | 以宿主配置为准 | 以宿主配置为准 |

目录有自定义配置时使用实际配置。WorkBuddy 优先读取当前宿主的 `WORKBUDDY_CONFIG_DIR`；未设置时使用默认值。表中的 `~` 表示当前用户主目录，Windows 使用对应用户目录。**WorkBuddy 与 CodeBuddy 是不同宿主，不能互用安装目标。**

## skills CLI 支持的 Agent

需要 Node.js 22.20 或更新版本。在目标项目目录执行，替换 `<agent-id>` 为上表中匹配的值：

```bash
npx --yes skills add 9Ashwin/monthly-salary-cat-illustrations --skill monthly-salary-cat-illustrations --agent <agent-id> --yes --copy
```

用户级安装在末尾加 `--global`。第一个 `--yes` 跳过 npm 包安装确认，第二个 `--yes` 跳过 skills 安装确认；`--agent` 明确安装对象。不要只加 `--yes` 却省略 Agent，也不要使用 `--all`：这可能装给其他助手。

裸 `npx skills add ...` 可能进入交互式 Agent 选择。自动执行时使用上面的完整参数，不要等待用户替你操作终端菜单。

## WorkBuddy 或 CLI 不支持的 Agent

已核对的 skills CLI 1.7.6 不包含 WorkBuddy 目标。遇到不支持的目标、没有 Node.js，或宿主使用自定义技能目录时，直接复制文件即可，无需安装其他工具链。

1. 用现有 Git 工具将上述仓库浅克隆到临时目录，或下载仓库源码 ZIP 后解压；已有用户指定的本地副本时可直接使用。不要把整个仓库放进技能目录。
2. 读取 `skills/monthly-salary-cat-illustrations/SKILL.md`，确认技能名称。将这个目录的完整内容复制到目标技能目录下的 `monthly-salary-cat-illustrations/`。
3. 保留 `assets/`、`references/`、`agents/`、`LICENSE` 和 `NOTICE.md`。已有同名技能需要更新时，先保留旧目录备份，再替换本技能；不改其他技能。

例如，WorkBuddy 安装后应包含：

```text
<WorkBuddy 配置目录>/skills/monthly-salary-cat-illustrations/
├── SKILL.md
├── LICENSE
├── NOTICE.md
├── agents/openai.yaml
├── references/
└── assets/
    ├── character-reference.webp
    └── examples/
```

WorkBuddy 也可以通过“添加技能 → 上传技能”导入本地 ZIP，见[官方技能文档](https://www.workbuddy.ai/docs/zh/workbuddy/From-Beginner-to-Expert-Guide/Function-Description/Skills)。打包时让 `SKILL.md` 位于 ZIP 根目录，保留其余相对目录。

## 核验并继续用户任务

- 从安装位置重新读取 `SKILL.md`，确认名称为 `monthly-salary-cat-illustrations`。
- 确认引用的参考文档、14 张示例及 `assets/character-reference.webp` 均可读取。原始 WebP 为 803066 字节，SHA-256 为 `fc9ee0b926710c8bb6bde6dd462ff5a2db8c67503a9c4994478084e387bb0d95`。
- 报告实际安装路径和核验结果。宿主需要刷新技能列表或新建对话时，说明该步骤；不要把文件复制成功说成宿主已识别或已验证生图。
- 用户同时要求画图时，读取安装后的技能并继续完成绘图。使用当前宿主已启用、支持参考图的图像能力，将内置角色图实际传入工具；没有这种能力时说明限制并提供提示词。
