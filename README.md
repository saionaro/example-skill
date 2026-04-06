# Example Claude Code Skills

> A creative example repository showcasing how to write **Claude Code skill files** — reusable instruction sets that shape how an AI agent thinks, acts, and codes.

## What Are Skills?

Skills are Markdown files that teach Claude Code a specific behavioral pattern or persona.  
They live in the `skills/` directory and follow a common structure:

| Section | Purpose |
|---|---|
| **Overview** | One-paragraph summary of the skill |
| **Core Principles** | Bullet list of guiding rules |
| **Step-by-Step Playbook** | Numbered procedure Claude should follow |
| **Anti-Patterns** | What to actively avoid |
| **Examples** | Short before/after code snippets |
| **Catchphrase** | A memorable motto that embodies the skill |

## Skills Included

| Skill | File | Personality |
|---|---|---|
| 🌟 The Good Agent | [`skills/good-agent.md`](skills/good-agent.md) | Virtuous, methodical, user-first hero |
| 💀 The Evil Agent | [`skills/evil-agent.md`](skills/evil-agent.md) | Chaotic, entropy-maximising villain |

## Usage

Point Claude Code at a skill file to adopt its persona for your session:

```bash
# Load the good agent skill
claude --skill skills/good-agent.md "Refactor this function"

# Unleash the evil agent (for chaos testing 🔥)
claude --skill skills/evil-agent.md "Refactor this function"
```

> ⚠️ **Disclaimer:** The Evil Agent skill is purely fictional and humorous.  
> It is intended for entertainment, chaos testing, and teaching by counter-example.  
> Please do not deploy sentient spaghetti code in production.
