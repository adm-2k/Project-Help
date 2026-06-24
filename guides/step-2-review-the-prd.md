# Step 2: Review the PRD

> Stress-test your plan and lock the v1 scope before anyone starts building.

**Goal:** turn a rough plan into a clear, agreed one · **Time:** 30 to 45 minutes · **Who:** the whole team, together

## Why it matters

Right now your plan is words on a page, so changing it costs nothing. Once people start building, changing the plan means throwing away work. The cheapest moment to fix a confusing or oversized plan is this meeting, before a single line of the app exists. And here is the thing to keep in mind: if a teammate reads the plan and feels confused, your *AI builder* (the [AI builder](../GLOSSARY.md) like Claude Code or Cursor that turns your words into code) will be confused too.

## What to do

1. **Read the PRD aloud, together.** Open your [PRD](../GLOSSARY.md) (the plan you wrote in [Step 1](step-1-write-the-prd.md)) and have one person read it out loud while everyone follows along. Hearing it catches problems that silent reading hides.

2. **Each person flags anything unclear.** Go around the group. Every person names at least one thing they found vague, missing, or too big. The rule: if you are not sure what a sentence means, say so now.

3. **Let the AI play skeptical product manager.** Paste the prompt from [../prompts/02-stress-test-prd.md](../prompts/02-stress-test-prd.md) into your AI builder, along with your PRD. It acts as a tough but fair reviewer and surfaces:
   - Ambiguities (sentences that could mean two things)
   - Missing edge cases (the "but what if..." situations)
   - Scope creep (features sneaking in that are not really v1)
   - Open questions the team has not answered yet

   The prompt starts like this:

   ```
   You are a skeptical but constructive product manager. Review the
   PRD below for a v1 (minimum viable) release. Find ambiguities,
   missing edge cases, scope creep, and unanswered questions. Be
   specific. [Paste the full PRD here.]
   ```

4. **Work through the review checklist.** Open [../templates/prd-review-checklist.md](../templates/prd-review-checklist.md) and tick each item as a team. It makes sure you did not skip anything the AI or the group missed.

5. **Resolve each issue.** For every flag, either tighten the wording or cut the feature out of v1. Leave nothing unresolved.

6. **Record your choices.** Every real decision goes into [../templates/DECISIONS.md](../templates/DECISIONS.md) as one short line, so nobody re-argues it later.

7. **Lock the v1 scope.** Once the checklist passes, agree out loud: "This is v1. Everything else is Later." Write the final v1 feature list at the top of the PRD.

Define every fuzzy word while you are at it. "Fast", "simple", and "easy" mean nothing until you attach a number or an example. "Fast" becomes "the recipe list loads in under 2 seconds".

> Tip: Save the finished PRD in the repo as `PRD.md` so it lives next to the code and gets versioned right alongside it. When the plan changes, the history shows what changed and when.

## Example: RecipeRoll

The team reads the RecipeRoll PRD aloud. When they reach the "Add a recipe" section, Sam asks a sharp question: what happens if two people add a recipe with the same name? Do we block it? Warn them? Allow it?

Nobody had thought about it. The AI's stress-test had flagged the same thing as an open question. The team talks for two minutes and decides: duplicate recipe names are allowed for v1, to keep things simple, and they will revisit it if it becomes confusing.

Maya logs it in [../templates/DECISIONS.md](../templates/DECISIONS.md):

```
| 2026-06-24 | Duplicate recipe names | Allow duplicates for v1; keep it simple, revisit if confusing | Whole team |
```

They also catch a vague phrase, "search should be fast", and replace it with a real success criterion: a new visitor can add a recipe and then find it by searching one of its ingredients, in under a minute, without help. Then they confirm that photos, ratings, logins, and comments are all Later, and lock v1.

## Watch out for

- **The polite review that challenges nothing.** If everyone nods and no flags are raised, the review failed. Your job here is to find problems, not to be agreeable. Make sure each person names at least one concern.
- **Fuzzy words left undefined.** "Simple", "fast", "intuitive", and "clean" are traps. Replace each one with a number, an example, or a concrete sentence.
- **Scope that quietly grows.** Every "we could also..." is a Later, not a v1. Write it down under Later and move on.

## You're done when

- [ ] The whole team read the PRD aloud together
- [ ] Each person flagged at least one concern
- [ ] You ran the stress-test prompt and read the AI's findings
- [ ] Every item on the [review checklist](../templates/prd-review-checklist.md) is ticked
- [ ] Every fuzzy word now has a number or a concrete example
- [ ] Each real decision is logged in [DECISIONS.md](../templates/DECISIONS.md)
- [ ] The v1 feature list is written down and everyone agreed "this is v1"

## Next

Your plan is solid and locked. Before you split the work, turn it into a single source of truth your AI tools can all follow: [Turn your PRD into a shared source of truth](prepare-ai-ready-deliverables.md). Then slice it into bite-sized tasks: [Step 3: Break into tasks](step-3-break-into-tasks.md).

## Prompts and templates

- [../prompts/02-stress-test-prd.md](../prompts/02-stress-test-prd.md) — have the AI act as a skeptical product manager
- [../templates/prd-review-checklist.md](../templates/prd-review-checklist.md) — the item-by-item review checklist
- [../templates/DECISIONS.md](../templates/DECISIONS.md) — where you log each decision
