# Debaser Policy Repository — Full Spec

> Status: FINAL — approved for implementation
> Written: 2026-02-18
> Working dir: /Users/brodieconley/Claude/RANDOM/Debaser_Policy_Git/

---

## Context

Debaser (debaser.ca) is an Ottawa-based music presenter and arts not-for-profit. They have developed three organizational policies and want to share them publicly as open resources — free for other organizations (especially small arts and music nonprofits) to fork, adapt, and reuse under Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0).

**Source documents** in `Original_Policy_Docs/` (treat as read-only):
| Document | Original Effective Date | Corrected Date |
|----------|------------------------|----------------|
| Mandate and Vision | 2026-02-20 *(error)* | **2026-01-20** |
| Conflict of Interest Policy | 2025-03-31 | 2025-03-31 |
| Partnership Policy | 2025-03-31 | 2025-03-31 |

---

## Decisions Log

All decisions made during requirements interview on 2026-02-18:

| Decision | Choice | Notes |
|----------|--------|-------|
| GitHub home | Personal account | github.com/brodieconley/debaser-policies |
| Repo name | `debaser-policies` | |
| Sensitive content | Publish as-is | PACBI reference stays; Debaser stands behind all language |
| M&V effective date | Corrected to 2026-01-20 | Original had a typo |
| Other content corrections | None | Everything else is final as-written |
| Attribution format | Credit + link | "Adapted from Debaser (debaser.ca) under CC BY-SA 4.0" |
| PDF style | Debaser-branded | Logo + brand colors; logo file to be dropped in project folder |
| PDF generation | Manual, no GitHub Actions | Whoever updates markdown regenerates PDF and commits both |
| .docx files in repo | No | Markdown is the source of truth; originals stay local only |
| Community interaction | Issues + PRs welcome | Debaser reviews and merges |
| Branch protection | Yes | All changes to main go through PR, including Debaser's own |
| Versioning | Replace in place | Git history serves as archive of old versions |
| French versions | English only for now | May revisit |
| README voice | Warm, first-person | "We are Debaser…"; brief on org, quickly pivot to repo purpose |
| GitHub topics | policy, open-source, nonprofit | |
| Repo description | "Open-source policy documents from Debaser — free to fork, adapt, and reuse under CC BY-SA 4.0" | |
| Newsletter link | Use Mailchimp URL directly | Brodie accepts the risk of link staleness |
| CONTRIBUTING.md | Beginner-friendly fork instructions + adapter's checklist | Audience: small arts nonprofits, many GitHub newcomers |

---

## Repository Design

**GitHub URL:** https://github.com/brodieconley/debaser-policies

**Repo settings:**
- Visibility: Public
- Description: "Open-source policy documents from Debaser — free to fork, adapt, and reuse under CC BY-SA 4.0"
- Website: https://debaser.ca
- Topics: `policy`, `open-source`, `nonprofit`
- Branch protection on `main`: require pull request review before merging

**Final file structure:**
```
debaser-policies/
├── README.md
├── LICENSE
├── CONTRIBUTING.md
├── policies/
│   ├── mandate-and-vision.md
│   ├── conflict-of-interest-policy.md
│   └── partnership-policy.md
└── pdfs/
    ├── mandate-and-vision.pdf
    ├── conflict-of-interest-policy.pdf
    └── partnership-policy.pdf
```

---

## Contact & Identity

For use in README:
- **Website:** https://debaser.ca
- **Email:** hello@debaser.ca
- **Instagram:** @debaser__ (https://instagram.com/debaser__)
- **Newsletter:** https://debaser.us20.list-manage.com/subscribe?u=3bf41d84668569408308c15be&id=cc5d7069a8

**Logo:** `Debaser Logo.png` — present in project folder.

---

## Content Notes

### README.md
- Tone: warm, first-person ("We are Debaser…"), focused on the repo's purpose
- Brief Debaser description, then quickly pivot to: what's here, why we're sharing it, how to use it
- Include: document index with quick links, adapter's checklist intro, license statement, contact block
- Do NOT over-explain Debaser's history or achievements

### CONTRIBUTING.md
Must include:
1. **Beginner GitHub walkthrough**: Step-by-step "How to fork and adapt" written for someone who has never used GitHub — plain English, no assumed knowledge
2. **Adapter's Checklist**: Specific list of what to change when adapting these policies:
   - Find and replace "Debaser" with your organization's name throughout all documents
   - Update all `Effective Date:` fields to your board adoption date
   - Adjust "Board Chair" and "Vice-Chair" references to match your governance model (e.g., Executive Director, Steering Committee)
   - Review the Conflict of Interest Policy definitions — do "Members" and "participants" match how your org defines participants?
   - Partnership Policy — PACBI clause: decide if this applies to your org's values. Keep, remove, or replace with your own ethical partnership criteria
   - Review for any jurisdiction-specific language and adapt for your province/region/country
   - Replace any Debaser contact references with your own
   - Mandate and Vision: rewrite your 8-year vision to reflect your organization's goals and context
3. **PR contribution norms**: What makes a good PR, who reviews it, what Debaser is looking for

### LICENSE
- Full CC BY-SA 4.0 legal text, copied verbatim from Creative Commons
- GitHub should auto-detect and display the license type in the sidebar

### Policy Markdown Files
- Convert using pandoc from .docx originals
- Correct M&V effective date from 2026-02-20 → 2026-01-20 during conversion
- Preserve all section structure, numbering, definitions, and appendices/forms
- Publish all content as-is — no political or content edits

### PDF Files
- Generated using pandoc from the markdown files
- Branded: include Debaser logo in header or cover
- Use colors sourced from debaser.ca if no brand spec provided alongside logo
- Plain, readable layout — this is a functional document, not a design showcase
- Manually committed alongside the markdown files

---

## Implementation Steps

### PRE-STEP: Await logo file
**Status:** COMPLETE — `Debaser Logo.png` is present in the project folder.

---

### Step 1: Create project plan file ✅
**Action:** Write this spec as `PLAN.md` in the project folder.

---

### Step 2: Initialize git repository
**Action:**
```bash
cd /Users/brodieconley/Claude/RANDOM/Debaser_Policy_Git
git init
echo ".DS_Store" > .gitignore
echo "firebase-debug.log" >> .gitignore
```

---

### Step 3: Convert .docx → Markdown
**Action:** Run pandoc on each source file. Write output to `policies/`:
```bash
pandoc "Original_Policy_Docs/Debaser Mandate and Vision.docx" -o "policies/mandate-and-vision.md"
pandoc "Original_Policy_Docs/Debaser Conflict of Interest Policy.docx" -o "policies/conflict-of-interest-policy.md"
pandoc "Original_Policy_Docs/Debaser Partnership Policy.docx" -o "policies/partnership-policy.md"
```
- After conversion: correct M&V effective date from `2026-02-20` to `2026-01-20`
- Review each file for pandoc conversion artifacts

---

### Step 4: Write README.md

---

### Step 5: Write LICENSE

---

### Step 6: Write CONTRIBUTING.md

---

### Step 7: Generate PDFs
**PDF regeneration command (for future reference):**
```bash
# From repo root, after updating a markdown file:
pandoc policies/mandate-and-vision.md \
  --pdf-engine=xelatex \
  -V geometry:margin=1in \
  --include-in-header=pdf-header.tex \
  -o pdfs/mandate-and-vision.pdf

pandoc policies/conflict-of-interest-policy.md \
  --pdf-engine=xelatex \
  -V geometry:margin=1in \
  --include-in-header=pdf-header.tex \
  -o pdfs/conflict-of-interest-policy.pdf

pandoc policies/partnership-policy.md \
  --pdf-engine=xelatex \
  -V geometry:margin=1in \
  --include-in-header=pdf-header.tex \
  -o pdfs/partnership-policy.pdf
```

---

### Step 8: Initial git commit
```bash
git add PLAN.md README.md LICENSE CONTRIBUTING.md policies/ pdfs/ .gitignore
git commit -m "Initial commit: Debaser policy documents, README, LICENSE, CONTRIBUTING"
```

---

### Step 9: Create GitHub repo & push
```bash
gh repo create brodieconley/debaser-policies \
  --public \
  --description "Open-source policy documents from Debaser — free to fork, adapt, and reuse under CC BY-SA 4.0" \
  --homepage "https://debaser.ca"

git remote add origin https://github.com/brodieconley/debaser-policies.git
git branch -M main
git push -u origin main
```

Then add topics and branch protection.

---

### Step 10: Final QA pass

---

## Post-Launch Notes

- When Debaser updates a policy: edit the markdown file, regenerate the PDF, commit both, submit via PR to main
- To add French versions later: create `policies/fr/` and `pdfs/fr/` folders; update README with a language toggle section
- The git log is the archive of all old policy versions — no separate versioning files needed
