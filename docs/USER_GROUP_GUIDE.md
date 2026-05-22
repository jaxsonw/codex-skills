# Codex Skills User Group Guide

这份指南给第一次从用户群体验 Codex skills 的朋友使用。

## 加入群聊

扫码加入「Codex 使用交流群 4」：

![Codex 使用交流群 4](assets/codex-user-group-4-qr.jpg)

二维码 7 天内有效，有效期至 2026-05-29。过期后请重新获取最新二维码。

## 先装什么

建议先装 1-3 个，不要一次装太多。体验顺序：

1. `openai-docs`
2. `playwright`
3. `pdf`

安装命令示例：

```text
$skill-installer install https://github.com/jaxsonw/codex-skills/tree/main/skills/.curated/openai-docs
$skill-installer install https://github.com/jaxsonw/codex-skills/tree/main/skills/.curated/playwright
$skill-installer install https://github.com/jaxsonw/codex-skills/tree/main/skills/.curated/pdf
```

安装完成后重启 Codex。

## 可以怎么试

复制下面任意一句到 Codex：

```text
用 openai-docs 查一下现在做语音转文字应该用哪个 OpenAI API，并给我一个最小可运行示例。
```

```text
用 playwright 打开本地 localhost:3000，帮我检查首页有没有明显 UI 问题。
```

```text
用 pdf 帮我读取这个 PDF，并整理成结构化摘要。
```

## 体验时要知道的事

- 有些 skill 需要外部账号、API key、命令行工具或连接器权限。
- 安装 skill 不等于自动安装所有依赖；skill 会告诉 Codex 应该按什么流程做事。
- 如果 Codex 提示需要重启，重启后再试。
- 如果某个 skill 触发不稳定，可以在提示词里直接写 skill 名称。

## 推荐反馈格式

发到群里时可以这样反馈：

```text
体验的 skill：
我的任务：
成功的地方：
卡住的地方：
Codex 的报错或截图：
我希望它下次更自动处理：
```

## 适合继续整理的方向

- 高频工作流：部署、代码审查、写文档、处理 Excel/PDF。
- 行业工作流：财务、人事、教育、运营、科研。
- 团队规范：代码风格、PR 模板、验收标准、发布流程。
- 工具连接：GitHub、Gmail、Notion、Figma、Linear 等。
