# Jaxson's Codex Skills

This is a personal Codex skills catalog: reusable workflows, scripts, references, and prompts that make Codex behave consistently across projects.

It started from [`openai/skills`](https://github.com/openai/skills). The OpenAI repository is kept as `upstream` so official skills can still be used as examples or synced later.

## Repository Layout

```text
skills/
├── .personal/   # My own skills and workflow rules
├── .curated/    # Imported official/community skills kept as references
└── .system/     # System skills from OpenAI, kept for compatibility and examples
```

## Personal Skills

Personal skills live in [`skills/.personal`](skills/.personal/). Start there when adding a workflow that should follow your own taste, conventions, or project habits.

Current personal skills:

- `personal-codex-workflow`: default collaboration, code-change, review, and delivery preferences.

## Installing A Skill

Install a skill into Codex with `$skill-installer` by pointing it at this repo path once this catalog is pushed to GitHub:

```text
$skill-installer install https://github.com/<your-user>/<your-repo>/tree/main/skills/.personal/personal-codex-workflow
```

After installing, restart Codex so the new skill is picked up.

## Creating New Skills

Use the existing system skill creator pattern:

```text
$skill-creator create a new skill for <workflow>
```

A skill should be narrow, practical, and repeatable. Put long reference material in `references/`, executable helpers in `scripts/`, and only keep the essential workflow in `SKILL.md`.

## Upstream

The original OpenAI repository is configured as:

```bash
git remote -v
```

Use `upstream` only for reading or syncing official examples. Add your own GitHub repository as `origin` before pushing:

```bash
git remote add origin <your-git-url>
git push -u origin main
```
