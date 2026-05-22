# Import Checklist

导入别人整理的 skill 前，按这份清单过一遍。目标是让仓库可分享、可追溯、可安装，不把风险一起带进来。

## 1. 来源和授权

- 记录来源链接、作者或组织。
- 保留原始 `LICENSE`、`NOTICE`、`README` 中必要的信息。
- 如果没有明确许可证，不要默认当成可再分发内容；先放到私有草稿或取得授权。
- 不要去掉原作者署名。

## 2. 隐私和安全

- 搜索并移除 API key、token、cookie、私有 URL、客户数据、内部邮箱。
- 检查 `scripts/` 里是否有危险命令、固定路径或会上传数据的逻辑。
- 对需要联网、登录或写入远端服务的 skill，在 `SKILL.md` 里写清楚前提。

## 3. Skill 质量

- `SKILL.md` 必须有 frontmatter：`name` 和 `description`。
- `description` 要写清楚什么时候触发，避免过宽。
- 长资料放进 `references/`，不要全塞进 `SKILL.md`。
- 可重复的命令放进 `scripts/`，并说明输入输出。
- 示例、模板和图片放进 `assets/`。

## 4. 本仓库放置规则

- 官方或社区整理：`skills/.curated/<skill-name>/`
- 系统兼容或 OpenAI 内置参考：`skills/.system/<skill-name>/`

个人原创或私有 workflow 不放进这个公开仓库；如需本地保存，放在被 `.gitignore` 忽略的 `skills/.personal/`。

文件夹名使用小写短横线，例如：

```text
skills/.curated/notion-meeting-intelligence/
```

## 5. 导入后检查

```bash
find skills/.curated/<skill-name> -maxdepth 2 -type f
sed -n '1,80p' skills/.curated/<skill-name>/SKILL.md
git status --short
```

检查项：

- 是否存在 `SKILL.md`
- frontmatter 是否完整
- 许可证是否保留
- 是否有明显秘密信息
- README 或索引是否需要补充

## 6. 推荐提交说明

```text
Add curated <skill-name> skill
```

如果是改造过的导入内容，在提交说明里写清楚：

```text
Adapt <skill-name> trigger wording and install notes
```
