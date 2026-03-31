---
name: document-creator
description: >
  Creates polished, professional documents — primarily PowerPoint presentations, but also Excel
  spreadsheets and Word reports — from raw inputs: meeting notes, data dumps, receipts, briefs,
  strategy memos, or even a rough description. Use this skill ANY TIME the user wants to turn
  information into a finished file. This includes requests like "make a deck", "turn these notes
  into slides", "build a spreadsheet from this data", "create a report", "summarize this into a
  presentation", or any task where the end result is a professional document. Apply a
  corporate, executive-ready style by default: dark header bars, structured layouts, data-driven
  visuals, clean typography. Don't wait for the user to ask for a "skill" — if they want a
  document, use this.
---

# Document Creator

Produce polished, professional documents from any raw input — notes, data, a brief description,
or uploaded files. Default to **PowerPoint** unless the user's request clearly calls for a
spreadsheet or text document.

---

## Format Decision Guide

| Request type | Best format |
|---|---|
| Presentation, deck, slides, executive summary, pitch | **PowerPoint (.pptx)** |
| Data with calculations, budgets, expense trackers, models | **Excel (.xlsx)** |
| Reports, contracts, formal letters, SOPs, written analyses | **Word (.docx)** |

When in doubt, ask one clarifying question: "Is this for a meeting/presentation, or will it be read?"

---

## Corporate Style Defaults

These defaults apply to all documents unless the user says otherwise:

- **Tone:** Formal, concise, confident. No filler phrases ("As we can see…"). Lead with the point.
- **Color palette:** Dark navy or forest green headers; warm cream or white content areas; amber/gold accent for emphasis. One dominant color, one accent — not a rainbow.
- **Typography:** Georgia or Calibri for headers; Calibri for body. No decorative fonts.
- **Structure:** Always start with a clear "so what" — the recommendation or takeaway first, then the supporting evidence.
- **Data:** Show numbers as callouts when they're strong (big stat + small label). Use charts for trends, tables for comparisons.

---

## Workflow

### 1. Understand the input

Before creating anything, scan all provided content — notes, files, data — and identify:
- The core message or recommendation
- The intended audience and their level of familiarity with the topic
- Key data points worth highlighting
- What's missing or unclear (ask only if blocking)

### 2. Plan the structure out loud

Before building, state your intended structure in 1-2 sentences:
> "I'll build a 7-slide deck: title → market opportunity → recommendation → location analysis → financials → risks → next steps."

This lets the user redirect before you invest in the wrong structure.

### 3. Build the document

Follow the relevant skill for the format:
- **PowerPoint** → use the `pptx` skill (`/sessions/.../skills/pptx/SKILL.md`)
- **Excel** → use the `xlsx` skill (`/sessions/.../skills/xlsx/SKILL.md`)
- **Word** → use the `docx` skill (`/sessions/.../skills/docx/SKILL.md`)

Always save the output to the workspace folder and present it to the user with `present_files`.

### 4. Confirm before iterating

After presenting the file, briefly state:
- What structure you chose and why
- Any assumptions you made about missing information
- 1-2 things the user might want to customize (colors, logo, specific numbers)

---

## PowerPoint: Corporate Template

When building slides from scratch, apply this structure as the default:

1. **Title slide** — dark background, company/project name, subtitle, date
2. **Executive summary** — 3 key stats as callouts + 4-5 bullet takeaways
3. **[Content slides]** — one clear message per slide; title = the takeaway, not the topic
4. **Recommendation** — bold single statement + 3 supporting pillars
5. **Risks / considerations** — concise, shows rigor without burying the recommendation
6. **Next steps** — numbered, owner + date format when possible
7. **Closing slide** — dark background, single memorable line, contact info

**Slide design rules:**
- Title = the conclusion, not the category ("Revenue grew 23%" not "Revenue")
- Every slide needs at least one visual element: chart, stat callout, icon, or comparison
- Use dark backgrounds for title + closing slides; light/cream for content ("sandwich" structure)
- Max 5 bullets per slide; max 12 words per bullet
- Never use decorative lines under titles

---

## Excel: Report Structure

For data-heavy files, always create at least two sheets:

1. **Data sheet** — raw or processed records with clear column headers
2. **Summary sheet** — SUMIF/PIVOT formulas, totals by category, charts

Apply conditional formatting to flag outliers (red for over-budget, green for on-target).
All totals must use Excel formulas, never hardcoded values.

---

## Quality Bar

Before delivering any document, verify:
- [ ] The main message is clear within the first 30 seconds of reading
- [ ] Numbers are accurate and sourced from the provided data (no invented figures)
- [ ] No placeholder text remains (no "Lorem ipsum", "TBD", "XXX")
- [ ] For PPTX: run visual QA — convert to images and check for overflow/overlap
- [ ] For XLSX: run `scripts/recalc.py` and confirm zero formula errors
