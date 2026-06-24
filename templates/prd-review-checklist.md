# PRD Review Checklist

Use this to confirm your [PRD](../GLOSSARY.md) is clear and buildable before anyone starts building.

**How to use this checklist as a team**

1. Open your finished `PRD.md` next to this checklist.
2. Read each item out loud together and tick the box if your PRD passes it.
3. A box you can't tick isn't a failure. It's a thing to fix.
4. Want a second opinion? Paste your PRD into the [stress-test-the-PRD prompt](../prompts/02-stress-test-prd.md) and let your AI builder (Claude Code, Cursor, and the like) poke holes in it.

> Tip: Ticking a box should feel honest, not hopeful. If you're not sure, leave it unchecked and talk it through.

---

## Clarity

- [ ] Every term in the PRD is defined or obvious.
- [ ] A non-technical teammate can read it and explain it back in their own words.
- [ ] No vague word is doing the heavy lifting (like "simple", "fast", "nice", or "easy") without saying what it actually means.

## Scope

- [ ] The v1 list is genuinely minimal. Nothing on it could be cut and still leave a useful product.
- [ ] Each item in scope is a must-have, not a nice-to-have.
- [ ] There's an explicit "Out of scope" list, so everyone knows what you're _not_ building yet.

## Users

- [ ] A real user is named, not just "people" or "everyone."
- [ ] A real need that user has is described in plain words.

## Testable

- [ ] The success criteria are concrete and measurable.
- [ ] You could sit down and check whether each criterion is met.

## Feasible

- [ ] A small team could realistically build this v1 in the time you have.
- [ ] Nothing in scope secretly requires a skill or tool your team doesn't have.

## Splittable

- [ ] The work can be divided into independent tasks people can build without tripping over each other. (You'll do this in [Step 3: Break into tasks](../guides/step-3-break-into-tasks.md).)
- [ ] You can already imagine one person owning each in-scope feature.

## Risks

- [ ] Open questions are written down, not floating in someone's head.
- [ ] Assumptions and constraints are written down too.

---

## Decision rule

Count your unchecked boxes.

- **3 or fewer unchecked:** good enough. Note the gaps and move on to building.
- **More than about 3 unchecked:** stop and revise the PRD before building. Fixing it now is far cheaper than fixing it after four people have built the wrong thing.

Whenever you make a real choice during this review (for example, "v1 allows duplicate recipe names to keep it simple; revisit if it becomes confusing"), record it in [your decisions log](../templates/DECISIONS.md) so no one re-litigates it later.

> Watch out: Don't "fix" a failing box by deleting the requirement. Fix it by making the PRD clearer, smaller, or more testable.
