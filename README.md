# OpenCode: Global AGENTS.md vs Config `instructions`

> **à¸§à¸±à¸•à¸–à¸¸à¸›à¸£à¸°à¸ªà¸‡à¸„à¹Œ:** à¹€à¸›à¸£à¸µà¸¢à¸šà¹€à¸—à¸µà¸¢à¸šà¸Šà¸±à¸”à¹€à¸ˆà¸™à¹€à¸žà¸·à¹ˆà¸­à¸•à¸±à¸”à¸ªà¸´à¸™à¹ƒà¸ˆà¸§à¹ˆà¸²à¸ˆà¸°à¸§à¸²à¸‡à¸à¸Žà¹„à¸«à¸™à¹„à¸§à¹‰à¸—à¸µà¹ˆà¹„à¸«à¸™

---

## ðŸ“‹ Global AGENTS.md â€” à¹€à¸«à¸¡à¸²à¸°à¸à¸±à¸šà¸­à¸°à¹„à¸£

| à¸à¸£à¸“à¸µà¹ƒà¸Šà¹‰à¸‡à¸²à¸™ | à¸•à¸±à¸§à¸­à¸¢à¹ˆà¸²à¸‡ |
|------------|---------|
| à¸à¸Žà¸žà¸·à¹‰à¸™à¸à¸²à¸™à¸—à¸µà¹ˆà¸•à¹‰à¸­à¸‡à¸šà¸±à¸‡à¸„à¸±à¸šà¸—à¸¸à¸à¹‚à¸›à¸£à¹€à¸ˆà¸à¸•à¹Œ | "à¸”à¸¶à¸‡à¹€à¸­à¸à¸ªà¸²à¸£à¸à¹ˆà¸­à¸™à¸•à¸­à¸šà¸„à¸³à¸–à¸²à¸¡ OpenCode à¸—à¸¸à¸à¸„à¸£à¸±à¹‰à¸‡" |
| Code conventions à¸—à¸±à¹ˆà¸§à¹„à¸› | "à¸­à¸´à¸™à¹€à¸”à¸™à¸•à¹Œ 2 à¸Šà¹ˆà¸­à¸‡à¹€à¸§à¹‰à¸™, à¹„à¸¡à¹ˆà¹ƒà¸Šà¹‰ semicolon à¹ƒà¸™ JS/TS" |
| Workflow à¸šà¸±à¸‡à¸„à¸±à¸š | "à¸£à¸±à¸™à¹€à¸—à¸ªà¸•à¹Œà¸à¹ˆà¸­à¸™à¸„à¸­à¸¡à¸¡à¸´à¸•", "à¸£à¸±à¸™ typecheck à¸«à¸¥à¸±à¸‡à¹à¸à¹‰à¹‚à¸„à¹‰à¸”" |
| Architecture principles | "à¹€à¸à¹‡à¸š business logic à¹„à¸§à¹‰à¹ƒà¸™ domain layer, à¸­à¸¢à¹ˆà¸²à¹„à¸§à¹‰ controllers" |
| Security rules | "à¸­à¸¢à¹ˆà¸² commit secrets, à¹ƒà¸Šà¹‰ environment variables" |
| à¸ªà¸´à¹ˆà¸‡à¸—à¸µà¹ˆà¸­à¸¢à¸²à¸à¹ƒà¸«à¹‰ agent à¸ˆà¸³à¸•à¸¥à¸­à¸”à¸à¸²à¸¥ | "à¸œà¸¹à¹‰à¹ƒà¸Šà¹‰à¸•à¹‰à¸­à¸‡à¸à¸²à¸£à¸ à¸²à¸©à¸²à¹„à¸—à¸¢", "à¸œà¸¹à¹‰à¹ƒà¸Šà¹‰ Windows PowerShell" |

**à¸ˆà¸¸à¸”à¹€à¸”à¹ˆà¸™:** Hot reload (à¹à¸à¹‰à¹„à¸Ÿà¸¥à¹Œ â†’ à¹ƒà¸Šà¹‰à¹„à¸”à¹‰à¸—à¸±à¸™à¸—à¸µ), à¹‚à¸«à¸¥à¸”à¸à¹ˆà¸­à¸™à¸—à¸¸à¸à¸­à¸¢à¹ˆà¸²à¸‡, à¹ƒà¸Šà¹‰ Markdown à¸˜à¸£à¸£à¸¡à¸”à¸²

---

## âš™ï¸ `instructions` Array à¹ƒà¸™ Config â€” à¹€à¸«à¸¡à¸²à¸°à¸à¸±à¸šà¸­à¸°à¹„à¸£

| à¸à¸£à¸“à¸µà¹ƒà¸Šà¹‰à¸‡à¸²à¸™ | à¸•à¸±à¸§à¸­à¸¢à¹ˆà¸²à¸‡ |
|------------|---------|
| à¸­à¹‰à¸²à¸‡à¸­à¸´à¸‡à¹„à¸Ÿà¸¥à¹Œà¹€à¸‰à¸žà¸²à¸°à¹€à¸ˆà¸²à¸°à¸ˆà¸‡à¸«à¸¥à¸²à¸¢à¹„à¸Ÿà¸¥à¹Œ | "CONTRIBUTING.md", "docs/coding-standards.md", "docs/git-workflow.md" |
| à¹ƒà¸Šà¹‰ Glob pattern | "docs/guidelines/*.md", "**/RULES.md" |
| à¸”à¸¶à¸‡à¸ˆà¸²à¸ Remote URL | "https://company.com/opencode-rules.md", "https://api.internal/rules?team=backend" |
| Centralized rules à¸—à¸µà¹ˆ update à¹à¸šà¸š centralized | URL à¸Šà¸µà¹‰à¹„à¸› internal wiki â€” update à¸—à¸µà¹ˆà¸™à¸±à¹ˆà¸™à¸—à¸¸à¸à¸—à¸µà¹ˆà¹„à¸”à¹‰à¸£à¸±à¸šà¸­à¸±à¸›à¹€à¸”à¸• |
| Supplement à¹€à¸‰à¸žà¸²à¸°à¹‚à¸›à¸£à¹€à¸ˆà¸à¸•à¹Œà¸šà¸™ global rules | Global AGENTS.md à¸¡à¸µà¸à¸Žà¸—à¸±à¹ˆà¸§à¹„à¸› â†’ instructions à¹€à¸žà¸´à¹ˆà¸¡à¹‚à¸›à¸£à¹€à¸ˆà¸à¸•à¹Œà¹€à¸‰à¸žà¸²à¸° |
| à¸ªà¸´à¹ˆà¸‡à¸—à¸µà¹ˆà¸­à¸¢à¸²à¸ version control à¹à¸¢à¸à¸ˆà¸²à¸ AGENTS.md | Config file à¸­à¸¢à¸¹à¹ˆà¹ƒà¸™ git, AGENTS.md à¸­à¸¢à¸¹à¹ˆà¹ƒà¸™ global (à¹„à¸¡à¹ˆ commit) |

**à¸ˆà¸¸à¸”à¹€à¸”à¹ˆà¸™:** à¸£à¸­à¸‡à¸£à¸±à¸š URL/glob/multiple files, à¹‚à¸«à¸¥à¸”à¸«à¸¥à¸±à¸‡ AGENTS.md (override/extend à¹„à¸”à¹‰)

---

## ðŸ”§ à¸•à¸±à¸§à¸­à¸¢à¹ˆà¸²à¸‡à¸ˆà¸£à¸´à¸‡: à¹ƒà¸Šà¹‰à¸„à¸¹à¹ˆà¸à¸±à¸™à¹„à¸”à¹‰à¸­à¸¢à¹ˆà¸²à¸‡à¹„à¸£

### Global AGENTS.md (Foundation - à¸à¸Žà¸«à¸¥à¸±à¸)
```markdown
<!-- ~/.config/opencode/AGENTS.md -->

## Universal Rules
- **NO GUESSING** on OpenCode questions â†’ FETCH docs first
- CITE sources with URLs
- Default to Thai language
- Run typecheck after TS changes

## Security
- Never log/commit secrets
- Use env vars for API keys

## Workflow
- Small commits, clear messages
- Test before push
```

### Config `instructions` (Extensions - à¹€à¸žà¸´à¹ˆà¸¡à¹€à¸•à¸´à¸¡/à¹€à¸‰à¸žà¸²à¸°à¹€à¸ˆà¸²à¸°à¸ˆà¸‡)
```jsonc
// ~/.config/opencode/opencode.json
{
  "instructions": [
    "~/rules/team-conventions.md",           // Team-specific (local file)
    "https://wiki.company.com/opencode-rules", // Centralized (remote URL)
    "docs/architecture/*.md"                  // Project-specific (glob)
  ]
}
```

---

## ðŸŽ¯ Decision Matrix: à¹ƒà¸ªà¹ˆà¸­à¸°à¹„à¸£à¹„à¸«à¸™?

| à¹€à¸™à¸·à¹‰à¸­à¸«à¸² | à¹ƒà¸ªà¹ˆ AGENTS.md | à¹ƒà¸ªà¹ˆ instructions |
|----------|--------------|-----------------|
| "No guessing on OpenCode" | âœ… | âŒ |
| "Run `bun test` before commit" | âœ… | âŒ |
| Team coding standards (10 pages) | âŒ | âœ… (file/URL) |
| Architecture decision records | âŒ | âœ… (glob: `docs/adr/*.md`) |
| Centralized company rules (update à¸—à¸¸à¸à¸—à¸µà¹ˆ) | âŒ | âœ… (URL) |
| "User prefers Thai" | âœ… | âŒ |
| Project-specific build commands | âŒ | âœ… (relative path) |
| Security rules à¸—à¸¸à¸à¹‚à¸›à¸£à¹€à¸ˆà¸à¸•à¹Œ | âœ… | âŒ |

---

## ðŸ“– à¸à¸Žà¸ªà¸£à¸¸à¸›: AGENTS.md = "Always", instructions = "Additionally"

| à¸„à¸³à¸–à¸²à¸¡ | à¸„à¸³à¸•à¸­à¸š |
|--------|-------|
| à¸•à¹‰à¸­à¸‡à¸à¸²à¸£à¹ƒà¸«à¹‰ **à¸—à¸¸à¸ session à¸—à¸¸à¸à¹‚à¸›à¸£à¹€à¸ˆà¸à¸•à¹Œ** à¸ˆà¸³à¹„à¸”à¹‰? | **AGENTS.md** |
| à¸•à¹‰à¸­à¸‡à¸à¸²à¸£ **à¸«à¸¥à¸²à¸¢à¹„à¸Ÿà¸¥à¹Œ / URL / glob** à¸£à¸§à¸¡à¹€à¸‚à¹‰à¸²à¸”à¹‰à¸§à¸¢à¸à¸±à¸™? | **instructions** |
| à¸•à¹‰à¸­à¸‡à¸à¸²à¸£ **hot reload** (à¹à¸à¹‰à¹à¸¥à¹‰à¸§à¹ƒà¸Šà¹‰à¹„à¸”à¹‰à¹€à¸¥à¸¢)? | **AGENTS.md** |
| à¸•à¹‰à¸­à¸‡à¸à¸²à¸£ **override/extend** à¸à¸Žà¸ˆà¸²à¸ AGENTS.md? | **instructions** (à¹‚à¸«à¸¥à¸”à¸—à¸µà¸«à¸¥à¸±à¸‡) |
| à¹„à¸Ÿà¸¥à¹Œà¸­à¸¢à¸¹à¹ˆà¹ƒà¸™ **repo/version control**? | **instructions** (relative path) |
| à¹„à¸Ÿà¸¥à¹Œà¸­à¸¢à¸¹à¹ˆ **global/user-level**? | **AGENTS.md** |

---

## ðŸ“ à¸ªà¸£à¸¸à¸›à¹à¸šà¸šà¸ªà¸±à¹‰à¸™

```
AGENTS.md     â†’ "Constitution" (à¸à¸Žà¸«à¸¥à¸±à¸ à¸šà¸±à¸‡à¸„à¸±à¸šà¸—à¸¸à¸à¸—à¸µà¹ˆ à¹‚à¸«à¸¥à¸”à¸à¹ˆà¸­à¸™)
instructions  â†’ "Amendments"  (à¹€à¸žà¸´à¹ˆà¸¡à¹€à¸•à¸´à¸¡ à¸¢à¸·à¸”à¸«à¸¢à¸¸à¹ˆà¸™ à¹‚à¸«à¸¥à¸”à¸—à¸µà¸«à¸¥à¸±à¸‡)
```

**à¹à¸™à¸°à¸™à¸³:** à¹€à¸£à¸´à¹ˆà¸¡ `AGENTS.md` à¸à¹ˆà¸­à¸™ (foundation) â†’ à¹€à¸žà¸´à¹ˆà¸¡ `instructions` à¸•à¸­à¸™à¸•à¹‰à¸­à¸‡à¸à¸²à¸£ reference à¹„à¸Ÿà¸¥à¹Œ/URL à¹€à¸‰à¸žà¸²à¸°à¹€à¸ˆà¸²à¸°à¸ˆà¸‡

---

## ðŸ“š Key Docs References

| Topic | URL |
|-------|-----|
| Config | https://opencode.ai/v2/docs/config |
| Instructions | https://opencode.ai/v2/docs/instructions |
| Skills | https://opencode.ai/v2/docs/skills |
| Experimental Flags | https://opencode.ai/v2/docs/config#experimental |
| CLI | https://opencode.ai/v2/docs/cli |
| Keybinds | https://opencode.ai/v2/docs/cli/keybinds |