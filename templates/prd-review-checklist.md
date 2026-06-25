# PRD Review Rubric

This turns "is our plan good?" from a gut feeling into a clear, scored conversation your whole team can have together.

## How to use it

This works best as a small, honest ritual before anyone writes code. Here's the protocol:

1. Read your finished [PRD](../GLOSSARY.md) aloud together, start to finish. Reading it out loud catches vague words and gaps that the eye skims past.
2. Each teammate scores every dimension **independently** first. No peeking at each other's numbers. The point is to surface where you secretly disagree.
3. Compare your scores and talk through the gaps. If one person gave Scope a 3 and another gave it a 1, that gap is the conversation worth having.
4. Want a neutral second opinion? Paste your PRD into the [stress-test-the-PRD prompt](../prompts/02-stress-test-prd.md) and let your AI builder (Claude Code, Cursor, and the like) poke holes in it.
5. Whenever the discussion produces a real choice (for example, "v1 allows duplicate recipe names to keep it simple"), write it down in [your decisions log](../templates/DECISIONS.md) so no one re-litigates it later.

> Tip: A score should feel honest, not hopeful. If you're torn between two levels, pick the lower one and write down what would move it up.

## The scale

Every dimension is scored on the same three levels:

- **1 = Needs work.** A real gap. Someone could build the wrong thing because of it.
- **2 = Solid.** Good enough to build on, with minor rough edges.
- **3 = Strong.** Clear, specific, and hard to misread.

## The rubric

Score each of the eight dimensions below from 1 to 3 using its table.

### 1. Problem and user clarity

Is a specific user and a real pain named, instead of "people" who want "a thing"?

| Score | What it looks like |
| --- | --- |
| 1 | The user is "everyone" or "users." The problem is abstract or assumed. You can't picture a real person who is stuck. |
| 2 | A user type is named and a problem is described, but it's a little generic. You'd have to guess at the details. |
| 3 | A specific user and their real pain are named in plain words you could repeat to a stranger. |

_RecipeRoll at level 3:_ "Home cooks who keep recipes scattered across screenshots, texts, and bookmarks, and can never find the one they want when they're standing at the stove."

### 2. Measurable success

Are the goals checkable, with a number or a condition, not just a feeling?

| Score | What it looks like |
| --- | --- |
| 1 | Success is described with words like "useful" or "popular" and no way to check it. |
| 2 | Goals are concrete but partly fuzzy. You could check some of them, but at least one still needs interpretation. |
| 3 | Every goal has a number or a clear yes/no condition. You could sit down and check each one. |

_RecipeRoll at level 3:_ "A cook can add a recipe and find it again by name in under 10 seconds, with zero recipes lost between sessions."

### 3. Scope discipline

Is the _Must-have_ list genuinely minimal, with explicit non-goals?

| Score | What it looks like |
| --- | --- |
| 1 | The Must-have list is a wish list. Nice-to-haves are mixed in. There's no "Out of scope" section. |
| 2 | Scope is mostly tight, but one or two items could be cut, or the non-goals are implied rather than written. |
| 3 | Nothing on the Must-have list could be removed without breaking the product, and an explicit "Out of scope" list says what you're _not_ building yet. |

_RecipeRoll at level 3:_ "Must-have: add, browse, search recipes. Out of scope for v1: photos, ratings, sharing, import from links."

### 4. User stories and acceptance criteria

Are the stories testable, each with a "done when" condition?

| Score | What it looks like |
| --- | --- |
| 1 | Features are listed as nouns ("search") with no story and no way to tell when they're finished. |
| 2 | Stories exist, but the "done when" conditions are vague or missing for some of them. |
| 3 | Each story is written from the user's view and has clear _acceptance criteria_ ([what it means](../GLOSSARY.md) for the work to be done). |

_RecipeRoll at level 3:_ "As a cook, I can search by name. Done when: typing part of a saved recipe's name returns it in the list, and an empty search shows everything."

### 5. Feasibility

Can this small team actually build this v1, in the time they have, with the tools they know?

| Score | What it looks like |
| --- | --- |
| 1 | The plan quietly needs a skill, tool, or amount of time the team doesn't have. The timeline is a hope. |
| 2 | Mostly buildable, but one item is a stretch or rests on a tool nobody has used yet. |
| 3 | Every in-scope item is something this team can build with what they know, in the time they've set. |

_RecipeRoll at level 3:_ "Add, browse, and search are plain list operations the team has built before, well within a two-week window."

### 6. Decomposability

Can the work split into independent, one-owner tasks? (You'll do this in [Step 3: Break into tasks](../guides/step-3-break-into-tasks.md).)

| Score | What it looks like |
| --- | --- |
| 1 | The work is one tangled lump. Everything depends on everything, so two people can't work without colliding. |
| 2 | It mostly splits, but a couple of features are knotted together and would need careful hand-offs. |
| 3 | You can already picture one person owning each in-scope feature and building it without tripping over the others. |

_RecipeRoll at level 3:_ "One person owns 'add a recipe,' another owns 'search,' another owns 'browse the list,' and they meet only at the shared data shape."

### 7. Risks and assumptions surfaced

Are the unknowns written down, instead of living in one person's head?

| Score | What it looks like |
| --- | --- |
| 1 | No open questions or assumptions are written. Everyone assumes everyone else has it handled. |
| 2 | Some risks are noted, but the obvious unknowns or the assumptions you're betting on aren't all on paper. |
| 3 | Open questions, assumptions, and constraints are all written down where the team can see and challenge them. |

_RecipeRoll at level 3:_ "Open question: do we allow duplicate recipe names? Assumption: search is case-sensitive in v1, which we already know is a bug to revisit."

### 8. Communication and clarity

Can a non-technical teammate explain the PRD back, with no vague words doing the heavy lifting?

| Score | What it looks like |
| --- | --- |
| 1 | Vague words like "fast," "simple," or "nice" carry the meaning without ever being defined. A non-technical reader gets lost. |
| 2 | Mostly readable, but a term or two is undefined or a fuzzy word slips in unexplained. |
| 3 | Every term is defined or obvious, no vague word is load-bearing, and a non-technical teammate can explain it back in their own words. |

_RecipeRoll at level 3:_ "'Fast search' is defined as 'results appear in under one second,' so 'fast' isn't left to interpretation."

## Scoring

Add up all eight dimensions. The total is out of **24** (eight dimensions, three points each).

- **20-24 - Strong.** Ready to build. Note any single low dimension and keep an eye on it.
- **14-19 - Solid.** Build is in reach, but fix your lowest-scoring dimensions first. That's where the wrong thing gets built.
- **Below 14 - Revise before building.** Fixing the plan now is far cheaper than fixing it after four people have built the wrong thing.

The goal is honest improvement, not a high score. A 16 you trust is worth more than a 22 you talked yourself into.

> Watch out: Don't "fix" a low score by deleting the requirement. Fix it by making the PRD clearer, smaller, or more testable. Cutting a hard requirement just to score higher is how teams ship the wrong product on time.

## A note on what good looks like

This rubric is a lightweight version of how real teams gate a spec before they build it. Companies call it a spec review, a design review, or a readiness gate, but the move is the same: pressure-test the plan while changing it is still cheap. Practicing this habit now means that when you join a team that does it for real, you'll already know why it matters and how to take part. That makes it a transferable, employer-relevant skill, not just a class exercise.
