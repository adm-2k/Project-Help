# Turn Your PRD Into a Shared Source of Truth

> Save one plan that every teammate and every AI tool reads the same way, so nobody's AI builder wanders off and builds something different.

**Goal:** Turn your reviewed PRD into a small set of files every teammate and every AI tool points at. · **Time:** 30 to 45 minutes · **Who:** The whole team, together, with your AI builder.

## Why it matters

You reviewed and locked your PRD in [Step 2](step-2-review-the-prd.md). But right now that plan lives in one place and your teammates are about to scatter, each opening their own *AI builder* ([AI builder](../GLOSSARY.md) like Claude Code or Cursor) to work on their own piece.

Here is the trap. When four people prompt four AI tools, and each one feeds the AI a slightly different summary of the plan, the AIs drift. One builds a recipe form that requires a photo; another builds a browse page that assumes photos never exist. Each tool was "right" about the scraps it was given. None of them saw the same whole picture. You only find out when the pieces refuse to fit.

The fix is plain: one canonical plan, and every teammate in every tool points their AI at the exact same files. Not five summaries. One source of truth. This guide turns your locked PRD into the small set of files that makes that happen, before anyone splits the work into tasks.

## What to do

1. **Save the reviewed PRD as `PRD.md` at the top of your project repo.** This is the project the team is building, not this playbook. Put `PRD.md` in the root of that repo so it sits next to the code and gets versioned alongside it. This file is the full plan. Everything else points back to it.

2. **Create an AI context file and save it under the name your tool reads.** Copy [../templates/AI-CONTEXT.md](../templates/AI-CONTEXT.md), fill it in, and save it in your project repo under the filename your AI builder looks for automatically:

   | Tool | Filename it reads |
   | --- | --- |
   | Claude Code | `CLAUDE.md` in the repo root |
   | Many AI tools (open convention) | `AGENTS.md` in the repo root |
   | Cursor | `.cursor/rules/*.mdc` (newer) or a legacy `.cursorrules` file |

   The content is the same; only the filename differs. If your team uses more than one tool, keep the same content in more than one filename, for example a `CLAUDE.md` and an `AGENTS.md` that say the identical thing. You can even ask your AI builder to write these files for you, which is what the prompt in step 4 does.

3. **Write one short feature spec per planned feature.** For each feature in your v1, copy [../templates/feature-spec.md](../templates/feature-spec.md), fill it in, and save it in a `specs/` folder in your project repo (for example `specs/add-recipe-form.md`). A spec is a one-page description of a single feature: what it does, what is in and out of scope, and which files it will touch. It is the close-up that `PRD.md` is too high-level to give.

4. **Have the AI draft all of this from the PRD, then read it over together.** Use [../prompts/11-build-ai-context-from-prd.md](../prompts/11-build-ai-context-from-prd.md). Paste in your reviewed PRD and the AI produces a first draft of the context file and one feature spec per feature. The draft is a starting point, not the finished article. Read every line out loud as a team and correct anything the AI guessed wrong.

5. **From now on, everyone points their AI at these same files.** Whatever tool a teammate opens, the first move is the same: make sure the AI is reading `PRD.md`, the context file, and the relevant feature spec. Same plan, same words, every tool, every person. That is what keeps four AI builders building one app.

## Example: RecipeRoll

The RecipeRoll team saves their reviewed plan as `PRD.md`. Then they create their AI context file from the template and save it as both `CLAUDE.md` and `AGENTS.md`, since Maya uses Claude Code and Sam uses a tool that reads `AGENTS.md`. In brief, it says:

```
RecipeRoll is a friendly web app for saving recipes and browsing your friends'.
The full plan is in PRD.md. v1 is for home cooks who want one shared recipe box.
Where things live: PRD.md (the plan), the task board, DECISIONS.md, specs/.
House rules: build only the task you are given, keep changes small, follow the
branch name from the task board, and ask before any big choice.
v1 allows duplicate recipe names (see DECISIONS.md).
```

Then they write one spec per feature into `specs/`. The add-recipe spec, in brief:

```
Feature: Add a recipe form
Owner: Maya · Branch: feature/add-recipe-form
What it does: a cook fills in title, ingredients, and steps, and saves the recipe.
In scope: the form and saving. Out of scope: photos, ratings (both Later).
Touches: add-recipe.html, add-recipe.js, the shared recipes data.
Done when: a new recipe appears in the browse list after saving.
```

Now when Maya opens Claude Code and Sam opens his tool, both AIs read the same plan, the same rules, and the same specs. They are far less likely to drift apart.

## Watch out for

- **Letting the PRD and the context file drift apart.** The context file is a short pointer to `PRD.md`, not a second copy of the plan. If you change the scope, update both in the same sitting so they never disagree.
- **Five sources of truth instead of one.** It is fine to save the same content under `CLAUDE.md` and `AGENTS.md`, but they must say the identical thing. The moment two files disagree, your AIs have a reason to drift again.
- **Treating the AI's draft as final.** The AI guesses. Read its draft together and fix what it got wrong before anyone builds on it.

## Next

Now that every teammate and every tool shares one plan, slice it into branch-sized tasks: [Step 3: Break into tasks](step-3-break-into-tasks.md).

## Prompts and templates

- Prompt: [../prompts/11-build-ai-context-from-prd.md](../prompts/11-build-ai-context-from-prd.md) — have the AI draft your context file and feature specs from the PRD.
- Template: [../templates/AI-CONTEXT.md](../templates/AI-CONTEXT.md) — the AI context file you save as `CLAUDE.md`, `AGENTS.md`, or Cursor rules.
- Template: [../templates/feature-spec.md](../templates/feature-spec.md) — one short spec per feature, kept in `specs/`.
