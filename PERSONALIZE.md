# Migration Notes

This repository has been converted from the upstream OpenAI skills catalog into Jaxson's personal Codex skills catalog.

## What Changed

- `origin` was renamed to `upstream` so the OpenAI repository is read-only by convention.
- The root `README.md` now describes this as a personal skills catalog.
- Personal skills now live under `skills/.personal`.
- A starter personal workflow skill was added at `skills/.personal/personal-codex-workflow`.
- `contributing.md` now describes local maintenance rules instead of OpenAI contribution guidance.

## What Was Preserved

- `skills/.system`: preserved for compatibility and examples.
- `skills/.curated`: preserved as imported official/community skill references.
- Per-skill license files: preserved in place.

## Next Steps

1. Create a new GitHub repository for this catalog.
2. Add it as `origin`.
3. Push `main`.
4. Install personal skills into Codex with `$skill-installer`.

Example:

```bash
git remote add origin <your-git-url>
git push -u origin main
```

To keep syncing official examples later:

```bash
git fetch upstream
```
