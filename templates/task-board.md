# 📋 Task Board

> The single place that shows who is doing what, and where each piece of work stands right now.

This board is your team's shared map. Keep it open, glance at it often, and update it as things move.

## 💬 How to use this board

- **One owner per task.** Every task has exactly one person responsible for it. If two of you want to help, one owns it and the other can pair, but the row shows a single name.
- **Update your row's Status whenever it changes.** When you start, change `Not started` to `In progress`. When you open a [pull request](../GLOSSARY.md), change it to `In review`. When it's merged, change it to `Done`. This takes ten seconds and saves everyone confusion.
- **Pick a clear branch name.** A [branch](../GLOSSARY.md) is your own private copy of the project to work in. Name it `feature/short-description` — lowercase words separated by dashes, like `feature/add-recipe-form`. Put that exact name in your row.
- **Watch the "Files/areas it touches" column.** If your task and someone else's touch the *same* files, flag it early and talk to each other so your changes don't collide. A little coordination now prevents headaches later.

> 💡 **Why this matters:** When the board is honest and current, nobody has to ask "who's doing the search feature?" or "is that done yet?" The answer is always right here.

For how tasks are chosen and split up so they *don't* overlap, see [Step 3: Break into tasks](../guides/step-3-break-into-tasks.md). For how to claim a task and start building on your branch, see [Step 4: Claim and build](../guides/step-4-claim-and-build.md).

## 🗂️ The board

| Feature | Task | Owner | Branch | Files/areas it touches | Status | Notes |
| --- | --- | --- | --- | --- | --- | --- |
| A — Add a recipe | Build the "Add a recipe" form (title, ingredients, steps) | Maya | `feature/add-recipe-form` | `add-recipe.html`, `add-recipe.js`, shared `recipes` data | In progress | Saving works; tidying up the form layout |
| B — Browse all recipes | Build the "Browse all recipes" list page | Sam | `feature/recipe-list` | `browse.html`, `browse.js`, shared `recipes` data | In progress | Reads the same `recipes` data Maya writes — coordinating with Maya |
| C — Search by ingredient | Add "Search by ingredient" to the browse page | Priya | `feature/search-by-ingredient` | `browse.html`, `search.js` | Not started | Waiting on Sam's browse page; will build on top of it |
| D — Save favorites | Add a "Save favorite" button and a favorites view | Devin | `feature/favorites` | `favorites.js`, `browse.html` (adds a button) | In review | Pull request open; waiting for one reviewer |

> 📝 The "Files/areas it touches" column is your early-warning system. Notice that Sam (B) and Maya (A) both touch the shared `recipes` data, and that Priya (C), Devin (D), and Sam (B) all touch `browse.html`. Those are exactly the spots to coordinate on.

## 🔑 Status legend

- **Not started** — claimed by an owner, but no work has begun yet.
- **In progress** — actively being built on the owner's branch.
- **In review** — a pull request is open and waiting for a teammate to review and merge it.
- **Done** — merged into the main project and finished.

## ➡️ Next

Once you've claimed your row, head to [Step 4: Claim and build](../guides/step-4-claim-and-build.md) to start working on your branch.
