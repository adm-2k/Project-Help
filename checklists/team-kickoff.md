# Team Kickoff Checklist

> A one-time setup list to run together before your team writes a single line of anything.

Goal: get every person and every document ready so building can start smoothly. Time: about 60 to 90 minutes together. Who: the whole team.

A calm start prevents most of the confusion that hits teams later. An hour now to agree on tools, rules, and who does what means nobody gets lost, stuck, or stepping on a teammate's work. Tick these off together, out loud, so everyone shares the same picture.

> Tip: Do this on a call or in the same room, with the [README](../README.md) open on a shared screen. Read each item aloud, and only check it when everyone agrees.

## Get everyone on the same page

- [ ] Everyone has read the [README](../README.md) and skimmed the [GLOSSARY](../GLOSSARY.md), so the words ahead won't feel scary
- [ ] You agreed, in a sentence or two, what problem you're solving and who it's for
- [ ] You read the [example walkthrough](../examples/EXAMPLE-walkthrough.md) together, so everyone has seen the whole journey once

## Set up your tools

- [ ] You created (or got access to) the team's GitHub repository, and every person can push to it
- [ ] You agreed on the AI builder tool everyone will use (Claude Code, Cursor, and the like). Pick one, so help is easy to share
- [ ] Everyone installed a visual git tool such as GitHub Desktop, or knows how to use the git buttons built into their AI builder

> Watch out: Don't skip the "everyone can push" check. The fastest way to lose an afternoon is discovering halfway through that one teammate has no access to the repo.

## Agree how you'll work together

- [ ] You picked a coordinator for the week. This can rotate weekly; it's a light role, not a boss
- [ ] You agreed on a communication channel (chat, and so on) and a weekly sync time
- [ ] You agreed on the branch-naming convention, `feature/short-description` (lowercase words separated by dashes), for example `feature/add-recipe-form`
- [ ] You agreed on the two golden rules and said them out loud:
  - `main` always works (never break the shared, working version)
  - one owner per task (no two people building the same thing at once)

## Write your starting documents

- [ ] You wrote your PRD together, following [Step 1: Write the PRD](../guides/step-1-write-the-prd.md)
- [ ] You reviewed that PRD as a team, following [Step 2: Review the PRD](../guides/step-2-review-the-prd.md)
- [ ] You set up your working docs by copying these templates into your repo:
  - your finished PRD (from Step 1)
  - [task board](../templates/task-board.md)
  - [ROADMAP](../templates/ROADMAP.md)
  - [ISSUE-LOG](../templates/ISSUE-LOG.md)
  - [DECISIONS](../templates/DECISIONS.md)

## RecipeRoll example

The four-person RecipeRoll team spent one call doing exactly this. They confirmed the pitch, "A friendly place to save your recipes and discover your friends'," and what v1 means: add a recipe, browse all recipes, search by ingredient. They named Maya the first coordinator, agreed to sync every Tuesday, and picked branch names like `feature/add-recipe-form` and `feature/recipe-list`. Then they copied in the five working docs and were ready to break the work into tasks.

## You're done when

- [ ] Every box above is checked and everyone agreed to each one

When all boxes are checked, go to [Step 3: Break into tasks](../guides/step-3-break-into-tasks.md).
