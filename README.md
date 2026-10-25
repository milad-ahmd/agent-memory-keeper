<div align="center">

# 🧠 agent-memory-keeper

**Persistent project memory (MEMORY.md) so your agent stops repeating the same mistakes. An Agent Skill for Claude Code, Cline, Cursor, Codex and other AI coding agents.**

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
What do you remember about this project?
```

The full workflow, rules and output format are in [`SKILL.md`](skills/agent-memory-keeper/SKILL.md).

## 🧩 More skills

See the full collection: **[milad-ahmd/agent-skills](https://github.com/milad-ahmd/agent-skills)**.

## 🤝 Contributing

Issues and PRs are welcome, especially real-world before/after examples.

## 📄 License

[MIT](LICENSE) © Milad Ahmadi

<div align="center">

**If this skill saved you time, a ⭐ helps others find it.**

</div>
