# Issue Log

> A shared list of every bug, blocker, idea, or question your team does not want to forget.

This is the simplest way to keep track of loose ends. It is one table in one file, and anyone on the team can add a row.

## When to log something

Add a row whenever you hit one of these and you do not want it to slip through the cracks:

- **Bug** — something works in a way it should not. (For example, search misses results it should find.)
- **Blocker** — something is stopping you from finishing your task right now.
- **Idea** — a "wouldn't it be nice if..." you want to revisit later.
- **Question** — something the team needs to decide or find out.

When in doubt, log it. A one-line note now saves a "wait, what was that thing?" conversation later.

## How to log something

1. **Pick the next free ID.** Count up: 001, 002, 003, and so on.
2. **Turn the thought into a clear entry.** Use the prompt [../prompts/09-log-an-issue.md](../prompts/09-log-an-issue.md) to tidy a messy thought into a short entry, then paste the result into the table below.
3. **Set the status to `Open`.**
4. **Update the status as work moves.** When someone starts on it, change the status to `In progress`. When it is fixed or answered, change it to `Resolved` and link to the [pull request](../GLOSSARY.md) that fixed it, if there is one.

A *pull request* (PR) is how a change gets reviewed and added to the project. If the term is new, see the [glossary](../GLOSSARY.md).

## The log

| ID | Date | Type | Description | Raised by | Status | Link / PR |
|----|------|------|-------------|-----------|--------|-----------|
| 001 | 2026-06-20 | Bug | Search is case-sensitive, so typing `Tomato` misses `tomato`. Search should ignore capital letters. | Priya | Open | — |
| 002 | 2026-06-21 | Idea | Let people sort the recipe list alphabetically by title. Nice-to-have, not needed for v1. | Sam | Open | — |
| 003 | 2026-06-22 | Question | When two recipes have the same name, how do we tell them apart in the list? | Maya | Resolved | See [DECISIONS.md](DECISIONS.md) — duplicates allowed for v1 |

> Watch out: A few habits keep this log trustworthy.
> - Do not reuse an ID. Each row keeps its own number forever, even after it is resolved.
> - Keep the description to one or two sentences. Detail can live in the linked PR or a follow-up note.
> - "Resolved" means done and checked, not "probably fixed." If you are unsure, leave it `In progress`.

## Ready for the real thing? Use GitHub Issues

This file is a fine way to start. Once your team is comfortable, GitHub Issues is the natural next step: it lives right next to your code, lets people comment, and connects directly to pull requests. Think of this table as training wheels, and Issues as the bike.

To make the switch easy, ready-made forms already live in the `.github` folder:

- Report a bug with [../.github/ISSUE_TEMPLATE/bug_report.md](../.github/ISSUE_TEMPLATE/bug_report.md)
- Suggest a feature with [../.github/ISSUE_TEMPLATE/feature_request.md](../.github/ISSUE_TEMPLATE/feature_request.md)

When you switch over, you can keep this file as a historical record, or copy the open rows into GitHub Issues and retire it.

## Related

- Guide: [Step 7 — Update the roadmap and log issues](../guides/step-7-update-roadmap-and-log-issues.md)
- Prompt: [Log an issue](../prompts/09-log-an-issue.md)
- Decisions: [DECISIONS.md](DECISIONS.md)
