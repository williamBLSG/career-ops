---
description: "AI job search command center -- show menu or evaluate job description"
---

# career-ops — AI Job Search Pipeline

Arguments provided: "$ARGUMENTS"

## Auto-detect mode

If arguments contain a job description or URL (keywords like "responsibilities", "requirements", "qualifications", "about the role", "http", "https"), execute **auto-pipeline mode** — read `modes/auto-pipeline.md` and follow all steps.

If arguments match a sub-command, route to the appropriate mode:

| Argument | Mode file | Description |
|----------|-----------|-------------|
| `oferta` or `evaluate` | `modes/oferta.md` | Evaluate job offer (A-F scoring) |
| `ofertas` or `compare` | `modes/ofertas.md` | Compare and rank multiple offers |
| `contacto` or `contact` | `modes/contacto.md` | LinkedIn outreach (find contacts + draft) |
| `deep` | `modes/deep.md` | Deep company research |
| `interview-prep` or `interview` | `modes/interview-prep.md` | Interview preparation for specific company |
| `pdf` | `modes/pdf.md` | Generate ATS-optimized CV |
| `training` | `modes/training.md` | Evaluate course/cert against goals |
| `project` | `modes/project.md` | Evaluate portfolio project idea |
| `tracker` | `modes/tracker.md` | Application status overview |
| `apply` | `modes/apply.md` | Live application assistant |
| `scan` | `modes/scan.md` | Scan portals for new offers |
| `pipeline` | `modes/pipeline.md` | Process pending URLs from inbox |
| `batch` | `modes/batch.md` | Batch processing with parallel workers |
| `patterns` | `modes/patterns.md` | Analyze rejection patterns and improve targeting |

## If no arguments or unrecognized command

Show the discovery menu:

```
📋 career-ops — AI Job Search Command Center

Paste a job URL or description to auto-evaluate it, or use a command:

  /career-ops evaluate    — Evaluate a job offer (A-F scoring)
  /career-ops compare     — Compare and rank multiple offers
  /career-ops pdf         — Generate ATS-optimized CV for a role
  /career-ops scan        — Scan portals for new offers
  /career-ops pipeline    — Process pending URLs from inbox
  /career-ops batch       — Batch process offers in parallel
  /career-ops tracker     — View application status
  /career-ops contact     — LinkedIn outreach (find contacts + draft)
  /career-ops deep        — Deep company research
  /career-ops interview   — Interview prep for specific company
  /career-ops apply       — Live application assistant
  /career-ops training    — Evaluate course/cert against goals
  /career-ops project     — Evaluate portfolio project idea
  /career-ops patterns    — Analyze rejection patterns

💡 Tip: Just paste a job URL and I'll run the full pipeline automatically.
```

## Before executing any mode

1. Read `modes/_shared.md` (system rules, scoring logic)
2. Read `modes/_profile.md` (user customizations — always override _shared.md)
3. Read `cv.md` and `config/profile.yml`
4. Read `article-digest.md` if it exists
5. Then read and execute the specific mode file
