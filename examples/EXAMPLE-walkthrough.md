# RecipeRoll: The Whole Journey, Start to Finish

> Follow one small team through all seven steps once, so you can see how every piece connects before you try it yourself.

This is a story. Maya, Sam, Priya, and Devin are four friends who can use a computer but have never written code or touched [git](../GLOSSARY.md). They want to build **RecipeRoll**, "a friendly place to save your recipes and discover your friends'." Watch what they do, and you'll have a map for your own team.

Each step below has its own detailed guide. This page is the view from above: short, concrete, and complete. When a step catches your interest, click through to its full guide.

---

## Step 1: Write the PRD

The team sat down together for 30 minutes and asked their AI builder (Claude Code, Cursor, or similar) to help them write a short plan. A *PRD* ([product requirements document](../GLOSSARY.md)) is a one-page document that says what you're building and why.

Full guide: [Step 1: Write the PRD](../guides/step-1-write-the-prd.md)

Here's the mini-PRD they produced:

> **RecipeRoll — Product Requirements (v1)**
>
> **Pitch:** A friendly place to save your recipes and discover your friends'.
>
> **Who it's for:** Home cooks who want their recipes in one place and want to find new ones by ingredient.
>
> **v1 scope (the MVP):**
> - Add a recipe (title, ingredients, steps)
> - Browse all recipes
> - Search by ingredient
>
> **Out of scope for now (Later):** user accounts and login, photos, ratings, comments.
>
> **Success looks like:** A new visitor can add a recipe and then find it by searching one of its ingredients, in under a minute, without help.

Writing the scope down, including what they were *not* building, kept the team from arguing about it later. "Later" is a promise, not a no.

---

## Step 2: Review the PRD

One person read the PRD slowly and used the AI to stress-test it: "What's unclear? What could go wrong?" The AI came back with a sharp question the team had to answer.

Full guide: [Step 2: Review the PRD](../guides/step-2-review-the-prd.md)

> **Review note (from the AI's stress-test):**
> "What happens if two recipes have the same name, like two different 'Banana Bread' entries?"

The team talked it through and made a call, then wrote it into their [decisions log](../templates/DECISIONS.md):

> **Decision:** v1 allows duplicate recipe names. Keep it simple; revisit if it becomes confusing.
> **Decided by:** the team — **Date:** day 1

A logged decision means nobody re-litigates it in week three. The reasoning is right there for anyone who asks.

---

## Step 3: Break the work into branch-sized tasks

The team asked the AI to split the v1 scope into independent pieces, one per person, so nobody would step on anyone else's work. Each piece gets its own *[branch](../GLOSSARY.md)*: a safe, separate copy of the project to work in.

Full guide: [Step 3: Break into tasks](../guides/step-3-break-into-tasks.md)

Here's their [task board](../templates/task-board.md):

| Feature | Owner | Branch | Status |
|---|---|---|---|
| A — Add a recipe form | Maya | `feature/add-recipe-form` | To do |
| B — Browse all recipes list | Sam | `feature/recipe-list` | To do |
| C — Search by ingredient | Priya | `feature/search-by-ingredient` | To do |
| D — Save favorites | Devin | `feature/favorites` | To do |

Four owners, four branches, four lanes. Because each person works in a separate branch, all four can build at the same time without overwriting each other.

---

## Step 4: Claim a task and build it

Maya took Feature A. She created her branch and described the form to the AI in plain English. The AI wrote the code, Maya checked it in the running app, and she saved her progress in small chunks.

Full guide: [Step 4: Claim and build](../guides/step-4-claim-and-build.md)

She made her branch using her AI tool's built-in git button. The command underneath is shown for reference:

```
git checkout -b feature/add-recipe-form
```

Then she built the form bit by bit, saving each working piece as a *[commit](../GLOSSARY.md)*: a labeled snapshot of the project at that moment. Her commit messages:

```
Add recipe form with title, ingredients, and steps fields
```

```
Show a thank-you message after a recipe is saved
```

> Tip: Small commits are like save points in a game. If something breaks, Maya can go back to the last good one, so she doesn't have to get it perfect in one go.

---

## Step 5: Open a pull request

When Maya's form worked, she opened a *[pull request](../GLOSSARY.md)*, or PR: a polite request to add her work to the team's main copy. She filled in the [PR template](../.github/PULL_REQUEST_TEMPLATE.md).

Full guide: [Step 5: Open a pull request](../guides/step-5-open-a-pull-request.md)

> **What does this do?**
> Adds the "Add a recipe" form. You can type a title, ingredients, and steps, then save the recipe.
>
> **Why?**
> First piece of v1. Without it, there's nothing to browse or search.
>
> **How to test it:**
> 1. Open the app.
> 2. Click "Add a recipe".
> 3. Fill in a title, ingredients, and steps, then save.
> 4. You should see a thank-you message.
>
> **Anything reviewers should know:**
> Saving works; I haven't styled it yet. Allows duplicate names on purpose (see decisions log).
>
> **Branch:** `feature/add-recipe-form`

A clear PR description tells the reviewer exactly how to check the work in two minutes. Think of it as a gift to whoever reviews it.

---

## Step 6: Review and merge

Sam reviewed Maya's PR. He followed the test steps, confirmed it worked, left a friendly comment, and approved it. Then the team *[merged](../GLOSSARY.md)* it into the main copy.

Full guide: [Step 6: Review and merge](../guides/step-6-review-and-merge.md)

> **Sam's review comment:**
> "Tested it. I added a 'Tomato Soup' recipe and the thank-you message popped up. Works great, approving."

After approval, Maya clicked `Merge`, then deleted her branch. The work was safely in `main` now, so the branch had done its job:

```
git branch -d feature/add-recipe-form
```

Everyone else then **pulled** the latest `main` into their own work, so they were building on top of Maya's form:

```
git pull
```

Merging is how one person's finished work becomes everyone's starting point. Pulling regularly keeps the whole team in sync and prevents painful surprises later.

---

## Step 7: Update the roadmap and log issues

With Feature A merged, the team kept their shared docs honest. They moved "Add a recipe" to Done on the [roadmap](../templates/ROADMAP.md), and Priya, who was testing search, found a small bug and logged it.

Full guide: [Step 7: Update the roadmap and log issues](../guides/step-7-update-roadmap-and-log-issues.md)

**Roadmap, updated:**

| Feature | Status |
|---|---|
| Add a recipe | Done |
| Browse all recipes | In progress |
| Search by ingredient | In progress |
| Save favorites | To do |

Priya logged the bug in the [issue log](../templates/ISSUE-LOG.md):

> **Bug:** Search is case-sensitive, so typing "Tomato" misses "tomato."
> **Found by:** Priya — **Severity:** small — **Status:** open

And the team recorded the follow-up decision in the [decisions log](../templates/DECISIONS.md):

> **Decision:** Search should ignore upper/lower case before v1 ships. Track via the bug above.
> **Decided by:** the team

A roadmap that matches reality and a tidy issue log mean anyone can glance at them and know exactly where things stand. Nothing lives only in someone's head.

---

## Now it's your turn

That's the whole loop. Maya, Sam, Priya, and Devin will repeat Steps 4 through 7 for each remaining feature until v1 is done. Notice that nobody had to be a programmer. They described what they wanted, the AI built it, and git kept everyone's work safe and separate.

You can do exactly this.

- Start here: [Step 1: Write the PRD](../guides/step-1-write-the-prd.md)
- See the full map of every step and tool: [the README](../README.md)

> Remember: You will make mistakes, and that is completely fine. Branches and commits exist precisely so that mistakes stay cheap and easy to undo. Take the first step.
