# Step 1: Write the PRD

> In this step your whole team agrees, in writing, what you are building and for whom, before anyone builds a single thing.

**Goal:** one short document that everyone reads the same way · **Time:** about 1 hour · **Who:** the whole team, together, in a kickoff meeting

## Why it matters

A *[PRD](../GLOSSARY.md)* (Product Requirements Document) is a short, plain-English description of what you are building and why. It becomes your single source of truth: the one place your teammates and your AI builder both read to know what "done" looks like. A vague plan produces vague software, so a focused hour here saves you days of confusion later. And remember, the AI is only as clear as the instructions you give it. The PRD is those instructions.

There is a second reason this hour pays off, and it is about you, not just the project. Writing a clear PRD is the core skill of a product manager, and it is the part of the work that survives every change in technology. Tools come and go; the ability to define a real problem, scope it honestly, and say what "good" means is what companies hire for. Do this step well and you have something to talk about in an interview, which we will come back to at the end.

## The mindset: start with the problem, not the solution

The most common mistake on a new project is to start with the solution. Someone says "let's build an app with a recipe feed and tags and a comment section," and the team starts arguing about features before anyone has said what problem those features solve. Strong teams flip the order. They describe the problem first, in the user's words, and only then ask what is the smallest thing that would solve it.

A useful way to think about this is *[Jobs-to-be-Done](../GLOSSARY.md)*: the idea that people "hire" a product to get a specific job done in their life. Nobody wants a recipe app for its own sake. They have a job to do, and they reach for whatever does it. So before you describe a feature, describe the job.

For RecipeRoll, the job is not "browse a recipe feed." The job is closer to this: *"When I'm about to cook and I only have a few ingredients on hand, I want to find a recipe that uses them, so I don't have to shop or give up and order takeout."* Notice that this sentence contains no feature at all. It names a situation, a motivation, and a desired outcome. Once you can say the job that plainly, the feature almost designs itself: search by ingredient. That is problem-first thinking, and it is the habit the rest of this guide is built on.

## What a strong PRD contains

A good PRD is not long, but it has parts that do specific jobs. Here are the building blocks, each in one plain sentence. The numbered steps further down will walk you through producing them.

- **The problem and who has it** — a real, specific person and the pain they feel, written before any solution.
- **The one core outcome** — the single most important thing a person can do, your *[MVP](../GLOSSARY.md)* (minimum viable product), which is the smallest version that is actually useful to a real user.
- **[User stories](../GLOSSARY.md) with [acceptance criteria](../GLOSSARY.md)** — short descriptions of what someone wants, in the form "As a [person], I want [something], so that [reason]," each paired with a testable list of "done when" conditions so you can tell whether it actually works.
- **[Scope](../GLOSSARY.md), set with [MoSCoW](../GLOSSARY.md)** — a sorted list of what is in and what is out, using four buckets: Must have, Should have, Could have, and Won't have yet.
- **A [success metric](../GLOSSARY.md)** — one measurable signal you will actually check, not a vague "it works."
- **[Non-goals](../GLOSSARY.md)** — the things you are deliberately not building, written down so nobody quietly adds them back.

You do not need fancy formatting for any of this. A clear page that hits these six things beats a beautiful ten-page document that hides the decisions.

## What to do

1. **Sit down together.** Get all four teammates in one room or one video call. One person shares their screen and types; everyone talks.
2. **Describe the problem and who has it, before any feature.** Spend ten minutes on the job to be done: what is the person trying to accomplish, in what situation, and why? Write it as a sentence about them, not about your app. Messy notes are fine; the discipline is to stay on the problem and resist jumping to features.
3. **Agree on the one core outcome for v1 (your MVP).** Decide the single most important thing a person should be able to do. This is your MVP: the smallest version that is genuinely useful. Everything else goes on a "Later" list. (*[v1](../GLOSSARY.md)* means "version 1," your first, smallest useful version.)
4. **Turn the core outcome into user stories with acceptance criteria.** For each thing a person can do, write one user story ("As a... I want... so that...") and underneath it a short, testable list of conditions that mean it is done. If you cannot write a "done when" line you could check by hand, the story is still too vague.
5. **Set scope with MoSCoW.** Sort every idea into Must have, Should have, Could have, and Won't have yet. Only the Must haves are v1. This turns a fuzzy "Later" list into honest, named decisions, and it makes your non-goals explicit.
6. **Write one success metric.** Decide the single measurable signal you will check to know v1 worked. Make it something you could observe a stranger doing, with a number in it.
7. **Open the template and fill it in together.** Open [`../templates/PRD-template.md`](../templates/PRD-template.md) and work through it section by section, out loud, as a team.
8. **Let the AI tidy your notes into a clean draft.** Open the prompt in [`../prompts/01-draft-prd.md`](../prompts/01-draft-prd.md), paste your rough notes where it asks, and let your AI builder (Claude Code, Cursor, and the like) turn them into a clean first draft. Here is a short version you can paste:

   ```
   Here are my team's rough notes for an app.
   Turn them into a clear, 1-2 page PRD with these sections:
   the problem and who has it, the one core outcome (MVP),
   user stories with acceptance criteria, scope sorted by
   MoSCoW, one measurable success metric, and explicit
   non-goals. Keep it plain and short. Here are the notes:
   [PASTE YOUR ROUGH NOTES HERE]
   ```

9. **Read it back together and trim.** Keep it to about one to two pages. If a feature is not a Must have for the core outcome, move it down the MoSCoW list.
10. **Save it as `PRD.md` in the repo.** Ask your AI builder to save the file as `PRD.md` at the top level of your project. (A *[repo](../GLOSSARY.md)* is the shared folder that holds your project. See [how git works](../HOW-GIT-WORKS-FOR-NON-CODERS.md).)

## A weak section versus a strong one

The difference between a PRD that helps and one that wastes everyone's time usually comes down to a few sentences. Here is what that looks like in practice.

**A weak success criterion:**

> Search should be fast and easy.

**A strong success metric:**

> A first-time visitor can add a recipe and find it by an ingredient in under 60 seconds, with no help.

The strong one wins because it is testable and unambiguous. "Fast and easy" cannot be checked; two people will disagree about whether you hit it. The strong version names who (a first-time visitor), what (add a recipe, find it by ingredient), and a number you can actually time (under 60 seconds). You could hand it to a stranger and watch.

The same gap shows up in user stories. Here is one without acceptance criteria:

> As a cook, I want to search recipes.

And here is the same story with acceptance criteria:

> As a home cook, I want to search recipes by an ingredient, so that I can cook with what I already have.
>
> Done when:
> - Typing an ingredient shows every recipe that lists it.
> - A search with no matches shows a clear "no recipes found" message, not a blank screen.
> - Search is not case-sensitive: "Egg" and "egg" return the same results.

The second version is something you can build to and test against. The first is a wish. That last "done when" line is exactly the kind of condition that catches real bugs early; it is the case-sensitive search problem Priya found later in testing, which would never have slipped through if it had been written down here.

## How a reviewer reads your PRD

When an experienced product manager picks up a PRD, they are not reading top to bottom. They are scanning for a few quality signals that predict whether the project will go well. Knowing what they look for lets you write to it.

- **Is the user real and specific?** "Home cooks who want to cook with what they have" is reviewable; "users" or "people" is a red flag that nobody pictured an actual person.
- **Is success measurable?** They look for a number or an observable behavior. If success reads like an opinion, they push back.
- **Is scope honestly small, with explicit non-goals?** A short Must-have list and a written list of what you are *not* building signals a team that made real decisions instead of dodging them.
- **Could the work be split among people?** Clear user stories mean Maya, Sam, Priya, and Devin can each pick one up and work in parallel. A vague blob means everyone trips over the same lines of code.

If your PRD answers these four cleanly, it will read as the work of someone who has done this before.

> Tip: A strong PRD is also the best context you can hand your AI builder. The same clarity that lets a reviewer trust it lets the AI build the right thing the first time, instead of guessing and making you redo it. It is also a genuine portfolio piece: being able to point at a crisp problem statement, honest scope, and a measurable goal is exactly what hiring managers want to see. See [Build your portfolio piece](../guides/build-your-portfolio-piece.md) and [Prepare AI-ready deliverables](../guides/prepare-ai-ready-deliverables.md) for how to use it that way.

## Example: RecipeRoll

Here is the team's finished mini-PRD for our running example, RecipeRoll:

> **RecipeRoll — PRD (v1)**
>
> **The problem and who has it:** Home cooks often have a few ingredients on hand and no idea what to make, so they shop again or order takeout. They want to find a recipe that uses what they already have.
>
> **The one core outcome (MVP):** A new visitor can add a recipe and find it again by searching one of its ingredients.
>
> **User stories (Must have):**
> - As a home cook, I want to add a recipe (title, ingredients, steps), so that I can keep it in one place.
> - As a home cook, I want to browse all recipes, so that I can see what's there.
> - As a home cook, I want to search recipes by an ingredient, so that I can cook with what I have.
>   - Done when: typing an ingredient shows every recipe that lists it; no matches shows a clear "no recipes found" message; search is not case-sensitive.
>
> **Scope (MoSCoW):** Must: add, browse, search by ingredient. Should: nothing for v1. Could: nothing for v1. Won't have yet: user accounts and login, photos, ratings, comments.
>
> **Non-goals:** No accounts, no photos, no ratings, no comments in v1.
>
> **Success metric:** A first-time visitor can add a recipe and find it by an ingredient in under 60 seconds, with no help.
>
> **Logged decision:** v1 allows two recipes to have the same name. We accept possible duplicates to keep v1 simple.

Notice how short it is. Anyone on the team can read it in under a minute and picture the same app. Notice also that the logged decision about duplicate names is written down: when a small choice like that lives in the PRD, nobody relitigates it later, and the AI builder does not have to guess.

## Watch out for

- **Starting with the solution.** If your notes name features before they name the person and their problem, stop and write the job to be done first. The feature list is the easy part; the problem is the part that makes the feature list correct.
- **Cramming everything into v1.** It is tempting to make login, photos, and ratings all Must haves. Don't. If it is not part of the one core outcome, sort it below Must have in MoSCoW and move on. A small v1 that ships beats a big v1 that never does.
- **Unmeasurable success.** "Fast and easy," "intuitive," "delightful" — if you cannot check it by watching a stranger, it is not a success metric. Rewrite it with a who, a what, and a number.
- **Writing it so only one person understands it.** If only the person typing knows what a line means, the AI and your teammates will guess, and they will guess differently. Read each section aloud and make sure all four of you agree.

## Say it like a pro

These are the words product people use every day. Knowing them, and being able to give the one-line meaning in an interview, signals that you have done the work. Full definitions live in the [glossary](../GLOSSARY.md).

- **PRD** — the short document that says what you are building and why.
- **MVP** — the smallest version that is actually useful to a real user.
- **Scope** — what is in the build and what is out, decided on purpose.
- **Non-goal** — something you are deliberately not building, written down.
- **Acceptance criteria** — the testable "done when" conditions for a feature.
- **Success metric** — the one measurable signal you check to know it worked.

## You're done when

- [ ] Every teammate can say, in one sentence, the problem you are solving and who has it.
- [ ] The one core outcome (your MVP) is written down.
- [ ] Each thing a person can do has a user story with at least one testable acceptance criterion.
- [ ] Scope is sorted with MoSCoW, and the non-goals are written out explicitly.
- [ ] There is one measurable success metric everyone agrees on.
- [ ] The document is saved as `PRD.md` in your repo.

## Next

Now that you have a first draft, pressure-test it before you build: [Step 2: Review the PRD](step-2-review-the-prd.md).

## Prompts and templates

- [`../templates/PRD-template.md`](../templates/PRD-template.md) — the blank PRD you fill in together.
- [`../prompts/01-draft-prd.md`](../prompts/01-draft-prd.md) — turns your rough notes into a clean draft.
