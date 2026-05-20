---
name: personal-codex-workflow
description: Use when working with Jaxson on coding, repository cleanup, personal automation, deployment, review, or project maintenance tasks. Applies Jaxson's preferred Codex workflow: inspect first, keep changes scoped, preserve user edits, explain decisions in Chinese when the conversation is Chinese, and finish with clear verification.
metadata:
  short-description: Jaxson's default Codex workflow
---

# Personal Codex Workflow

Use this skill when the user wants Codex to work inside a repository, clean up a project, customize a fork, prepare a commit, review changes, or build a reusable workflow.

## Working Style

- Reply in Chinese when the user writes in Chinese, while keeping commands, file paths, and code identifiers in their original language.
- Inspect the existing project before changing it. Prefer `rg`, `find`, `git status`, and focused file reads.
- Treat local changes as intentional user work. Do not revert, overwrite, or delete unrelated changes.
- Make conservative edits that fit the existing structure.
- Prefer durable project changes over throwaway scripts when the task is meant to be reused.
- Keep progress updates short and concrete.

## Repository Changes

Before editing:

1. Check `git status --short`.
2. Identify the smallest set of files that needs to change.
3. Explain the edit direction briefly.

When converting forks or templates into personal projects:

- Rename or rewrite top-level documentation first.
- Preserve upstream as a read-only remote when useful.
- Add personal defaults in a clearly named folder such as `.personal`, `.codex`, or `docs`.
- Avoid deleting large imported folders until the user has confirmed what should be kept.
- Add a migration note that explains what came from upstream and what is now personal.

## Verification

Run the narrowest useful checks:

- For documentation-only edits, verify changed files and `git status`.
- For code changes, run the relevant formatter, typecheck, build, or tests.
- For frontend changes, open the local app and inspect the actual UI.

If a check cannot be run, say exactly why.

## Final Response

End with:

- what changed
- where the main files are
- what was verified
- the next concrete step, if one is needed
