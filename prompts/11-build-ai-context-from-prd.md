# Prompt 11 — Build Your AI Context and Feature Specs From the PRD

> Have the AI turn your reviewed plan into one context file every AI tool can read, plus one short spec per feature, so nobody's AI builder drifts off the plan.

When to use: Right after your PRD is reviewed and locked, and before you split the work into tasks. This is the companion guide between Step 2 and Step 3.

## Before you start

- Have your reviewed [PRD](../templates/PRD-template.md) ready to paste.
- Know which AI tool each teammate uses, so you save the context file under the right filename (`CLAUDE.md`, `AGENTS.md`, or Cursor rules).
- Open the two templates so you can compare the AI's draft against them: the [AI context template](../templates/AI-CONTEXT.md) and the [feature spec template](../templates/feature-spec.md).

The *AI context file* is the short brief every AI builder reads before working. A *feature spec* is a one-page description of a single feature. See the [glossary](../GLOSSARY.md) if a word here is new.

## The prompt

Copy this, replace the `[BRACKETED PARTS]`, and paste it into your AI builder.

```
You are an experienced product manager helping a non-technical team get their
plan ready for AI builders. I will paste our reviewed PRD. Produce two things,
in plain English, so that any AI coding tool can read them and stay on plan.

Here is our reviewed PRD:
[PASTE YOUR REVIEWED PRD HERE]

We use these AI tools: [LIST YOUR TOOLS, e.g. Claude Code and Cursor].

FIRST, produce an AI CONTEXT FILE, about one page, with these sections:
- Project in one sentence
- The full plan (point to PRD.md)
- Who it is for and the v1 goal
- Where things live (PRD.md, the task board, DECISIONS.md, specs/)
- House rules for the AI: build only the task or feature spec it is given;
  do not change unrelated files; keep changes small; match the existing style;
  follow the branch name from the task board; ask before any big choice;
  write so the change merges cleanly
- Tech and tool choices (point to DECISIONS.md)
- Project words and what they mean

SECOND, produce ONE SHORT FEATURE SPEC per feature in the v1 scope. Each spec
should have: feature name; a one-line user story (As a ___ I want ___ so that
___); in scope; out of scope; the files or areas it will likely touch; a few
checkable "done when" criteria; and which PRD section it comes from.

After the specs, add a short "Overlaps" note: flag any two features that will
likely touch the SAME files, and say which one should probably go first.

Keep everything simple and friendly. This is for a non-technical team.
```

## Tips

- Save the context file in your project repo under the filename your tool reads: `CLAUDE.md` for Claude Code, `AGENTS.md` for tools that follow the open convention, or `.cursor/rules/*.mdc` (or a legacy `.cursorrules` file) for Cursor. Same content, different filename.
- Save each feature spec into a `specs/` folder, named after the feature, like `specs/add-recipe-form.md`.
- The AI's draft is a starting point. Read it over together and fix anything it guessed wrong before anyone builds on it.
- When your scope changes later, update `PRD.md` and the context file in the same sitting so they never disagree.

## What good output looks like

- A one-page context file that points back to `PRD.md` instead of repeating the whole plan.
- One spec per v1 feature, each naming the files it will likely touch.
- An "Overlaps" note that flags features touching the same files and suggests an order.

### RecipeRoll example

For RecipeRoll, the AI returns a context file that opens "RecipeRoll is a web app where friends save and browse recipes; the full plan is in `PRD.md`," followed by the house rules and the project words. Then it returns four specs, one each for Add a recipe, Browse, Search, and Favorites. Its Overlaps note reads:

```
Overlaps: "Search by ingredient" and "Browse all recipes" both touch the browse
page. Build Browse first, then add Search on top, so they don't edit the same
file at once.
```

> Watch out: Do not let the context file become a second copy of the plan. It is a short pointer to `PRD.md`. If the two ever disagree, your AIs have a reason to drift.

## Next

Save these files in your project repo, then split the work in [Step 3: Break into tasks](../guides/step-3-break-into-tasks.md). For the full walkthrough, see [Turn your PRD into a shared source of truth](../guides/prepare-ai-ready-deliverables.md).

## Templates this prompt fills

- [../templates/AI-CONTEXT.md](../templates/AI-CONTEXT.md) — the AI context file you save as `CLAUDE.md`, `AGENTS.md`, or Cursor rules.
- [../templates/feature-spec.md](../templates/feature-spec.md) — one short spec per feature, kept in `specs/`.
