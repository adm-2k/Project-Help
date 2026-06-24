# 🎯 Step 1: Write the PRD

> In this step your whole team agrees, in writing, what you are building and for whom — before anyone builds a single thing.

**Goal:** one short document that everyone understands the same way. **Time:** about 1 hour. **Who:** the whole team, together, in a kickoff meeting.

## Why this matters

A PRD (Product Requirements Document) is a short, plain-English description of what you are building and why. It becomes your single source of truth — the one place both your teammates *and* your AI builder read from to know what "done" looks like. A vague plan produces vague software, so a focused hour here saves you days of confusion later. Write it once, together, and everyone (including the AI) builds the same thing.

> 💡 **Why this matters:** the AI is only as clear as the instructions you give it. The PRD is those instructions.

## What you'll do

1. **Sit down together.** Get all four teammates in one room or one video call. One person shares their screen and types; everyone talks.
2. **Brainstorm the problem and who has it.** Spend ten minutes on two questions: *What problem are we solving?* and *Who has that problem?* Write the rough answers down — messy notes are fine.
3. **Agree the ONE core outcome for v1.** Decide the single most important thing a person should be able to do. Everything else goes on a "Later" list. (v1 means "version 1" — your first, smallest useful version. See the [glossary](../GLOSSARY.md).)
4. **Open the template and fill it in together.** Open [`../templates/PRD-template.md`](../templates/PRD-template.md) and work through it section by section, out loud, as a team.
5. **Let the AI tidy your notes into a clean draft.** Open the prompt in [`../prompts/01-draft-prd.md`](../prompts/01-draft-prd.md), paste your rough notes where it asks, and let your AI builder (Claude Code, Cursor, etc.) turn them into a clean first draft. A short version you can paste:

   ```
   Here are my team's rough notes for an app.
   Turn them into a clear, 1-2 page PRD with these sections:
   one-line pitch, who it's for, what they can do in v1,
   what's explicitly out of scope for now, and one success
   criterion. Keep it plain and short. Here are the notes:
   [PASTE YOUR ROUGH NOTES HERE]
   ```

6. **Read it back together and trim.** Keep it to about one to two pages. If a feature is not needed for the core outcome, move it to "Later".
7. **Save it as `PRD.md` in the repo.** Ask your AI builder to save the file as `PRD.md` at the top level of your project. (A repo is the shared folder that holds your project — see [how git works](../HOW-GIT-WORKS-FOR-NON-CODERS.md).)

## 🍳 RecipeRoll example

Here is the team's finished mini-PRD for our running example, RecipeRoll:

> **🍳 RecipeRoll — PRD (v1)**
>
> **One-line pitch:** A friendly place to save your recipes and discover your friends'.
>
> **Who it's for:** Home cooks who want their recipes in one place, and who want to find new ones by ingredient.
>
> **What they can do in v1:**
> - Add a recipe (title, ingredients, steps)
> - Browse all recipes
> - Search recipes by ingredient
>
> **Out of scope for now (Later):** user accounts and login, photos, ratings, comments.
>
> **Success criterion:** A new visitor can add a recipe and then find it by searching one of its ingredients, in under a minute, without help.

Notice how short it is. Anyone on the team can read it in thirty seconds and picture the same app.

> ⚠️ **Watch out**
> - **Cramming everything into v1.** It is tempting to add login, photos, and ratings now. Don't. If it is not part of the one core outcome, write it on the "Later" list and move on. A small v1 that ships beats a big v1 that never does.
> - **Writing it so only one person understands it.** If only the person typing knows what a line means, the AI and your teammates will guess — and guess differently. Read each section aloud and make sure all four of you agree.

## ✅ You're done when

- [ ] Every teammate can say, in one sentence, what you are building and for whom.
- [ ] The v1 scope (what's in) is written down.
- [ ] The "Later" list (what's out for now) is written down.
- [ ] There is one clear success criterion everyone agrees on.
- [ ] The document is saved as `PRD.md` in your repo.

## ➡️ Next

Now that you have a first draft, pressure-test it before you build: [Step 2: Review the PRD](step-2-review-the-prd.md).

## 🗣️ Prompts & templates you'll use

- [`../templates/PRD-template.md`](../templates/PRD-template.md) — the blank PRD you fill in together.
- [`../prompts/01-draft-prd.md`](../prompts/01-draft-prd.md) — turns your rough notes into a clean draft.
