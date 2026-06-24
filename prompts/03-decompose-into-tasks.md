# 🧩 Prompt 03 — Decompose Into Tasks

> Have the AI break your finished plan into small, independent jobs the team can build at the same time without stepping on each other.

**When to use:** After the PRD is reviewed and agreed. This is Step 3.

## ✅ Before you start

- Have your finished [PRD](../templates/PRD-template.md) ready to paste.
- Know how many teammates you have, so tasks can be split fairly.
- Open the [task board](../templates/task-board.md) — you'll copy the AI's table into it.

> 💡 **What's a branch?** A *branch* is your own private copy of the project where you build your feature without disturbing anyone else's. A *branch name* like `feature/add-recipe-form` just labels that copy. See the [glossary](../GLOSSARY.md) and [How git works](../HOW-GIT-WORKS-FOR-NON-CODERS.md).

## 💬 The prompt

Copy this, replace the `[BRACKETED PARTS]`, and paste it into your AI builder.

```
You are an experienced product manager and tech lead. Break this PRD into
small, independent, branch-sized tasks the team can build in parallel.

Here is the PRD:
[PASTE YOUR FINISHED PRD HERE]

We have [NUMBER] teammates. Each person should be able to own a task alone.

Please output a TABLE with these columns:
- Feature — which part of the app this belongs to
- Task — the specific job to do (small and clear)
- Branch name — suggested name in the form feature/short-description
  (lowercase words separated by dashes)
- Files / areas it touches — the likely files or parts of the app affected
- Notes — anything important about this task

Rules for the tasks:
- Each task should take about 1 to 3 days for one person.
- Each task should have a single owner.
- Make tasks as INDEPENDENT as possible so people don't block each other.

After the table, add a section called "Collision risks":
- FLAG any two tasks that would touch the SAME files.
- For each flagged pair, suggest how to handle it: either sequence them
  (do one first, then the other) or split the shared file so they don't overlap.
```

## 💡 Tips

- Aim for one clear owner per task — shared ownership causes confusion.
- If a task looks bigger than three days, ask the AI to split it further.
- Pay special attention to "Collision risks" — those are the spots where merge conflicts could happen, and a little planning now saves headaches later.

## 🎯 What good output looks like

- A clean table where each row is one ownable task.
- Branch names follow the `feature/short-description` pattern.
- Tasks are mostly independent, and any overlaps are flagged with a plan.

### RecipeRoll example

For our running example, RecipeRoll, the table might come out like this:

| Feature | Task | Branch name | Files / areas it touches | Notes |
| --- | --- | --- | --- | --- |
| A — Add a recipe | Build the "Add a recipe" form (title, ingredients, steps) | `feature/add-recipe-form` | the add-recipe page, the recipe data store | Maya owns this |
| B — Browse recipes | Build the "Browse all recipes" list page | `feature/recipe-list` | the list page, reads the recipe data store | Sam owns this |
| C — Search | Add "Search by ingredient" | `feature/search-by-ingredient` | the list page, search box | Priya owns this |

**Collision risk flagged:** Tasks B and C both touch the list page. Suggestion — let Sam finish the basic list page first, then Priya adds search on top, so they don't edit the same file at once.

> ⚠️ **Watch out:** Don't skip the collision check. Two people editing the same file is the most common cause of a [merge conflict](../GLOSSARY.md) — easy to avoid with a little sequencing.

## ➡️ Next

Use this in [Step 3: Break into tasks](../guides/step-3-break-into-tasks.md), then everyone claims a task in [Step 4: Claim and build](../guides/step-4-claim-and-build.md).
