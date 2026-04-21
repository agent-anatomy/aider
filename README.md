# Aider — Starter Boilerplate

> Ready-to-use `.aider.conf.yml`, `.aiderignore`, and `CONVENTIONS.md` for your project. Clone, copy, edit.

Part of [agent-anatomy](https://github.com/agent-anatomy) — boilerplates for every AI coding agent.

📊 **[View diagram →](https://agent-anatomy.github.io/graphics/aider.html)**

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
.aider.conf.yml                    ← aider configuration (model, flags, conventions file)
.aiderignore                       ← files aider should never read or modify
CONVENTIONS.md                     ← coding conventions aider reads before every session
```

---

## What is .aider.conf.yml?

The main configuration file for Aider. Controls which model to use, auto-commit behavior, linting, testing, and which conventions file to load.

```yaml
model: gpt-4o
auto-commits: true
read: CONVENTIONS.md
lint-cmd: "npm run lint"
test-cmd: "npm test"
```

---

## What is CONVENTIONS.md?

A plain text file Aider reads before every session via the `read:` key in `.aider.conf.yml`. Use it to define coding style, naming conventions, test patterns — anything you'd tell a new engineer on day one.

Different from `.aiderignore` — `CONVENTIONS.md` tells Aider *how* to write code, not *what* to avoid touching.

---

## What is .aiderignore?

Works like `.gitignore` but for Aider. Files listed here are invisible to Aider — it won't read, suggest changes to, or modify them.

Use for: generated files, large data files, secrets, lock files, build output.

---

## What to commit vs gitignore

| File | Commit? |
|------|---------|
| `.aider.conf.yml` | ✅ Yes |
| `.aiderignore` | ✅ Yes |
| `CONVENTIONS.md` | ✅ Yes |
| `.aider.chat.history.md` | ❌ No — personal chat log |
| `.aider.tags.cache.v3/` | ❌ No — local cache |

Add to your `.gitignore`:
```
.aider.chat.history.md
.aider.tags.cache.v3/
```

---

## FAQ

**Does Aider read CONVENTIONS.md automatically?**
Only if you add `read: CONVENTIONS.md` to `.aider.conf.yml`. It doesn't load automatically by filename alone.

**What model should I use in .aider.conf.yml?**
`gpt-4o` or `claude-opus-4-7` for best results. Aider supports most frontier models.

**Should I commit .aider.conf.yml?**
Yes — it configures project-level behavior. The whole team benefits from shared lint/test commands and conventions.

**What's the difference between .aiderignore and .gitignore?**
`.gitignore` tells git what to exclude. `.aiderignore` tells Aider what to ignore — they're independent. A file can be committed to git but ignored by Aider.

---

## Other agents

| Agent | Boilerplate |
|-------|-------------|
| Claude Code | [agent-anatomy/claude](https://github.com/agent-anatomy/claude) |
| Cursor | [agent-anatomy/cursor](https://github.com/agent-anatomy/cursor) |
| OpenAI Codex | [agent-anatomy/codex](https://github.com/agent-anatomy/codex) |
| Windsurf | [agent-anatomy/windsurf](https://github.com/agent-anatomy/windsurf) |
| GitHub Copilot | [agent-anatomy/copilot](https://github.com/agent-anatomy/copilot) |
| Gemini CLI | [agent-anatomy/gemini](https://github.com/agent-anatomy/gemini) |
