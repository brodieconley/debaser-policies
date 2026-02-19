# Debaser Policy Git — CLAUDE.md

> Project shortcut: `debaser-policy`
> Last updated: 2026-02-18

---

## Project Overview

This project manages **Debaser's organizational policy documents** — version-controlling, editing, and potentially publishing formal policy documents for the Debaser organization.

**Core documents:**
- Conflict of Interest Policy
- Mandate and Vision
- Partnership Policy

**Source documents:** `.docx` files in `Original_Policy_Docs/`

**Likely goals:** Convert raw `.docx` policies into a versioned, distributable format — output format TBD.

---

## Current Status

| Area | Status |
|------|--------|
| Original policy docs | ✅ Loaded in `Original_Policy_Docs/` |
| CLAUDE.md / project scaffolding | ✅ Created 2026-02-18 |
| Git history | ❌ Not initialized |
| Output format (HTML/PDF/MD) | ❓ TBD |

---

## Key Files

```
Debaser_Policy_Git/
├── CLAUDE.md                          ← You are here
├── DEVLOG.md                          ← Session log + dev notes
├── Original_Policy_Docs/
│   ├── Debaser Conflict of Interest Policy.docx
│   ├── Debaser Mandate and Vision.docx
│   └── Debaser Partnership Policy.docx
└── .claude/
    └── skills/
        └── debaser-policy/
            └── skill.md               ← Project workflow skill
```

---

## Architecture Notes

- **Input format:** `.docx` (Microsoft Word)
- **Source of truth:** `Original_Policy_Docs/` — treat as read-only originals
- **No git history yet** — initialize git before making significant changes

---

## Workflow Conventions

1. Never overwrite files in `Original_Policy_Docs/` — copy before transforming
2. Keep processed/converted outputs in a separate directory (e.g., `output/` or `docs/`)
3. Log meaningful decisions and discoveries in `DEVLOG.md`
4. Update this file whenever architecture or status changes significantly
5. Update `.claude/skills/debaser-policy/skill.md` as new recurring workflows emerge

---

## Next Steps

- [ ] Clarify the goal: What is the end output format? (HTML, PDF, Markdown, hosted site?)
- [ ] Initialize git repository
- [ ] Extract / convert `.docx` files to working format
- [ ] Define folder structure for converted/processed docs
- [ ] Establish review/approval workflow for policy changes

---

## Open Questions

- Who is the audience? Internal team, external partners, or public?
- Are policy documents meant to be **editable via a UI** or just version-controlled flat files?
- Should policies be broken into sections/chapters or kept as monolithic documents?
