# 🎯 Before You Start a Task

> A quick check to run every time you pick up a new task, so you build on the latest work and never collide with a teammate.

**Goal:** Start your task cleanly on a fresh, up-to-date branch. **Time:** about 5 minutes. **Who:** each person, every time they start a task.

## 💬 Why this matters

Two minutes of checking now saves hours of untangling later. Pulling the latest shared work and claiming your task means you build on top of everyone's newest changes and nobody else starts the same thing. This little habit is what keeps a four-person team from tripping over each other.

> 💡 **Tip:** Your AI builder (Claude Code, Cursor, etc.) can do every git step below for you — just ask in plain English. The buttons in GitHub Desktop work too.

## ✅ Before you write any code

- [ ] You **pulled the latest `main`** so you have everyone's newest merged work (the shared, always-working version)
- [ ] You **claimed your task** on the [task board](../templates/task-board.md) and set it to **In progress** so the team knows it's yours
- [ ] You **confirmed your branch name** follows `feature/short-description` (lowercase words separated by dashes)
- [ ] You **created your branch from the latest `main`** (a branch is your own safe copy to work on, see the [glossary](../GLOSSARY.md))
- [ ] You **checked the task board for anyone editing the same files** — if someone is, message them and coordinate before you start
- [ ] You **re-read the relevant part of the PRD** so you're clear on exactly what "done" means for this task
- [ ] You **opened [the build prompt](../prompts/04-build-a-task-on-a-branch.md)** ready to paste into your AI builder

> ⚠️ **Watch out:** Don't create your branch from an old copy of `main`. Always pull first, then branch — otherwise you'll be building on yesterday's version and risk a needless conflict later.

## 🍳 RecipeRoll example

Maya is starting Feature A, the "Add a recipe" form. She pulls the latest `main`, sets her row on the task board to **In progress**, and creates her branch `feature/add-recipe-form` from that fresh `main`. She glances at the board, sees nobody else is touching the form files, re-reads the "add a recipe" section of the PRD (title, ingredients, steps), and opens the build prompt. Five minutes, and she's building with confidence.

## ➡️ You're done when

- [ ] Every box above is checked and your branch is ready

When all boxes are checked, follow **[Step 4: Claim and build](../guides/step-4-claim-and-build.md)**.
