# Feature Spec Template

> One short page that describes a single feature, so the owner and the AI build exactly the right thing and teammates can see what files it will touch.

Write one spec per task and keep it in a `specs/` folder in your project repo, named after the feature (for example `specs/add-recipe-form.md`). Where `PRD.md` describes the whole product, a spec zooms in on one feature.

Each section has an _italic instruction_ and a quoted RecipeRoll example. Replace both with your own answer, and keep it tight: half a page is plenty.

---

## Feature name

_Name the one feature this spec covers._

> Add a recipe form

## Owner

_The one person responsible for building it._

> Maya

## Branch

_The branch name from the task board, in the form `feature/short-name`._

> `feature/add-recipe-form`

## What it does

_One user story: As a ___ I want ___ so that ___._

> As a home cook, I want to fill in a title, ingredients, and steps and save the recipe, so that it shows up for everyone to browse.

## In scope

_The handful of things this feature must do for v1._

> - A form with fields for title, ingredients, and steps.
> - A save button that adds the recipe to the shared recipe data.
> - A short confirmation that the recipe was saved.

## Out of scope

_What this feature does not do, so it does not quietly grow._

> - Photos (Later).
> - Star ratings (Later).
> - Editing or deleting a recipe (Later).

## Files / areas it will touch

_List the files this feature will create or edit, so teammates can spot overlaps with their own tasks._

> - `add-recipe.html` — the form page.
> - `add-recipe.js` — handles the save.
> - The shared `recipes` data — also read by the browse page (coordinate with Sam).

## Done when

_A few checkable acceptance criteria. Each one is something you can confirm by trying it._

> - [ ] A cook can fill in title, ingredients, and steps and click Save.
> - [ ] The saved recipe appears in the browse list.
> - [ ] Saving an empty form shows a clear message and saves nothing.

## Links

_The PRD section this feature comes from._

> `PRD.md`, section "Add a recipe".

---

For how specs fit into the workflow, see [../guides/prepare-ai-ready-deliverables.md](../guides/prepare-ai-ready-deliverables.md). For who owns each spec and its branch, see [../templates/task-board.md](../templates/task-board.md).
