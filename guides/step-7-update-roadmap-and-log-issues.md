# 🔄 Step 7: Update the Roadmap and Log Issues

> Every time you finish something, take five minutes to update the team's shared picture: where we are, what's next, what's broken, and what we decided.

**Goal:** Keep the team's shared truth current. &nbsp;**Time:** about 5–10 minutes after each finished task, plus a short weekly sync. &nbsp;**Who:** everyone, after each finished task.

## Why this matters

When you finish a task, the work lives in your head and on your screen. Your teammates can't see it. This step turns "I know what's going on" into "we all know what's going on," written down where anyone can read it. Without this small habit, finished work goes unnoticed, bugs get forgotten, and the same questions get re-argued every week.

> 💡 **Why this matters:** The roadmap is how a non-technical team always knows where things stand without asking. The [issue log](../GLOSSARY.md) stops bugs and ideas from falling through the cracks. The decision log keeps everyone — and your AI builder — aligned on the choices you've already settled.

## What you'll do

You do three quick things after your work is [merged](../GLOSSARY.md) (see [Step 6: Review and merge](step-6-review-and-merge.md)). Then you loop back to pick up the next task.

### 1. Update the roadmap

Move your finished feature to **Done** with today's date, and make sure **Next** shows what the team should pick up.

1. Open [`../templates/ROADMAP.md`](../templates/ROADMAP.md) (your team copies this into the repo once, then keeps editing it).
2. Open the [`prompts/10-update-the-roadmap.md`](../prompts/10-update-the-roadmap.md) prompt and paste it into your AI builder (Claude Code, Cursor, etc.) to draft the update for you. A simple version:

```
Here is our current ROADMAP.md:
[paste the file]

I just finished and merged "Add a recipe" form on 2026-06-24.
Please move it to Done with that date, and suggest what should be Next.
Keep the same headings and table format.
```

3. Read what it suggests, fix anything that's wrong, and save the file.

### 2. Log any bug, blocker, or idea

If you (or a teammate) noticed something broken, stuck, or worth doing later, write it down now while it's fresh.

1. Open [`../templates/ISSUE-LOG.md`](../templates/ISSUE-LOG.md) and add a row, **or** open a [GitHub issue](../GLOSSARY.md) using the [bug report](../.github/ISSUE_TEMPLATE/bug_report.md) or [feature request](../.github/ISSUE_TEMPLATE/feature_request.md) template.
2. Use the [`prompts/09-log-an-issue.md`](../prompts/09-log-an-issue.md) prompt to turn a rough note into a clear entry:

```
Help me write a clear issue from this note:
"Search seems broken when you use capital letters."

Give me a short title, what's expected vs. what happens,
and steps to reproduce. Keep it plain and brief.
```

> 📋 **Bug or idea?** A *bug* is something that's broken now. An *idea* is something to maybe build later. Both belong in the log — just label them so the team can tell them apart.

### 3. Record notable decisions

If the team agreed on something that shapes how the app works, write it in the decision log so nobody re-argues it.

1. Open [`../templates/DECISIONS.md`](../templates/DECISIONS.md) and add a one-line entry: what you decided, why, and who decided.
2. Keep it short. One sentence is fine.

### 4. Loop back to the next task

You're now ready to start again. Pick your next task from the board and return to [Step 3: Break into tasks](step-3-break-into-tasks.md) (if you need new tasks) or jump straight to [Step 4: Claim and build](step-4-claim-and-build.md).

## 🍳 RecipeRoll example

Maya just merged the **Add a recipe** form (her branch `feature/add-recipe-form`). Here's her five-minute wrap-up.

**Roadmap** — she moves her feature to Done:

```
## Done
- ✅ Add a recipe (title, ingredients, steps) — merged 2026-06-24 (Maya)

## Next
- Browse all recipes (Sam, feature/recipe-list)
- Search by ingredient (Priya, feature/search-by-ingredient)
```

**Issue log** — Priya noticed a bug while testing, so Maya logs it:

| ID | Type | Title | Details | Found by | Status |
|----|------|-------|---------|----------|--------|
| 7 | Bug | Search is case-sensitive | Typing "Tomato" misses "tomato" — search should ignore capital letters | Priya | Open |

**Decision log** — the team's earlier choice already sits here, so nobody reopens it:

```
- 2026-06-20 — v1 allows duplicate recipe names. Keep it simple; revisit if it becomes confusing. (Decided by the team)
```

That's it. Maya closes her laptop knowing the whole team can see exactly where RecipeRoll stands.

> ⚠️ **Watch out**
> - **Finishing work but never updating the roadmap.** If it's not on the roadmap, your teammates can't see it's done — and two people might build the same thing.
> - **Keeping bugs only in your head.** "I'll remember it" almost always becomes "I forgot it." Log it now, even roughly.
> - **Re-deciding settled things.** Before debating, check [`../templates/DECISIONS.md`](../templates/DECISIONS.md). If it's already decided, point to the entry instead of starting over.

## You're done when

- [ ] The roadmap reflects reality — your finished feature is in **Done** with a date, and **Next** is current.
- [ ] Any new bug, blocker, or idea is logged in the issue log (or as a GitHub issue).
- [ ] Any notable decision is recorded in the decision log.
- [ ] You've picked your next task and know where to go.

## Next

➡️ Loop back to [Step 3: Break into tasks](step-3-break-into-tasks.md) for new work, or [Step 4: Claim and build](step-4-claim-and-build.md) to start your next task. To see the whole journey again, return to the [README](../README.md).

## Prompts & templates you'll use

- 💬 Prompt: [`prompts/09-log-an-issue.md`](../prompts/09-log-an-issue.md) — turn a rough note into a clear issue.
- 💬 Prompt: [`prompts/10-update-the-roadmap.md`](../prompts/10-update-the-roadmap.md) — draft your roadmap update.
- 📄 Template: [`templates/ROADMAP.md`](../templates/ROADMAP.md) — where the team tracks Done, Now, and Next.
- 📄 Template: [`templates/ISSUE-LOG.md`](../templates/ISSUE-LOG.md) — the running list of bugs, blockers, and ideas.
- 📄 Template: [`templates/DECISIONS.md`](../templates/DECISIONS.md) — the record of choices the team has made.
