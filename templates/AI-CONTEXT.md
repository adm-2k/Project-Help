# AI Context Template

> A one-page brief that tells any AI builder how to work on your project, so every teammate's tool follows the same plan and the same rules.

This file is the short note every AI tool reads before it touches your project. It points at the full plan in `PRD.md` and lays out the house rules so the AI does not have to guess.

**Where to save it.** Put it in the root of your *project* repo (the app you are building, not this playbook), under the filename your AI builder reads automatically:

| Tool | Filename it reads |
| --- | --- |
| Claude Code | `CLAUDE.md` |
| Many AI tools (open convention) | `AGENTS.md` |
| Cursor | `.cursor/rules/*.mdc` (newer) or a legacy `.cursorrules` file |

If your team uses more than one tool, save the same content under more than one filename. Keep them identical. You can also ask your AI builder to write these files for you, using the prompt in [../prompts/11-build-ai-context-from-prd.md](../prompts/11-build-ai-context-from-prd.md).

**How to fill it in.** Each section has an _italic instruction_ and a quoted RecipeRoll example. Replace both with your own answer, and keep the whole file to about one page.

---

## Project in one sentence

_Say what the app is, in one friendly sentence._

> RecipeRoll is a web app where a small group of friends save their recipes and browse one another's.

## The full plan

_Point to the complete plan so the AI reads it before building._

> The full product plan is in `PRD.md` in the repo root. Read it before starting any task.

## Who it is for and the v1 goal

_Say who uses it and what "version one" must do, nothing more._

> For home cooks who want one shared recipe box. v1 lets a person add a recipe, browse all recipes, search by ingredient, and save favorites. Everything else is Later.

## Where things live

_List the files that hold the plan, the work, and the decisions._

> - `PRD.md` — the full plan.
> - The task board — who owns what and which branch they are on.
> - `DECISIONS.md` — choices we have locked, and why.
> - `specs/` — one short spec per feature.

## House rules for the AI

_Set the rules the AI should follow on every task. Keep these tight._

> - Build only the one task or feature spec you are given. Nothing extra.
> - Do not change files that are unrelated to your task.
> - Keep changes small and easy to review.
> - Match the existing code and writing style; do not reformat the whole file.
> - Use the branch name listed for this task on the task board.
> - Ask before any big choice (a new tool, a data change, a new dependency).
> - Write your change so it merges cleanly with what teammates are building.

## Tech and tool choices

_Point to where the team records its tool and technology decisions._

> Our locked tool and technology choices are in `DECISIONS.md`. Follow them. Do not introduce a new framework, library, or service without asking first.

## Project words and what they mean

_Define the few terms unique to this project, so the AI uses them correctly._

> - **Recipe** — a saved entry with a title, ingredients, and steps.
> - **Favorite** — a recipe a user has marked to find again quickly.
> - **Duplicate names are allowed** in v1; two recipes may share a title (see `DECISIONS.md`).

---

For how this file fits into the workflow, see [../guides/prepare-ai-ready-deliverables.md](../guides/prepare-ai-ready-deliverables.md).
