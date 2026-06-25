# PRD Template

A _[PRD](../GLOSSARY.md)_ is a Product Requirements Document: a short, shared description of what you're building and why. See [the glossary](../GLOSSARY.md) if a word here is new to you.

**How to use this template**

1. Copy everything below the line into a new file called `PRD.md` in your project's _[repository](../GLOSSARY.md)_, the shared folder your team works from.
2. Fill it in together. One person types while everyone talks.
3. Keep it short. One to two pages when you're done is plenty.
4. Each section has an _italic instruction_ telling you what to write, plus a quoted RecipeRoll example showing one good answer.
5. As you fill in a section, delete the italic instruction and replace the example with your own answer.
6. Each section also has a one-line `_What reviewers look for:_` note. That's the quality bar a real product team would hold you to. Read it before you move on.

> Tip: Don't aim for perfect. Aim for clear enough that a teammate could explain it back to you. You'll tighten it in the next step.

---

# [Product name] — Product Requirements Document

_Fill in this short header first. The status and version lines aren't busywork: they tell a teammate at a glance whether this document is safe to build from yet, and which version they're looking at when two copies disagree. That's what makes it read like a real product document instead of a draft someone abandoned._

- **Product:** [name] — [one-line pitch]
- **Author(s):** [who wrote and owns this]
- **Date:** [last updated]
- **Status:** Draft / Reviewed / Locked _(Draft = still changing; Reviewed = team has read and agreed; Locked = build from this)_
- **Version:** [v0.1, v1.0, and so on]

> **Product:** RecipeRoll — A friendly place to save your recipes and discover your friends'.
> **Author(s):** Maya (with Sam, Priya, Devin)
> **Date:** 2026-06-24
> **Status:** Draft
> **Version:** v0.1

## 1. Problem and context

_Name the specific person who has the problem, describe the pain in their own words, and say why now is the time to solve it. Include any evidence you have, even informal: a conversation, a search you keep repeating, a workaround you keep doing._

> Home cooks keep their recipes scattered across notebooks, screenshots, and browser bookmarks. When it's time to cook, they can't find the one they want: "I know I saved that soup somewhere." They also have no simple way to see what friends are cooking, so the same text goes out over and over: "send me that recipe again?" Why now: the four of us cook at home more than we used to, and we've each sent or begged for a recipe by text in the last month. There's no shared, searchable place to keep them, and we can build a useful first version quickly.

_What reviewers look for:_ a specific user and a real pain in their words, not "everyone has trouble with recipes."

## 2. Goals and success metrics

_Write 1 to 3 goals. Give each one a measurable signal you can actually sit down and check, with a number or a clear yes/no condition. A goal without a checkable signal is just a wish._

> 1. **Cooks can save a recipe and get it back.** Signal: a first-time visitor adds a recipe and finds it again by an ingredient in under 60 seconds, without help.
> 2. **The library is worth browsing.** Signal: by launch, at least 15 real recipes are in it, added by the four of us.
> 3. **Search actually finds things.** Signal: searching a known ingredient returns every recipe that lists it, every time (see the case-sensitive bug in Open questions).

_What reviewers look for:_ each goal has a number or a checkable yes/no condition, not a vague "users will be happy."

## 3. Non-goals

_List what you are deliberately not building yet. Saying no on purpose is what keeps v1 small enough to finish._

> - User accounts and login
> - Photos of dishes
> - Ratings
> - Comments

_What reviewers look for:_ you said no on purpose. Deciding what not to build is a senior move, not a gap.

## 4. Target users and primary use cases

_Name the main people who will use this, and the main things they come to do. Keep it to the people you're actually building for in v1._

> **Primary user: the home cook.** Someone who already cooks and keeps recipes, just badly scattered. They come to RecipeRoll to:
> - Save a recipe they want to keep (paste in title, ingredients, steps).
> - Browse the library when they don't know what to make.
> - Find a recipe by an ingredient they have on hand or remember.

_What reviewers look for:_ a clear primary user and the few real jobs they show up to do, not a list of everyone who might wander by.

## 5. User stories with acceptance criteria

_Write a few short stories in the form: As a [user], I want [thing], so that [benefit]. Under each, list 1 to 3 "Done when ..." conditions. These are your _[acceptance criteria](../GLOSSARY.md)_: testable checks that say the story is truly finished._

> **As a home cook, I want to add a recipe with its title, ingredients, and steps, so that I never lose it.**
> - Done when: I can open an add-a-recipe form, type a title, ingredients, and steps, and press `Save`.
> - Done when: after saving, the new recipe appears in the browse-all list by its title.
> - Done when: the recipe still appears after I close and reopen the app.
>
> **As a home cook, I want to browse all the recipes, so that I can get ideas for dinner.**
> - Done when: the browse page lists every saved recipe by title.
> - Done when: opening a recipe shows its full ingredients and steps.
>
> **As a home cook, I want to search by an ingredient, so that I can use up what's in my fridge.**
> - Done when: typing an ingredient shows every recipe that lists it.
> - Done when: a search with no matches shows a clear "no recipes found" message, not a blank page.

_What reviewers look for:_ each "Done when" is something you could actually test by hand, not a vague hope like "works well."

## 6. Scope for v1 (MoSCoW)

_Sort your features into the four _MoSCoW_ buckets below: Must have, Should have (later), Could have (someday), Won't do yet. The Must column is your real v1. Everything in it has to ship for the product to make sense._

> | Must have (v1) | Should have (later) | Could have (someday) | Won't do yet |
> | --- | --- | --- | --- |
> | Add a recipe (title, ingredients, steps) | Edit a saved recipe | Tags or categories | User accounts and login |
> | Browse all recipes | Delete a recipe | Sort by newest | Photos of dishes |
> | Search by ingredient | Case-insensitive search | Share a recipe by link | Ratings and comments |

_What reviewers look for:_ the Must column is genuinely minimal. If you can cut a Must and still have a useful product, it wasn't a Must.

## 7. Key flows or screens

_Describe the main pages or steps a user moves through, in plain words. No design needed._

> - **Add a recipe:** a form with fields for title, ingredients, and steps, plus a `Save` button. After saving, the cook lands back on the browse list and sees their new recipe.
> - **Browse all recipes:** a list page showing every saved recipe by title. Clicking a title opens the full recipe.
> - **Search by ingredient:** a search box at the top of the browse page. Typing an ingredient filters the list to recipes that include it; clearing the box shows everything again.

_What reviewers look for:_ a teammate could walk through each flow out loud without needing a mockup.

## 8. Assumptions, dependencies, and risks

_Note what you're assuming is true, what you depend on to build this, and what could go wrong. Naming a risk early is cheaper than discovering it late._

> - **Assumptions:** recipes are short text (no photos in v1); the four of us can seed the first 15 recipes; cooks are fine typing or pasting a recipe in.
> - **Dependencies:** an AI builder (Claude Code, Cursor, and the like) so we don't need a database expert; a few weeks of part-time work from a team of four, each owning one feature.
> - **Risks:** search misses recipes because of the case-sensitive bug (see Open questions); duplicate recipe names could confuse the browse list; if no one seeds recipes, the library looks empty at launch.

_What reviewers look for:_ at least one honest risk that could actually sink v1, with a hint of how you'd handle it.

## 9. Open questions

_List decisions you haven't made yet. It's fine to leave these open, as long as they're written down where the team and the AI can see them._

> - **Duplicate recipe names:** should we allow two recipes with the same title? Leaning yes for v1 to keep it simple, even though it makes the browse list slightly harder to scan.
> - **Case-sensitive search:** right now searching "Onion" misses a recipe that lists "onion." Do we fix this for v1 (treat it as a Should-have we promote) or ship with the known limitation noted?
> - **Empty search:** what exactly should a cook see when a search returns no results?

_What reviewers look for:_ the open questions are real forks in the road, and each names who or what the decision waits on.

## 10. Definition of done

_Describe how you'll know v1 is ready to put in front of real people. This is your finish line: when every box here is true, you ship._

> v1 is done when:
> - All three Must-have features work end to end: add, browse, search.
> - The success metric in Goal 1 passes: a first-time visitor adds a recipe and finds it by an ingredient in under 60 seconds, with no help from us.
> - At least 15 real recipes are seeded so the library isn't empty.
> - Every open question above has either an answer or a written, agreed-upon "ship without it for now."

_What reviewers look for:_ a finish line you could check in one sitting, tied back to your goals, not "when it feels ready."

---

When this PRD is filled in, it does double duty. It becomes the core of your _AI context file_, the document your AI builder reads so it aims at the same goal you do ([prepare AI-ready deliverables](../guides/prepare-ai-ready-deliverables.md)). And it becomes the backbone of your portfolio case study, the story of what you built and why ([build your portfolio piece](../guides/build-your-portfolio-piece.md)). Write it once, well, and you get all three.

## Next

- Review this PRD before building: [Step 2: Review the PRD](../guides/step-2-review-the-prd.md)
- Want the AI to draft it for you first? Use [the draft-PRD prompt](../prompts/01-draft-prd.md)
