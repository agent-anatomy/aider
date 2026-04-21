# Aider — Starter Boilerplate

> Ready-to-use `.aider.conf.yml`, `.aiderignore`, and `CONVENTIONS.md` for your project. Clone, copy, edit.

Part of [agent-anatomy](https://github.com/agent-anatomy) — boilerplates for every AI coding agent.

---

## Usage

```bash
git clone https://github.com/agent-anatomy/aider.git .aider-boilerplate

cp .aider-boilerplate/.aider.conf.yml ./.aider.conf.yml
cp .aider-boilerplate/.aiderignore ./.aiderignore
cp .aider-boilerplate/CONVENTIONS.md ./CONVENTIONS.md

rm -rf .aider-boilerplate
```

Then edit the files to match your project.

---

## What's included

```
.aider.conf.yml                    ← aider configuration
.aiderignore                       ← files aider should not touch
CONVENTIONS.md                     ← coding conventions aider reads
```

---

## What to commit vs gitignore

| File | Commit? |
|------|---------|
| `.aider.conf.yml` | ✅ Yes |
| `.aiderignore` | ✅ Yes |
| `CONVENTIONS.md` | ✅ Yes |
| `.aider.chat.history.md` | ❌ No — personal |
| `.aider.tags.cache.v3/` | ❌ No — local cache |

Add to your `.gitignore`:
```
.aider.chat.history.md
.aider.tags.cache.v3/
```

---

## Other agents

| Agent | Boilerplate |
|-------|-------------|
| Claude Code | [agent-anatomy/claude](https://github.com/agent-anatomy/claude) |
| Cursor | [agent-anatomy/cursor](https://github.com/agent-anatomy/cursor) |
| OpenAI Codex | [agent-anatomy/codex](https://github.com/agent-anatomy/codex) |
| More... | [agent-anatomy](https://github.com/agent-anatomy) |
