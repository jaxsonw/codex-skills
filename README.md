# Jaxson's Codex Skills

这是一个面向 Codex 用户的 skills 体验仓库：把个人工作流、官方示例、社区整理的可复用 skill 放在一起，方便安装、试用和继续二次整理。

这个仓库适合两类人：

- 想快速体验 Codex skills 的用户。
- 想参考现成 skill 结构、再整理成自己工作流的创作者。

仓库最初参考了 [`openai/skills`](https://github.com/openai/skills)。导入的官方/社区 skill 会尽量保留原始许可证和说明；Jaxson 自己的默认工作流放在 `.personal` 里。

## Repository Layout

```text
skills/
├── .personal/   # My own skills and workflow rules
├── .curated/    # Imported official/community skills kept as references
└── .system/     # System skills from OpenAI, kept for compatibility and examples
```

## Quick Start

安装单个 skill：

```text
$skill-installer install https://github.com/jaxsonw/codex-skills/tree/main/skills/.curated/playwright
```

安装 Jaxson 的个人默认工作流：

```text
$skill-installer install https://github.com/jaxsonw/codex-skills/tree/main/skills/.personal/personal-codex-workflow
```

安装后重启 Codex，让新 skill 生效。

## Recommended First Skills

如果是第一次体验，建议从这些开始：

- `personal-codex-workflow`: Jaxson 的默认协作、代码修改、验收和中文回复偏好。
- `openai-docs`: 查询 OpenAI API 和模型文档时使用官方资料。
- `playwright`: 用真实浏览器检查本地网页、截图和调试 UI。
- `pdf`: 读取、生成和检查 PDF。
- `transcribe`: 转写音频/视频内容。
- `speech`: 生成语音、旁白或提示音频。
- `vercel-deploy`: 部署网站到 Vercel 预览环境。
- `gh-fix-ci`: 检查并修复 GitHub Actions CI 失败。

完整目录见 [`docs/SKILL_INDEX.md`](docs/SKILL_INDEX.md)。

## For User Groups

扫码加入「Codex 使用交流群 4」：

![Codex 使用交流群 4](docs/assets/codex-user-group-4-qr.jpg)

二维码 7 天内有效，有效期至 2026-05-29。过期后请重新获取最新二维码。

如果你是从用户群里看到这个仓库，先看 [`docs/USER_GROUP_GUIDE.md`](docs/USER_GROUP_GUIDE.md)。里面有：

- 推荐体验路径。
- 安装命令模板。
- 试用时可以直接复制的提示词。
- 遇到权限、API key、连接器问题时该怎么判断。

## Personal Skills

Personal skills live in [`skills/.personal`](skills/.personal/). Start there when adding a workflow that should follow your own taste, conventions, or project habits.

Current personal skills:

- `personal-codex-workflow`: default collaboration, code-change, review, and delivery preferences.

## Imported Skills

Imported skills live in [`skills/.curated`](skills/.curated/). They are organized as reference-quality skills for installation and adaptation.

Before importing someone else's skill, use [`docs/IMPORT_CHECKLIST.md`](docs/IMPORT_CHECKLIST.md) to check:

- license and attribution
- secrets or private data
- trigger clarity
- external service requirements
- install and smoke-test notes

## Installing From This Repo

Install a skill into Codex with `$skill-installer` by pointing it at a folder that contains `SKILL.md`:

```text
$skill-installer install https://github.com/jaxsonw/codex-skills/tree/main/skills/.curated/<skill-name>
```

## Creating New Skills

Use the existing system skill creator pattern:

```text
$skill-creator create a new skill for <workflow>
```

A skill should be narrow, practical, and repeatable. Put long reference material in `references/`, executable helpers in `scripts/`, and only keep the essential workflow in `SKILL.md`.

## Upstream

If you keep an upstream remote for official examples, use it only for reading or syncing reference material:

```bash
git remote -v
```

Push your own changes to `origin`:

```bash
git push -u origin main
```
