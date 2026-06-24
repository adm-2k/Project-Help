# Step 3: Break the work into branch-sized tasks

> Split the work into small, independent pieces so each teammate can build on their own without bumping into each other.

**Goal:** Turn your reviewed PRD into a list of small tasks, each with one owner and one branch. · **Time:** 45 to 60 minutes · **Who:** The whole team, together, with your AI builder (Claude Code, Cursor, and the like).

## Why it matters

This is the most important coordination step in the playbook, so give it extra care. When the work is split well, four people can build at the same time and almost never trip over each other. When it is split badly, two people end up editing the same file, and you get a _merge conflict_ ([merge conflict](../GLOSSARY.md)) — the moment when the tools cannot decide whose change to keep. Conflicts are normal, and they are fixable. But the easiest conflict to handle is the one you never create.

## What makes a good task

Before you split anything, learn the four rules. A good task is:

| Rule | What it means | Quick test |
| --- | --- | --- |
| **Small** | One person can finish it in 1 to 3 days. | "Could I show something working by Thursday?" |
| **One owner** | Exactly one named person is responsible. | "Whose name is on this?" |
| **One branch** | It maps to exactly one _branch_ ([branch](../GLOSSARY.md)), a private copy of the project to work in. | "What is this branch called?" |
| **Few shared files** | It touches as few of the same files as the other tasks as possible. | "Is anyone else editing these files?" |

Here is the idea worth holding onto: a branch is your own safe copy of the project. As long as you and your teammates change _different_ files, your work slots together cleanly when you combine it later. Two people editing the _same_ file at the same time is what creates a merge conflict, so keeping tasks independent is how you avoid them. For the gentle, full picture, read [How git works for non-coders](../HOW-GIT-WORKS-FOR-NON-CODERS.md).

## What to do

1. **Open your AI builder** in the project and load the decomposition prompt: [../prompts/03-decompose-into-tasks.md](../prompts/03-decompose-into-tasks.md). Paste your reviewed PRD when it asks. Here is the core request:

   ```
   Here is our reviewed PRD (pasted below).

   Break our v1 scope into small tasks, feature by feature. For each task give me:
   - the feature it belongs to
   - a one-line task description (small enough for one person in 1 to 3 days)
   - a suggested branch name in the form feature/short-description
   - the files this task will likely create or edit

   Then flag any two tasks that would touch the SAME files, and suggest how
   to keep them independent. Keep it simple — this is for a non-technical team.

   [PASTE YOUR PRD HERE]
   ```

2. **Read the proposal as a team.** The AI will suggest tasks, branch names, and the files each one touches. Look closely at any tasks it flagged as touching the same files.

3. **Adjust so each person owns independent work.** Give every teammate at least one task, and aim for each person to mostly touch their own files.

4. **Handle any overlap.** If two tasks must touch the same file, you have two options:
   - **Sequence them:** one person goes first and finishes, then the second person builds on top.
   - **Split responsibilities:** decide who owns that shared file, and have the other person work around it or ask for a small change.

5. **Decide who owns shared setup.** The first scaffolding — the empty project, the shared page layout, the place recipes are stored — belongs to _one_ named person who does it _first_, before others branch off. Do not leave it ownerless.

6. **Agree on your branch-naming convention** and write it down. Throughout this playbook we use:

   ```
   feature/short-description
   ```

   Lowercase words separated by dashes, always starting with `feature/`. For example, `feature/add-recipe-form`.

7. **Fill in the task board:** [../templates/task-board.md](../templates/task-board.md). One row per task, with these columns: Feature, Task, Owner, Branch, Files it touches, and Status.

## Example: RecipeRoll

The RecipeRoll team has four people and four features. They mapped each feature to one owner and one branch, and listed the files each task touches. Notice that the files barely overlap. That is the whole point.

| Feature | Task | Owner | Branch | Files it touches | Status |
| --- | --- | --- | --- | --- | --- |
| A — Add a recipe | Build the "Add a recipe" form (title, ingredients, steps) | Maya | `feature/add-recipe-form` | `add-recipe.html`, `add-recipe.js` | Not started |
| B — Browse recipes | Build the "Browse all recipes" list page | Sam | `feature/recipe-list` | `recipe-list.html`, `recipe-list.js` | Not started |
| C — Search | Build "Search by ingredient" | Priya | `feature/search-by-ingredient` | `search.html`, `search.js` | Not started |
| D — Favorites | Build "Save favorites" | Devin | `feature/favorites` | `favorites.html`, `favorites.js` | Not started |

Shared setup goes first. Before anyone branches, Maya volunteers to create the empty project and the one shared file where recipes live (`recipes-data.js`). She does that on its own small branch, the team merges it, and _then_ the four feature branches all start from that shared foundation. That way nobody creates the project twice.

The team also writes their first real decision into [../templates/DECISIONS.md](../templates/DECISIONS.md): "v1 allows duplicate recipe names — keep it simple; revisit if it becomes confusing."

> Going further on GitHub: Once your team is comfortable, track these tasks as GitHub Issues on a GitHub Projects board (a kanban board). It is the real-world version of the paper task board you are filling in here, and it lets you move a task from "To do" to "In progress" to "Done" as the work happens.

## Watch out for

- **Giant, vague tasks.** "Build the recipes feature" is too big and too fuzzy. If you cannot name the files it touches, split it smaller.
- **Two people in the same file at once.** This is the number-one cause of merge conflicts. If you see it, sequence the work or split who owns the file.
- **Nobody owning shared setup.** The empty project and shared layout need _one_ owner who goes _first_. Ownerless setup either never happens or happens twice.
- **Branch names that drift.** Stick to `feature/short-description`. Avoid spaces, capital letters, and people's initials, which get confusing fast.
- **Tasks bigger than three days.** If it cannot show something working within three days, cut it into smaller pieces.

## You're done when

- [ ] Every teammate owns at least one task.
- [ ] Each task has a clear one-line description.
- [ ] Each task has a branch name in the form `feature/short-description`.
- [ ] Each task lists the files it will likely touch.
- [ ] You checked for overlapping files and either avoided them or chose to sequence or split.
- [ ] Shared setup has one named owner who goes first.
- [ ] The task board ([../templates/task-board.md](../templates/task-board.md)) is filled in.
- [ ] Everyone knows the branch-naming convention.

## Next

Time to start building. Head to [Step 4: Claim a task and build on a branch](step-4-claim-and-build.md).

## Prompts and templates

- Prompt: [../prompts/03-decompose-into-tasks.md](../prompts/03-decompose-into-tasks.md) — have your AI propose the task breakdown and flag file overlaps.
- Template: [../templates/task-board.md](../templates/task-board.md) — where you record Feature, Task, Owner, Branch, Files it touches, and Status.
- Background reading: [How git works for non-coders](../HOW-GIT-WORKS-FOR-NON-CODERS.md) — why separate files keep your team conflict-free.
