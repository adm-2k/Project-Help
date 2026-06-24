# Step 5: Open a pull request (PR)

> You propose adding your finished piece to the shared project so a teammate can review it before it becomes part of the real app.

**Goal:** open a clear, well-described pull request from your branch · **Time:** about 15 minutes · **Who:** the person who built the task.

## Why it matters

A *pull request* [(PR)](../GLOSSARY.md) is a request that says, "Here is my piece. Please review it, and if it looks good, add it to the shared project." It is the moment your work goes from yours alone to something the team checks together. Think of it like handing in a short, tidy report instead of a messy pile of pages: the clearer your hand-off, the faster and kinder the review. Nothing merges into the shared project without a PR, so this is the gate that keeps the team's app stable.

## What to do

First, run the checks in [../checklists/before-you-open-a-pr.md](../checklists/before-you-open-a-pr.md). Open a PR only when your piece actually works.

1. **Push your branch.** Pushing means uploading the work from your computer to the shared project online (on [GitHub](../GLOSSARY.md)). In your AI builder (Claude Code, Cursor, and the like) or in GitHub Desktop, click `Push`. The command-line equivalent, for reference, is:

   ```
   git push
   ```

2. **Open a pull request** from your branch into `main`. [`main`](../GLOSSARY.md) is the shared, trusted version of the app. On GitHub.com, after pushing, you usually see a yellow banner with a `Compare & pull request` button. Click it. (Your AI builder and GitHub Desktop also have a `Create Pull Request` button.) Confirm it is merging from your branch into `main`.

3. **Generate a clear description.** Paste the prompt from [../prompts/07-write-my-pr.md](../prompts/07-write-my-pr.md) into your AI builder. It writes a description covering what changed, why, how to test it, screenshots if your work is visual, and what a reviewer should watch for.

4. **Complete the PR template.** The repo includes a [pull request template](../.github/PULL_REQUEST_TEMPLATE.md) that fills in automatically when you open the PR. Drop in the description from step 3 and answer each section. Don't leave it blank.

5. **Link the related task or issue.** Connect this PR to the task you claimed on the [task board](../templates/task-board.md). Typing `Closes #12` (with your task's number) in the description tells GitHub to tick that task off automatically when the PR merges.

6. **Request a reviewer.** On the right side of the PR page, click `Reviewers` and pick one teammate. Tell them in your team chat that it is ready.

> Tip: Keep PRs small and focused, one feature or fix each. A small PR is reviewed in minutes; a giant one sits for days.

## Example: RecipeRoll

Maya finished her "Add a recipe" form. She pushes her branch `feature/add-recipe-form`, then opens a pull request into `main`.

She titles it "Add a recipe form" and pastes the description she generated from [../prompts/07-write-my-pr.md](../prompts/07-write-my-pr.md):

```
What changed: New "Add a recipe" form with fields for title, ingredients, and steps.
Why: Lets home cooks save a recipe — the first feature in our v1 scope.
How to test: Open the app, click "Add a recipe", fill in all three fields, and submit.
   The new recipe should appear in the list.
Screenshots: (attached the form and the saved recipe)
What to watch: v1 allows duplicate recipe names on purpose — that's expected, see DECISIONS.
```

She links it to her task (`Closes #3`) and requests Sam as her reviewer. It is now waiting for a friendly second pair of eyes.

> Going further on GitHub: Two optional conveniences are worth knowing. First, writing `Closes #12` in the description links the PR to its issue, and GitHub closes that issue automatically when the PR merges. Second, if you want early feedback before your work is ready, open a `Draft` pull request instead of a regular one; it signals "look, but don't merge yet." Third, if your team has connected a host (see [Step 8](step-8-share-and-go-live.md)), each pull request gets its own live preview link your reviewer can open and try before merging.

## Watch out for

- **Huge PRs.** If your PR touches many unrelated things, split it. Reviewers struggle with big ones.
- **Empty descriptions.** A PR titled "updates" with no detail forces your reviewer to guess. Always fill in the template.
- **Skipping the test.** Never open a PR for something you haven't run. Test it, then share it.

## You're done when

- [ ] Your branch is pushed to GitHub.
- [ ] A pull request is open, merging your branch into `main`.
- [ ] The title is short and clear (for example, "Add a recipe form").
- [ ] The description is complete: what changed, why, how to test, what to watch.
- [ ] The related task or issue is linked.
- [ ] A teammate is assigned as reviewer.

## Next

Hand it off and help close the loop: [Step 6: Review and merge](step-6-review-and-merge.md).

## Prompts and templates

- [../prompts/07-write-my-pr.md](../prompts/07-write-my-pr.md) — generates your PR description.
- [../.github/PULL_REQUEST_TEMPLATE.md](../.github/PULL_REQUEST_TEMPLATE.md) — the form that fills in automatically.
- [../checklists/before-you-open-a-pr.md](../checklists/before-you-open-a-pr.md) — quick checks to run first.
