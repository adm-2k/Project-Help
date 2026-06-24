# PRD Template

A _PRD_ is a Product Requirements Document: a short, shared description of what you're building and why. See [the glossary](../GLOSSARY.md) if a word here is new to you.

**How to use this template**

1. Copy everything below the line into a new file called `PRD.md` in your project's [repository](../GLOSSARY.md), the shared folder your team works from.
2. Fill it in together. One person types while everyone talks.
3. Keep it short. One to two pages when you're done is plenty.
4. Each section has an _italic instruction_ telling you what to write, plus a quoted RecipeRoll example showing one good answer.
5. As you fill in a section, delete the italic instruction and replace the example with your own answer.

> Tip: Don't aim for perfect. Aim for clear enough that a teammate could explain it back to you. You'll tighten it in the next step.

---

# [Product name] — Product Requirements Document

## 1. Product name and one-line pitch

_Write your product's name and one friendly sentence that says what it is._

> **RecipeRoll** — A friendly place to save your recipes and discover your friends'.

## 2. The problem and who has it

_Describe the problem in plain words, and name the real people who have it. Write for someone specific, not "everyone."_

> Home cooks keep their recipes scattered across notebooks, screenshots, and bookmarks, so they can never find the one they want. They also have no easy way to see what their friends are cooking. The users are home cooks who want their recipes in one place and want to find new ones by ingredient.

## 3. Why this, why now

_Two or three sentences on why this is worth building and why now is a good time._

> The people we know cook at home more than they used to, and they keep asking each other to "send me that recipe." There's no simple, shared place to do that. We can build a useful first version quickly, so now is a good time to start.

## 4. The one core outcome for v1

_Name the single most important thing a user can do in your first version. Just one. If you name two, pick the one you'd keep if you could only ship one._

> A home cook can add a recipe and find it again later by searching one of its ingredients.

## 5. In scope for v1 (must-have features)

_List only the features your first version truly needs. Keep them to short bullets. If a bullet could be cut and still leave a useful product, cut it._

> - Add a recipe (title, ingredients, steps)
> - Browse all recipes
> - Search by ingredient

## 6. Out of scope (non-goals)

_List what you are deliberately not building yet. Writing these down is what keeps v1 small, so don't skip it._

> - User accounts and login
> - Photos of dishes
> - Ratings
> - Comments

## 7. User stories

_Write a few short stories in the form: As a [user], I want [thing], so that [benefit]._

> - As a home cook, I want to add a recipe with its ingredients and steps, so that I never lose it.
> - As a home cook, I want to browse all the recipes, so that I can get ideas for dinner.
> - As a home cook, I want to search by ingredient, so that I can use up what's in my fridge.

## 8. Key screens or flows (in plain words)

_Describe the main pages or steps a user moves through. No design needed, just words._

> - **Add a recipe:** a form with title, ingredients, and steps, plus a `Save` button.
> - **Browse all recipes:** a list page showing every saved recipe by title.
> - **Search by ingredient:** a search box; typing an ingredient shows matching recipes.

## 9. Success criteria (concrete and measurable)

_Describe how you'll know v1 works. Make it something you can actually sit down and check._

> A new visitor can add a recipe and then find it by searching one of its ingredients, in under a minute, without help.

## 10. Constraints and assumptions

_Note anything you're assuming, and any limits you have to work within: time, team size, tools._

> - A team of four, each owning one feature.
> - We have a few weeks of part-time work.
> - We're using an AI builder (Claude Code, Cursor, and the like) and don't need a database expert.
> - We assume recipes are short text, with no photos in v1.

## 11. Open questions

_List anything you haven't decided yet. It's fine to leave these open for now._

> - Should we allow two recipes with the same name? (Leaning yes for v1 to keep it simple.)
> - Do we need to handle very long ingredient lists?
> - What should a user see when a search returns no results?

---

## Next

- Review this PRD before building: [Step 2: Review the PRD](../guides/step-2-review-the-prd.md)
- Want the AI to draft it for you first? Use [the draft-PRD prompt](../prompts/01-draft-prd.md)
