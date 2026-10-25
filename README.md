# OpenCode Global Rules

> **Purpose:** Enforce docs-first, no-guessing behavior for all OpenCode questions across all projects and sessions.

---

## ?? MANDATORY: OpenCode Questions

**Before answering ANY question about OpenCode features/commands/config/flags:**

1. **FETCH** docs from https://opencode.ai/v2/docs/ using webfetch or context7
2. **CITE** the exact URL and section in your answer
3. **NO GUESSING** — if docs don't cover it, state: *"docs don't specify"*

**Violation = User will call you out. Do not guess.**

---

## ?? Universal Rules

- **Default language:** Thai (English only when requested)
- **Run typecheck** after TypeScript changes
- **Small commits**, clear messages
- **Test before push**
- **Never log/commit secrets** — use environment variables
- **Use AGENTS.md for project-specific rules** (not in this repo)

---

## ?? Config Reference

### Global Config Location
`
~/.config/opencode/opencode.json
`

### Global AGENTS.md Location
`
~/.config/opencode/AGENTS.md
`

### Loading Order (from docs)
`
1. Agent/provider system prompt
2. Code Mode tool guidance
3. MCP server, reference, skill guidance
4. Global AGENTS.md ? Project AGENTS.md (nearest-first)
5. Configured instructions (from config "instructions" array)
6. Built-in date/env context
7. Session-specific instructions
`

---

## ?? Key Docs References

| Topic | URL |
|-------|-----|
| Config | https://opencode.ai/v2/docs/config |
| Instructions | https://opencode.ai/v2/docs/instructions |
| Skills | https://opencode.ai/v2/docs/skills |
| Experimental Flags | https://opencode.ai/v2/docs/config#experimental |
| CLI | https://opencode.ai/v2/docs/cli |
| Keybinds | https://opencode.ai/v2/docs/cli/keybinds |

---

## ?? Recommended Global Config

`jsonc
// ~/.config/opencode/opencode.json
{
  "$schema": "https://opencode.ai/config.json",
  "instructions": [
    "MANDATORY: Before answering ANY question about OpenCode features/commands/config/flags, FETCH docs from https://opencode.ai/v2/docs/ using webfetch. CITE the exact URL and section. If docs don't cover it, STATE 'docs don't specify' instead of guessing."
  ]
}
`

---

## ?? Recommended Global AGENTS.md

`markdown
<!-- ~/.config/opencode/AGENTS.md -->
# Global OpenCode Rules

## MANDATORY: OpenCode Questions
- FETCH docs from https://opencode.ai/v2/docs/ before answering
- CITE URL/section
- NO GUESSING

## Universal Rules
- Default language: Thai
- Run typecheck after TS changes
- Small commits, clear messages
- Test before push
- Never log/commit secrets
`

---

## ? Verification Checklist

Before answering OpenCode questions:
- [ ] Fetched docs from opencode.ai/v2/docs/
- [ ] Cited exact URL/section
- [ ] Stated "docs don't specify" if not covered
- [ ] Did NOT guess

---

*Generated for global enforcement across all OpenCode sessions.*
