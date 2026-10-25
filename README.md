# OpenCode: Global AGENTS.md vs Config \instructions\

> **Purpose:** Clear comparison to decide where to put your rules.

---

## 📋 Global AGENTS.md — เหมาะกับอะไร

| กรณีใช้งาน | ตัวอย่าง |
|------------|---------|
| กฎพื้นฐานที่ต้องบังคับทุกโปรเจกต์ | \"Always fetch docs before answering OpenCode questions\" |
| Code conventions ทั่วไป | \"Use 2 spaces indent, no semicolons in JS/TS\" |
| Workflow บังคับ | \"Run tests before commit\", \"Run typecheck after changes\" |
| Architecture principles | \"Keep business logic in domain layer, not controllers\" |
| Security rules | \"Never commit secrets, use env vars\" |
| สิ่งที่อยากให้ agent จำตลอดกาล | \"User prefers Thai responses\", \"User uses Windows PowerShell\" |

**จุดเด่น:** Hot reload (แก้ไฟล์ → ใช้ได้ทันที), โหลดก่อนทุกอย่าง, ใช้ Markdown ธรรมดา

---

## ⚙️ \instructions\ Array ใน Config — เหมาะกับอะไร

| กรณีใช้งาน | ตัวอย่าง |
|------------|---------|
| อ้างอิงไฟล์เฉพาะเจาะจงหลายไฟล์ | \\"CONTRIBUTING.md\", \"docs/coding-standards.md\", \"docs/git-workflow.md\"\ |
| ใช้ Glob pattern | \\"docs/guidelines/*.md\", \"**/RULES.md\"\ |
| ดึงจาก Remote URL | \\"https://company.com/opencode-rules.md\", \"https://api.internal/rules?team=backend\"\ |
| Centralized rules ที่ update แบบ centralized | URL ชี้ไป internal wiki — update ที่นั่นทุกที่ได้รับอัปเดต |
| Supplement เฉพาะโปรเจกต์บน global rules | Global AGENTS.md มีกฎทั่วไป → instructions เพิ่มโปรเจกต์เฉพาะ |
| สิ่งที่อยาก version control แยกจาก AGENTS.md | Config file อยู่ใน git, AGENTS.md อยู่ใน global (ไม่ commit) |

**จุดเด่น:** รองรับ URL/glob/multiple files, โหลดหลัง AGENTS.md (override/extend ได้)

---

## 🔧 ตัวอย่างจริง: ใช้คู่กันได้อย่างไร

### Global AGENTS.md (Foundation - กฎหลัก)
\\\markdown
<!-- ~/.config/opencode/AGENTS.md -->

## Universal Rules
- **NO GUESSING** on OpenCode questions → FETCH docs first
- CITE sources with URLs
- Default to Thai language
- Run typecheck after TS changes

## Security
- Never log/commit secrets
- Use env vars for API keys

## Workflow
- Small commits, clear messages
- Test before push
\\\

### Config \instructions\ (Extensions - เพิ่มเติม/เฉพาะเจาะจง)
\\\jsonc
// ~/.config/opencode/opencode.json
{
  \"instructions\": [
    \"~/rules/team-conventions.md\",           // Team-specific (local file)
    \"https://wiki.company.com/opencode-rules\", // Centralized (remote URL)
    \"docs/architecture/*.md\"                  // Project-specific (glob)
  ]
}
\\\

---

## 🎯 Decision Matrix: ใส่อะไรไหน?

| เนื้อหา | ใส่ AGENTS.md | ใส่ instructions |
|----------|--------------|-----------------|
| \"No guessing on OpenCode\" | ✅ | ❌ |
| \"Run \un test\ before commit\" | ✅ | ❌ |
| Team coding standards (10 pages) | ❌ | ✅ (file/URL) |
| Architecture decision records | ❌ | ✅ (glob: \docs/adr/*.md\) |
| Centralized company rules (update ทุกที่) | ❌ | ✅ (URL) |
| \"User prefers Thai\" | ✅ | ❌ |
| Project-specific build commands | ❌ | ✅ (relative path) |
| Security rules ทุกโปรเจกต์ | ✅ | ❌ |

---

## 📖 กฎสรุป: AGENTS.md = \"Always\", instructions = \"Additionally\"

| คำถาม | คำตอบ |
|--------|-------|
| ต้องการให้ **ทุก session ทุกโปรเจกต์** จำได้? | **AGENTS.md** |
| ต้องการ **หลายไฟล์ / URL / glob** รวมเข้าด้วยกัน? | **instructions** |
| ต้องการ **hot reload** (แก้แล้วใช้ได้เลย)? | **AGENTS.md** |
| ต้องการ **override/extend** กฎจาก AGENTS.md? | **instructions** (โหลดทีหลัง) |
| ไฟล์อยู่ใน **repo/version control**? | **instructions** (relative path) |
| ไฟล์อยู่ **global/user-level**? | **AGENTS.md** |

---

## 📝 สรุปแบบสั้น

\\\
AGENTS.md     → \"Constitution\" (กฎหลัก บังคับทุกที่ โหลดก่อน)
instructions  → \"Amendments\"  (เพิ่มเติม ยืดหยุ่น โหลดทีหลัง)
\\\

**แนะนำ:** เริ่ม \AGENTS.md\ ก่อน (foundation) → เพิ่ม \instructions\ ตอนต้องการ reference ไฟล์/URL เฉพาะเจาะจง

---

## 📚 Key Docs References

| Topic | URL |
|-------|-----|
| Config | https://opencode.ai/v2/docs/config |
| Instructions | https://opencode.ai/v2/docs/instructions |
| Skills | https://opencode.ai/v2/docs/skills |
| Experimental Flags | https://opencode.ai/v2/docs/config#experimental |
| CLI | https://opencode.ai/v2/docs/cli |
| Keybinds | https://opencode.ai/v2/docs/cli/keybinds |
