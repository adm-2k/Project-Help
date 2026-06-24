# 🧭 Decision Log

> A short record of the choices your team has made, and why, so you never have to re-argue the same point twice.

Teams forget *why* they decided things. Then someone reopens the debate, or your AI builder quietly does the opposite. This file fixes that.

## 🎯 What to record here

Whenever you make a choice that affects **the product** (what you are building) or **how you build** (tools, naming, ways of working), add one line to the table below.

You do not need a meeting. A choice as small as "we'll allow duplicate recipe names" counts. If it is the kind of thing someone might question later, log it.

> 💡 **Why this matters:** A clear decision log keeps every teammate aligned, and it keeps your AI builder (Claude Code, Cursor, etc.) consistent. When you point the AI at this file, it follows the same rules everyone agreed on instead of guessing.

## 💬 How to add a decision

1. Add a new row at the **top** of the table (newest first).
2. Fill in today's date, the decision in plain English, the reason, any alternatives you talked about, and who decided.
3. Keep each cell to one short sentence. This is a memory aid, not a report.

> ✅ **Tip:** State the decision as something you can act on. "Allow duplicate recipe names" is clear. "Discussed recipe names" is not.

## 📋 The log

| Date | Decision | Why | Alternatives considered | Decided by |
|------|----------|-----|-------------------------|------------|
| 2026-06-22 | v1 allows duplicate recipe names. | Keep it simple and ship faster; revisit if it becomes confusing. | Block duplicates; auto-number duplicates (e.g. "Soup (2)"). | The team |
| 2026-06-18 | We organize work using a [branch](../GLOSSARY.md) per feature, named `feature/short-description`. | Everyone can build their feature without stepping on each other; names stay tidy and predictable. | One shared branch for everyone; one branch per person. | The team |
| 2026-06-16 | We will use GitHub plus our AI builder (Claude Code, Cursor, etc.) for this project. | The team is non-technical; the AI handles the hard parts, and GitHub keeps everyone's work safe and shareable. | A shared folder with no version history; a no-code app builder. | The team |

> ⚠️ **Watch out:**
> - Record the decision, not the whole discussion. The "Why" column is one sentence, not a transcript.
> - Do not delete or rewrite old rows. If you change your mind, add a **new** row that says so and references the old one by date.
> - If a decision came out of a bug or question, link back to it in the [Issue Log](ISSUE-LOG.md).

## 🔗 Related

- Guide: [Step 2 — Review the PRD](../guides/step-2-review-the-prd.md) — many early decisions get logged here.
- Guide: [Step 7 — Update the roadmap and log issues](../guides/step-7-update-roadmap-and-log-issues.md)
- Issue Log: [ISSUE-LOG.md](ISSUE-LOG.md)
- Glossary: [../GLOSSARY.md](../GLOSSARY.md)
