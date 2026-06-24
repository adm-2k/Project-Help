# Before You Merge

> A quick check to run before and after you merge a pull request, so `main` keeps working and the team stays in sync.

Goal: merge a teammate's finished work safely, then tidy up so everyone moves on smoothly. Time: about 10 minutes. Who: one reviewer (and the person merging).

Merging means adding a finished branch into `main`, the shared version everyone builds on. Because of golden rule number one, `main` always works, a careful merge protects the whole team. The after-merge tidy-up keeps your documents honest and stops the next person from building on stale work.

> Tip: Your AI builder or GitHub Desktop does the actual merge with one button. Your job is the thinking around it, which is these checks.

## Before you merge

- [ ] At least one teammate reviewed and approved the pull request
- [ ] There are no unresolved conflicts. If any appear, fix them first with [the conflict prompt](../prompts/06-resolve-a-merge-conflict.md)
- [ ] You re-checked that `main` will still work after this merge (the change does what it claims and doesn't break what's already there)
- [ ] The description is accurate and matches what the branch actually changes

## After you merge

- [ ] Delete the branch. Its work now lives in `main`, so the branch isn't needed anymore
- [ ] Set the task to Done on the [task board](../templates/task-board.md)
- [ ] Tell the team to pull the latest `main`, so everyone is building on the newest version
- [ ] Update the [ROADMAP](../templates/ROADMAP.md) to reflect what's now finished
- [ ] Update the [ISSUE-LOG](../templates/ISSUE-LOG.md) if this merge closed or opened any issues

> Watch out: Don't forget to tell everyone to pull after a merge. If teammates keep working on an old `main`, they'll hit avoidable conflicts later. One quick message in your channel prevents it.

## RecipeRoll example

Maya reviews Sam's `feature/recipe-list` PR, approves it, and confirms there are no conflicts and that browsing recipes works. She clicks `Merge`, then deletes the branch, sets Feature B to Done on the task board, and posts "Browse page merged, everyone please pull the latest `main`." She ticks Feature B off the ROADMAP. No new issues, so the ISSUE-LOG stays as is.

## You're done when

- [ ] Every box above is checked, including the after-merge tidy-up

For the full walkthrough, see [Step 6: Review and merge](../guides/step-6-review-and-merge.md).
