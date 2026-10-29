> [!NOTE]
> **This skill lives in the main collection: [milad-ahmd/agent-skills](https://github.com/milad-ahmd/agent-skills/tree/main/skills/agent-memory-keeper)**. Please ⭐ star it there; that's where updates land first.
> Docs: **https://milad-ahmd.github.io/agent-skills/skills/agent-memory-keeper/** · Claude Code: `/plugin install all-skills --marketplace milad-ahmd/agent-skills`

<div align="center">

# 🧠 agent-memory-keeper

**Project memory (MEMORY.md) plus session handoffs (HANDOFF.md) so the next session picks up where this one stopped. An Agent Skill for Claude Code, Cline, Cursor, Codex and other AI coding agents.**

[![License: MIT](https://img.shields.io/github/license/milad-ahmd/agent-memory-keeper)](LICENSE)
[![Stars](https://img.shields.io/github/stars/milad-ahmd/agent-memory-keeper?style=social)](https://github.com/milad-ahmd/agent-memory-keeper)
![Category](https://img.shields.io/badge/category-Agent%20Productivity-blue)
![Works with](https://img.shields.io/badge/works%20with-Claude%20Code%20%7C%20Cline%20%7C%20Cursor%20%7C%20Codex-8A2BE2)

[Install](#-install) · [Usage](#-usage) · [How it works](skills/agent-memory-keeper/SKILL.md) · [All skills](https://github.com/milad-ahmd/agent-skills)

</div>

> Part of **[agent-skills](https://github.com/milad-ahmd/agent-skills)**, a growing collection of practical skills for AI coding agents.

## 📦 Install

**One command (installs the whole collection):**

```bash
curl -fsSL https://raw.githubusercontent.com/milad-ahmd/agent-skills/main/install.sh | bash -s -- agent-memory-keeper
```

**Manually (Claude Code):**

```bash
git clone https://github.com/milad-ahmd/agent-memory-keeper /tmp/agent-memory-keeper
mkdir -p ~/.claude/skills && cp -r /tmp/agent-memory-keeper/skills/agent-memory-keeper ~/.claude/skills/
```

**Per project:** copy `skills/agent-memory-keeper` into `<project>/.claude/skills/`.
**Any other agent:** paste [`SKILL.md`](skills/agent-memory-keeper/SKILL.md) into your rules or system prompt.

## 💬 Usage

Just ask your agent:

```text
Remember that we use pnpm, not npm
Write a handoff, I'm running out of context
```

The full workflow, rules and output format are in [`SKILL.md`](skills/agent-memory-keeper/SKILL.md).

## 🔎 Sample output

`handoff.py` is plain Python 3 with no dependencies and never touches your working tree. Real output halfway through a bug fix:

```text
$ python3 handoff.py

Handoff facts for ~/code/shop

- Repo: shop
- Branch: fix/discount-rounding
- HEAD: aa578d8 test: failing case for per-line discount rounding
- Upstream: none
- Base: main (merge-base f496d7e; 1 commits on this branch, 1 files changed)
- In progress: none
- Stash: 0
- Uncommitted: 1 (0 staged, 1 unstaged, 0 untracked, 0 conflicted)
  - .M cart.py

Commits on this branch (newest first):
- aa578d8 test: failing case for per-line discount rounding

Files changed on this branch:
- A test_discount.py

TODO/FIXME/XXX added:
- cart.py:2 (uncommitted) # TODO: confirm with finance whether coupons round per line or per order

MEMORY.md: none · HANDOFF.md: none
```

`--write HANDOFF.md` turns these facts into a skeleton for the agent to fill in, and `--check HANDOFF.md` at the start of the next session reports if the repo no longer matches.

## 🧩 More skills

See the full collection: **[milad-ahmd/agent-skills](https://github.com/milad-ahmd/agent-skills)**.

## 🤝 Contributing

This repo is a read-only mirror. Please open issues and PRs in **[milad-ahmd/agent-skills](https://github.com/milad-ahmd/agent-skills)**.

## 📄 License

[MIT](LICENSE) © Milad Ahmadi

<div align="center">

**If this skill saved you time, a ⭐ helps others find it.**

</div>
