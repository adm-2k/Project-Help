# Step 6: Review and Merge

> In this step you check a teammate's work, give kind and useful feedback, and then safely fold the approved work into the shared version of your app.

**Goal:** Keep `main` healthy by reviewing before merging. · **Time:** 20–40 minutes per pull request. · **Who:** One reviewer per pull request, plus the author who responds.

A quick reminder of two words you will see a lot here. [`main`](../GLOSSARY.md) is the one shared, always-working version of your app that everyone trusts. A [pull request](../GLOSSARY.md) (PR) is the polite "please add my work to `main`" request your teammate opened in [Step 5](step-5-open-a-pull-request.md).

## Why it matters

`main` is the version of the app your whole team builds on, so it has to keep working. A review is a friendly second pair of eyes that catches problems before they reach everyone. It is also how the team learns from each other and keeps quality high. The core rule of this whole playbook lives right here: `main` always works, so never merge something broken.

## What to do

This step has two roles. Read the role that is yours right now. Most people play both over a project, reviewing others and being reviewed in turn.

### As the reviewer

You were asked to review a teammate's pull request. Your job is to confirm it does what the task said and that `main` will still work after it merges.

1. **Read the description first.** Open the pull request on GitHub. Read the title and the description the author wrote. It should say what changed and how to try it. If you cannot tell what it does, that is your first piece of feedback.
2. **Try the change, or read what changed.** The best review is to actually use the feature. Pull the author's [branch](../GLOSSARY.md) to your computer and click around. In GitHub Desktop, use `Current Branch` at the top, pick the author's branch (for example `feature/add-recipe-form`), then run the app and try it. If you cannot run it, read the `Files changed` tab on GitHub instead.
3. **Get AI help spotting problems.** Open your AI builder (Claude Code, Cursor, and the like) and paste the prompt from [../prompts/08-review-a-teammates-pr.md](../prompts/08-review-a-teammates-pr.md). It helps you find likely bugs, confusing names, and missing pieces. The AI advises; you decide.
4. **Leave kind, specific feedback.** On the pull request, write comments that point to the exact spot and suggest a fix. "This is broken" is not helpful. "When I leave the title blank and click Save, the app shows a blank screen. Could it show a gentle message instead?" is helpful.
5. **Decide: approve or request changes.** Approve when the change does what the task said and `main` will still work. If something is off, choose `Request changes` and list what you would like fixed. Lean on [../checklists/before-you-merge.md](../checklists/before-you-merge.md) so you do not miss anything.

> Tip: Feedback is about the work, never the person. Start with what is good, be specific about what to change, and assume your teammate did their best. A review is a gift, not a grade.

### As the author

Your pull request came back with comments. This is normal and good. It means someone cared enough to look closely.

1. **Read all the feedback calmly.** Comments make the work better; they are not criticism of you. Reply to each one, even if it is only "Good catch, fixing now" or "I left this on purpose because…".
2. **Make the fixes on the same branch.** Stay on your feature branch. Ask your AI builder to make the change, then save your work (a [commit](../GLOSSARY.md)) and [push](../GLOSSARY.md) it. The pull request updates by itself, with no need to open a new one.
3. **Let the reviewer know.** Add a short comment like "Done. Fixed the blank-title case, ready for another look." Then the reviewer approves.

### Merging (the author does this once approved)

1. **Look for a conflict warning.** GitHub tells you if your branch and `main` changed the same lines. If you see "This branch has conflicts that must be resolved," do not panic. A _merge conflict_ ([merge conflict](../GLOSSARY.md)) just means two people edited the same spot and git wants you to pick. Conflicts are normal, and they are fixable. Read [../HOW-GIT-WORKS-FOR-NON-CODERS.md](../HOW-GIT-WORKS-FOR-NON-CODERS.md) for the mental model, then paste the prompt from [../prompts/06-resolve-a-merge-conflict.md](../prompts/06-resolve-a-merge-conflict.md) to walk through it step by step.
2. **Merge when it is green.** Once the pull request is approved and shows no conflicts, click `Merge` on GitHub. Your work is now part of `main`.
3. **Delete the branch.** GitHub offers a `Delete branch` button right after merging. Click it. The work is safely in `main`, so the branch has done its job, and keeping it around only creates clutter.
4. **Tell the team to pull `main`.** Post in your team chat: "Merged Add-a-recipe, everyone please pull `main`." Pulling means each teammate downloads the latest `main` so they are building on the newest version. In GitHub Desktop that is the `Fetch / Pull origin` button.

Deleting the branch and asking everyone to pull keeps the whole team in sync. Skip it and teammates keep building on yesterday's app, which causes the very conflicts everyone fears.

> Going further on GitHub: Right now the "`main` always works" rule lives on trust, which works fine for a small team. Once you are comfortable, you can make GitHub enforce it. In your repository under `Settings > Branches`, add a _branch protection rule_ on `main` that requires a review before anyone can merge. With that in place, the `Merge` button stays locked until a teammate approves. While you are there, consider turning on squash-and-merge as the default, which folds all of a branch's commits into one tidy entry so your project history stays readable.

## Example: RecipeRoll

Maya finished her "Add a recipe" form on branch `feature/add-recipe-form` and opened a pull request. Sam is the reviewer.

Sam reads Maya's description, then pulls `feature/add-recipe-form` and tries the form. It is almost perfect, but when Sam leaves the title blank and clicks Save, the screen goes blank. Sam runs the prompt in [../prompts/08-review-a-teammates-pr.md](../prompts/08-review-a-teammates-pr.md), which flags the same thing.

Sam chooses `Request changes` and writes: "Love this, works great with a title. One small thing: a blank title gives a blank screen. Could it show 'Please add a title' instead?"

Maya agrees, asks her AI builder to add a gentle message, saves and pushes to the same branch, and comments "Fixed!" Sam re-checks and clicks `Approve`.

GitHub shows no conflicts, so Maya clicks `Merge`, then `Delete branch`. She posts in chat: "Add-a-recipe is merged, please pull `main`." Sam, Priya, and Devin pull. `main` still works, now with one more feature.

## Watch out for

- **Rubber-stamp approvals.** Clicking Approve without actually trying or reading the change defeats the whole point. If you did not look, do not approve.
- **Merging broken behavior.** "It mostly works" is not done. If the feature misbehaves, even in a small case like a blank title, request changes first. `main` always works.
- **Forgetting to delete the branch.** Old branches pile up and confuse everyone about what is current. Delete right after merging.
- **Forgetting to tell the team to pull.** If teammates do not pull `main`, they keep building on the old version and create avoidable conflicts.

## You're done when

- [ ] The pull request has been genuinely reviewed (tried or read), not rubber-stamped.
- [ ] Feedback was given and the author responded to it.
- [ ] The pull request is approved.
- [ ] GitHub shows no conflicts (or the conflict was resolved).
- [ ] The branch was merged into `main`.
- [ ] The branch was deleted.
- [ ] The team was told to pull `main`, and teammates have pulled.

## Next

On to [Step 7: Update the roadmap and log issues](step-7-update-roadmap-and-log-issues.md), where you record what is now done and capture anything you spotted along the way.

## Prompts and templates

- [../prompts/08-review-a-teammates-pr.md](../prompts/08-review-a-teammates-pr.md) — spot bugs, unclear names, and missing pieces.
- [../prompts/06-resolve-a-merge-conflict.md](../prompts/06-resolve-a-merge-conflict.md) — calmly resolve a conflict if GitHub flags one.
- [../checklists/before-you-merge.md](../checklists/before-you-merge.md) — the final check before you click `Merge`.
- [../HOW-GIT-WORKS-FOR-NON-CODERS.md](../HOW-GIT-WORKS-FOR-NON-CODERS.md) — the gentle mental model of branches and merging.
