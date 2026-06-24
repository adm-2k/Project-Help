# 🔄 Prompt: Keep me in sync

> Paste this prompt once a day to pull your teammates' finished work into your branch and find out, early, if anything might clash.

Use this during [Step 4: Claim and build](../guides/step-4-claim-and-build.md). While you build your feature, your teammates are finishing theirs and adding them to the shared "main" copy of the project. Pulling their work into your [branch](../GLOSSARY.md) regularly keeps you up to date and turns big surprises into tiny, easy fixes.

If the words "main", "branch", or "merge" feel fuzzy, read the friendly explainer first: [How git works for non-coders](../HOW-GIT-WORKS-FOR-NON-CODERS.md).

## ⏱️ Before you start

- ✅ Know your branch name (for example `feature/add-recipe-form`). If you're not sure, your AI builder can tell you — just ask "what branch am I on?"
- ✅ Have saved your current work. The AI can save it for you if you ask.

> 💡 **Tip:** Do this **daily**, ideally first thing. Syncing a little every day is painless. Syncing after two weeks of everyone's changes is where the scary stories come from — and even those are fixable.

## 💬 The prompt to paste

You usually don't need to change anything — just paste it as-is.

```
I'm working on my own branch in a shared project. My teammates have been
adding their finished work to the "main" copy of the project. I want to
catch up safely. Please help me, step by step:

1. First, tell me which branch I'm currently on, and make sure my
   in-progress work is saved before we change anything.
2. Pull the latest "main" into my current branch.
3. In plain English, summarize what has changed in main since I started
   my branch — what features or files my teammates added or edited.
4. Tell me whether any of those changes touch the same files I'm currently
   editing. If yes, that's a "conflict risk" — explain which files overlap
   and what I should do about it.
5. If everything pulled in cleanly with no conflicts, just say so clearly
   so I know I'm safe to keep building.

Explain each step before you do it, and pause if anything looks risky.
```

## 🧑‍🍳 RecipeRoll example

Priya owns Feature C, "Search by ingredient", on branch `feature/search-by-ingredient`. Each morning she pastes this prompt. One day her AI builder reports back:

> *"Since you branched, Sam merged the 'Browse all recipes' list page into main. He added a new file for the recipe list and a small shared helper that reads saved recipes. Your search feature reads the same saved recipes, so there's a small overlap in one shared file — a low conflict risk. I pulled main into your branch and it merged cleanly with no conflicts. You're safe to keep building. Heads up: now that Sam's list exists, you can reuse his helper instead of writing your own."*

Because Priya synced daily, she found out about Sam's work the day after it landed — not two weeks later — and she even spotted a chance to reuse his code.

> ⚠️ **Watch out**
> - Don't skip days "to avoid the hassle." The longer you wait, the more changes pile up, and the bigger any clash becomes.
> - Always let the AI save your in-progress work before pulling. The prompt above asks for this, but double-check it happened.
> - A "conflict risk" is not a problem yet — it's an early heads-up. If a real conflict does appear, it's normal and fixable: use [Prompt 06: Resolve a merge conflict](06-resolve-a-merge-conflict.md).

## ✅ You're done when

- [ ] You know what branch you're on and your work was saved first.
- [ ] The latest main has been pulled into your branch.
- [ ] You understand, in plain English, what changed in main.
- [ ] You know whether any changes overlap your files — and what to do if so.

## ➡️ Next

Back to the guide: [Step 4: Claim and build](../guides/step-4-claim-and-build.md). If a real merge conflict shows up, don't panic — go to [Prompt 06: Resolve a merge conflict](06-resolve-a-merge-conflict.md).
