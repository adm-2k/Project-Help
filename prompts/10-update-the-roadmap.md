# 🗺️ Prompt: Update the roadmap

> After you finish a task, draft the tidy updates to your roadmap and task board so the whole team sees what is done and what is next.

Your **roadmap** is the team's shared picture of what is planned, in progress, and finished. Your **task board** tracks who is doing what right now. Keeping both current is how everyone stays in sync without a meeting. This prompt drafts those updates for you.

## ⏱️ Before you start

- Know exactly what you just finished (the task name).
- Know today's date so the "Done" entry is dated correctly.
- Have the [roadmap](../templates/ROADMAP.md) and [task board](../templates/task-board.md) open so you can see their current state.

> 💡 **Tip:** Do this the moment a task is merged, while it is fresh. A roadmap that is updated late is a roadmap nobody trusts.

## 💬 The prompt

Copy this into your AI builder. Fill in the [BRACKETS].

```
I just finished a task and need to update our roadmap and task board.

The task I completed: [task name]
Today's date: [YYYY-MM-DD]
The current roadmap content:
[paste the relevant part of ROADMAP.md]
The current task board content:
[paste the relevant part of task-board.md]

Please draft:

1. ROADMAP update: move this task into the Done section with today's
   date next to it. Then look at what is left and tell me clearly what
   is Next — the most sensible thing for the team to pick up.

2. Task board update: change this task's status to Done (or merged),
   and note who owned it.

Give me the exact text to paste into each file, showing only the lines
that change. Keep the wording short and consistent with what is
already there. Do not invent tasks that are not in what I pasted.
```

> 🎯 **Why this matters:** When the roadmap is current, teammates pick their next task themselves without asking. When it drifts, work gets duplicated or dropped.

## 🍳 RecipeRoll example

Sam finishes Feature B, the "Browse all recipes" list page, and it gets merged. He pastes his task name and today's date into the prompt. The AI drafts:

- **Roadmap, Done:** `Browse all recipes (list page) — done 2026-06-24, owner: Sam`
- **Roadmap, Next:** "Search by ingredient (Priya) is the natural next piece, since browsing now exists to search within."
- **Task board:** Feature B row status changed from `In review` to `Done`, owner Sam.

Sam pastes those exact lines into the [roadmap](../templates/ROADMAP.md) and [task board](../templates/task-board.md).

## ⚠️ Watch out

> - **Update both files.** A done task on the roadmap but still "in progress" on the task board confuses everyone.
> - Always include the date on the Done entry. "Done" with no date hides whether something is fresh or stale.
> - Do not let the AI invent or reorder tasks you did not paste in. It should only touch what you give it.

## ✅ You're done when

- [ ] The finished task is in the roadmap's Done section, with today's date.
- [ ] The roadmap clearly shows what is Next.
- [ ] The task board status for this task is updated, with the owner noted.

## ➡️ Next

Use this prompt as part of [Step 7: Update the roadmap and log issues](../guides/step-7-update-roadmap-and-log-issues.md).

## 📎 Related files

- Guide: [Step 7: Update the roadmap and log issues](../guides/step-7-update-roadmap-and-log-issues.md)
- Template: [Roadmap](../templates/ROADMAP.md)
- Template: [Task board](../templates/task-board.md)
