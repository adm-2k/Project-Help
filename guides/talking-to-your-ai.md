# Talking to Your AI

> The difference between a frustrating AI session and a smooth one is almost never luck. It is how you ask. This page teaches you how.

## Prompting is a skill, not a magic word

A lot of people believe that getting good results out of an AI builder is a matter of knowing some secret phrase, and that if the output is bad, they just have not found the magic word yet. That is not how it works, and the truth is better news: prompting is a skill you can learn, the same way you learned to write a clear email.

When a session goes sideways, it is usually because the request was vague, missing context, or trying to do too much at once. Tighten the ask and the output gets better. You will get the hang of this faster than you expect, because the moves are simple and they repeat.

If you just need something to paste right now, the quick-reference [prompt library](../prompts/README.md) gives you ready-made starting points for every step of the build. This page is different: it teaches the underlying skill, so that when a ready-made prompt does not quite fit, you can write your own and fix it when it drifts.

## The anatomy of a good ask

Almost every strong *prompt* (a term defined in the [glossary](../GLOSSARY.md) — it just means the instructions you type to your AI builder) has the same four parts:

- **Context** — Tell it what you are building and point it at your plan, so it is not guessing.
- **A specific request** — Name the one clear thing you want done, not a vague direction.
- **Constraints** — Say what to leave alone or avoid, so it does not wander into other work.
- **Ask it to explain** — Have it tell you what it changed and why, so you can check its thinking.

You will not need every part for every message, but when an ask goes wrong, the fix is almost always one of these four that you left out.

## Weak to strong: three rewrites

Here is what those four parts look like in practice. Each pair below takes a weak ask and rebuilds it into a strong one, using our running RecipeRoll project.

**Adding a feature.**

Weak:

```
make a recipe page
```

Strong:

```
In our RecipeRoll project (see PRD.md), build only the Add a Recipe form
with fields for title, ingredients, and steps, and a Save button. Do not
touch the browse or search pages. Explain what you changed.
```

Why the strong version works: it gives context (RecipeRoll, see `PRD.md`), names one specific thing (the Add a Recipe form and its fields), sets a constraint (do not touch browse or search), and asks for an explanation you can check.

**Fixing a bug.**

Weak:

```
the save button is broken, fix it
```

Strong:

```
In RecipeRoll, on the Add a Recipe form, clicking Save does nothing and no
recipe is added. Find out why and fix only that. Do not change the form
fields or the browse page. Explain in plain English what was wrong.
```

Why the strong version works: it describes what you expected versus what actually happened (context), points at one symptom to fix (specific), fences off everything else (constraint), and asks for a plain-English cause so you understand the fix.

**Making a small change.**

Weak:

```
make the form nicer
```

Strong:

```
On the RecipeRoll Add a Recipe form, change the Save button label to
"Save Recipe" and nothing else. Leave the layout and the other pages
alone. Tell me which file you edited.
```

Why the strong version works: "nicer" is an opinion the AI has to guess at, while "change the label to Save Recipe" is one concrete change (specific), bounded by a clear constraint, with a request to name the file so you can confirm.

## Course-correcting when it goes sideways

This is the part that matters most, because your AI builder will get things wrong, and the skill is not in writing one perfect prompt but in steering after the first try. When the output is not what you wanted, you do not start over and you do not argue in circles. You give a short, plain correction and move on.

Keep these lines handy and paste the one that fits:

```
That is not what I meant. Keep X, change Y.
```

```
You edited files I did not ask about. Undo those changes and only do Z.
```

```
Explain, in plain English, why you did that.
```

```
Go back to the simpler version before your last change.
```

The hardest judgment is knowing when to stop steering and start over. If you have corrected the same thing two or three times and it keeps drifting back, or the AI is undoing one fix while breaking something else, it is going in circles, and more corrections will not help. That is the moment to stop the conversation and open a fresh one.

The reason this works is that your AI builder has a short memory. As a chat gets long, earlier instructions fall out of view and the model starts working from a muddled picture of what you want; see the [short-memory idea](../HOW-AI-BUILDING-WORKS-FOR-NON-CODERS.md#it-has-a-short-memory) for why. A fresh session with the context re-given cleanly often fixes in one ask what ten corrections could not. For the full set of moves when you are well and truly stuck, see [getting unstuck](../guides/getting-unstuck.md).

> Tip: Before you start over, say what you want in one or two clean sentences and re-paste the relevant context. A fresh session only helps if you bring the plan with you.

## A few habits that help

A handful of small habits will save you most of the trouble before it starts:

- **Keep one task per conversation.** One feature or one bug per chat keeps the AI focused and keeps its short memory clear. Start a new conversation for the next thing.
- **Review what it gives you before accepting.** The AI is a fast assistant, not a final authority. Read the change and the explanation, and if either does not make sense, ask again.
- **Start fresh when a conversation gets long and muddled.** When the thread has wandered and corrections are not landing, open a new session and re-give the context. It is faster than fighting.

> Watch out: Never paste secrets into your AI builder. Passwords, API keys, and private personal data should not go into a chat tool, even when you are asking for help. If a secret is sitting in an error message, strip it out before you paste. When in doubt, leave it out.

## Related

- [Prompt library](../prompts/README.md) — ready-made prompts to copy, paste, and fill in.
- [How AI Building Works (for Non-Coders)](../HOW-AI-BUILDING-WORKS-FOR-NON-CODERS.md) — why the AI behaves the way it does, including its short memory.
- [Getting Unstuck](../guides/getting-unstuck.md) — what to do when a problem will not budge.
- [Prepare AI-Ready Deliverables](../guides/prepare-ai-ready-deliverables.md) — set up the context files your prompts point at.
