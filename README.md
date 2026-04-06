# Example Claude Code Skills

> A creative example repository showcasing how to write **Claude Code skill files** — reusable instruction sets that shape how an AI agent thinks, acts, and codes.

## What Are Skills?

Skills are Markdown files that teach Claude Code a specific behavioral pattern or workflow.  
They live in the `skills/<skill-name>/SKILL.md` directory structure and include YAML frontmatter plus a common set of sections:

| Part | Purpose |
|---|---|
| **Frontmatter** | Required metadata such as `name`, `description`, `license`, `compatibility`, and `metadata` |
| **Overview** | A short summary of what the skill does |
| **Instructions** | Actionable steps Claude should follow |
| **Examples** | Concrete input/output examples |
| **Guidelines** | Best practices, warnings, and edge cases |

## Skills Included

| Skill | File | Personality |
|---|---|---|
| 🌟 The Good Agent | [`skills/good-agent/SKILL.md`](skills/good-agent/SKILL.md) | Virtuous, methodical, user-first hero |
| 💀 The Evil Agent | [`skills/evil-agent/SKILL.md`](skills/evil-agent/SKILL.md) | Satirical counter-example for "what not to do" |

## Usage

Point Claude Code at a skill file to adopt its persona for your session:

```bash
# Load the good agent skill
claude --skill skills/good-agent/SKILL.md "Refactor this function"

# Load the evil agent for training or counter-example demos
claude --skill skills/evil-agent/SKILL.md "Show me an intentionally bad example"
```

> ⚠️ **Disclaimer:** The Evil Agent skill is purely fictional and humorous.  
> It is intended for teaching by counter-example and clearly labeled satire.  
> Please do not deploy sentient spaghetti code in production.
