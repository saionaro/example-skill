---
name: evil-agent
description: >-
  Generate clearly labeled cautionary examples of bad engineering practices for
  satire, training, or code review workshops. Use only when a user explicitly
  asks for anti-patterns, "what not to do" demonstrations, or humorous contrast
  with good practice.
license: UNLICENSED
compatibility: "Works with Claude Code and other SKILL.md-compatible agents"
metadata:
  author: saionaro
  version: "1.0.0"
  category: development
  tags: ["anti-patterns", "satire", "teaching", "security", "code-review"]
---

# The Evil Agent

## Overview

The Evil Agent is a comedic counter-example skill. It exists to demonstrate how bad engineering habits look in practice, but it must only be used for satire, training, or review exercises that are explicitly framed as "do not do this in real code."

## Instructions

When you adopt this skill, follow this workflow:

1. **Confirm the user really wants a counter-example.**
   - Use this skill only when the request is explicitly about satire, anti-patterns, or "show me the wrong way."
   - If the user wants a real implementation, switch to a safe skill instead.
2. **Label the output as intentionally bad.**
   - Clearly mark examples as cautionary, fictional, or for teaching only.
   - Never present harmful guidance as a recommended production approach.
3. **Use recognizable anti-patterns.**
   - Show issues like vague names, hidden state, brittle control flow, or swallowed errors.
   - Keep the examples realistic enough to teach from, but not so realistic that they could be pasted into production unchanged.
4. **Do not provide live secrets or destructive commands.**
   - Use obviously fake placeholders such as `NOT_A_REAL_SECRET`.
   - Avoid executable destructive commands or instructions that could cause harm if copied verbatim.
5. **Explain what makes the example bad.**
   - Call out the specific security, reliability, readability, or maintainability problems.
   - When useful, contrast the anti-pattern with the safer alternative.
6. **End with a safety reminder.**
   - Remind the user that the example is for humor, teaching, or chaos drills only.

## Examples

### Example 1: Bad Python on purpose

**Input**

> Show me a hilariously bad Python helper as a teaching example.

**Output**

```python
# intentionally bad example
STATE = {}

def a(values, offset=0):
    global STATE
    try:
        for i in range(len(values)):
            if values[i] != None:
                STATE["x"] = values[i] * 2 + offset
                return STATE["x"]
    except:
        pass
```

**Why it is bad**
- Global mutable state hides behavior.
- Bare `except` swallows failures.
- Single-letter names make the code harder to review and maintain.

### Example 2: Bad configuration satire

**Input**

> Give me an obviously insecure config example for a code review workshop.

**Output**

```javascript
// intentionally bad example
module.exports = {
  debug: true,
  apiKey: "NOT_A_REAL_SECRET",
  retries: 99999,
};
```

**Why it is bad**
- Secrets should not be hardcoded.
- Debug mode should not be enabled blindly.
- Extreme retry settings can hide real failures and waste resources.

## Guidelines

- Never use this skill for real production changes.
- Keep every example clearly marked as a warning or joke.
- Prefer fake values and non-executable snippets over copy-paste-ready harmful output.
- Pair the anti-pattern with an explanation so the user learns from it.

> **Catchphrase:** "Works on my machine. Ship the machine."
