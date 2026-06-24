# 🍳 Prompt: Build a task on a branch

> Paste this prompt to get your AI builder to build ONE task, in small steps, without wandering into anyone else's work.

This is the prompt you reach for during [Step 4: Claim and build](../guides/step-4-claim-and-build.md). It keeps your AI builder (Claude Code, Cursor, etc.) tightly focused on the single piece of work you own.

## ⏱️ Before you start

- ✅ Be on your own [branch](../GLOSSARY.md) (a safe, private copy of the project). Step 4 shows you how to create and switch to it.
- ✅ Have the [PRD](../GLOSSARY.md) open or to hand — that's the short document that says what the app is and what each feature should do.
- ✅ Have your row from the [task board](../templates/task-board.md) — the one task with your name on it.

> 💡 **Tip:** Keep it scoped. The number-one cause of messy merges later is an AI builder that "helpfully" edited ten files when you only asked for one feature. The prompt below tells it not to do that.

## 💬 The prompt to paste

Fill in the two `[BRACKETED]` parts, then paste the whole thing into your AI builder.

```
Here is our PRD (our product plan). Read it first so you understand
the whole app, but do NOT build all of it:

[PASTE THE PRD HERE, OR SAY: "the PRD is in the file README.md / PRD.md"]

Here is MY specific task — this is the ONLY thing I want you to build
right now:

[DESCRIBE YOUR ONE TASK IN PLAIN ENGLISH — what the feature does,
what the person using it should see and be able to do]

Please follow these rules:
1. Build ONLY my task above. Do not build other features, even if
   the PRD mentions them.
2. Work in small steps. Do one small piece, show me what you did,
   and explain it in plain English before moving on.
3. Do NOT change files that are outside the scope of my task. If you
   think you need to touch a shared file, stop and ask me first.
4. Match the existing project's style and structure — look at how the
   current code and files are organized and stay consistent.
5. Write it so it can merge cleanly later: keep your changes contained,
   and avoid sweeping edits to files other teammates are likely touching.

After each step, tell me how to check that the step works, then wait
for me to confirm before you continue.
```

## 🧑‍🍳 RecipeRoll example

Maya owns Feature A, the "Add a recipe" form, on branch `feature/add-recipe-form`. After switching to her branch, she pastes the prompt and fills in the brackets:

- For the PRD part: *"The PRD is in the file PRD.md at the top of the project."*
- For her task part:

```
My task is the "Add a recipe" form. A home cook should see a form with
three fields: a recipe title, a list of ingredients, and the steps to
make it. When they fill it in and click "Save recipe", the recipe should
be saved so it can be browsed later. Duplicate recipe titles are allowed
for v1 — that's a team decision, keep it simple.
```

Her AI builder reads the PRD, then builds just the form — one small step at a time — and leaves Sam's browse page and Priya's search alone.

> ⚠️ **Watch out**
> - Don't paste a vague task like "make RecipeRoll work." The AI will try to build everything and step on your teammates' files.
> - If the AI starts editing a file you didn't expect (especially a shared one), stop it and ask why. It's fine to say: *"Please undo that and only change files needed for my task."*
> - Resist "while I'm here" extras. If the AI offers to also add photos or ratings, decline — those are "Later" items, not your task.
> - Test each step as you go. Don't let ten steps pile up unchecked; small confirmations catch problems early.

## ✅ You're done when

- [ ] The AI built only your task, nothing else.
- [ ] You checked each step worked before moving on.
- [ ] No files outside your task's scope were changed (or any that were, you approved on purpose).
- [ ] Your feature does what your task-board row and the PRD describe.

## ➡️ Next

Back to the guide: [Step 4: Claim and build](../guides/step-4-claim-and-build.md). To stay current with your teammates' work while you build, use [Prompt 05: Keep me in sync](05-keep-me-in-sync.md).
