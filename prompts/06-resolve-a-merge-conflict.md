# Prompt: Resolve a merge conflict

> Paste this prompt when two sets of changes touch the same lines and git asks you to choose. Your AI builder will walk you through it calmly, step by step.

First, breathe. A *merge conflict* (defined in the [glossary](../GLOSSARY.md)) is normal and fixable. It means you and a teammate edited the same lines of the same file, and git wants a human to decide which version to keep. Nothing is broken, and nothing is lost. For the full mental picture, see [How git works for non-coders](../HOW-GIT-WORKS-FOR-NON-CODERS.md).

You'll usually meet a conflict during [Step 6: Review and merge](../guides/step-6-review-and-merge.md), or when you sync your branch.

## Before you start

- Note which file or files are showing a conflict. Your AI builder or GitHub will name them for you, for example "Conflict in `recipes.js`".
- Don't delete the strange `<<<<<<<`, `=======`, and `>>>>>>>` markers yourself. Let the AI explain them first.

> Remember: A conflict feels scary the first time because the file looks messy, but the fix is a conversation. The AI explains both versions in plain English, you pick what's right, and it cleans up. Most conflicts take a minute or two.

## The prompt to paste

Fill in the file name in the brackets, then paste it all.

```
I have a merge conflict and I'd like help fixing it calmly, step by step.
I'm not a coder, so please keep everything in plain English.

The conflict is in this file (or files):

[NAME THE FILE(S) THAT SHOW A CONFLICT, e.g. "recipes.js"]

Please:
1. Open the conflicting file and show me the conflict.
2. Explain in plain English what each "side" of the conflict is — what MY
   version is trying to do, and what the OTHER version (my teammate's) is
   trying to do.
3. Recommend whether I should keep one side, keep the other, or combine
   both — and explain WHY in simple terms.
4. Once I confirm, make the change for me, remove the conflict markers,
   and save the file.
5. Tell me clearly when the conflict is fully resolved and what to do next
   to finish the merge.

Go one file at a time, and check with me before you change anything.
```

## RecipeRoll example

When Priya merges her `feature/search-by-ingredient` work, git finds a conflict in a shared file because both she and Sam edited how recipes are read. She pastes the prompt with `recipes.js` in the brackets. Her AI builder replies:

> *"Here's the conflict. Your side adds a function that filters recipes by an ingredient for your search feature. Sam's side added a function that returns all recipes for his browse page. These two don't actually disagree — they're different functions that both belong in the file. My recommendation is to keep both, since the app needs the browse list AND the search. Shall I combine them and remove the conflict markers?"*

Priya says yes. The AI keeps both functions, deletes the `<<<<<<<` markers, saves the file, and tells her the merge is complete. Total time: about a minute. (She also notes a real bug to log later: search is case-sensitive, so "Tomato" misses "tomato".)

> Watch out:
> - Don't hand-edit the conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`) before the AI explains them. It's easy to delete the wrong half. Let the AI guide you.
> - "Keep both" is often right when the two changes are unrelated. "Keep one" is right when they're two versions of the same thing. Ask the AI which case you're in.
> - Resolve one file at a time and re-read the AI's plain-English summary before confirming. Don't rush-click `accept`.
> - After resolving, make sure the AI confirms the conflict is fully gone. Leftover markers will cause errors later.

## You're done when

- [ ] You understood, in plain English, what each side of the conflict was.
- [ ] You chose to keep one side or combine both, on purpose.
- [ ] All the conflict markers are gone and the file is saved.
- [ ] The AI confirmed the merge is complete and told you the next step.

## Next

Head back to [Step 6: Review and merge](../guides/step-6-review-and-merge.md) to finish merging. Still unsure how branches and merging fit together? Re-read [How git works for non-coders](../HOW-GIT-WORKS-FOR-NON-CODERS.md). It makes the next conflict even easier.
