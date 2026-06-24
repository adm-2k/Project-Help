# Prompt: Log an issue

> Turn a rough "this is broken" or "we should add this" into a clear, well-formed issue your team can act on.

An *issue* is a written note about a bug (something that is broken) or an idea (something to add), tracked so it does not get forgotten. This prompt helps your AI builder shape your rough notes into the format your team uses.

## Before you start

- Have a rough description, in your own words, of what you noticed.
- For a bug, copy any *error text* (the red message the app or tool showed) so you can paste it in.
- Decide whether this is a *bug* (something broke) or a *feature request* (a new idea), so you pick the right template.

> Tip: Do not polish your notes first. Paste them rough. Turning rough notes into a clean issue is exactly what this prompt is for.

## The prompt

Copy this into your AI builder. Paste in your rough notes and any error text.

```
Help me turn this rough note into a clear, well-formed issue for our
project tracker. Keep it short and plain — a teammate should understand
it in 20 seconds.

Here is my rough note:
[describe what happened or the idea, in your own words]

Here is any error text I saw (leave blank if none):
[paste error text]

Decide whether this is a BUG or a FEATURE REQUEST, then write the issue
in that format:

If it is a BUG, include:
- Title: short and specific.
- What happened: the actual behavior.
- What I expected instead: the correct behavior.
- Steps to reproduce: numbered steps anyone can follow to see it.
- Where it occurs: which page, screen, or feature.
- Severity: low / medium / high, with one line on why.

If it is a FEATURE REQUEST, include:
- Title: short and specific.
- What I want: the idea in plain English.
- Why it helps: the benefit to users.
- Where it would go: which page or feature.

Finally, suggest a label/type for it (for example: bug, enhancement,
question) and tell me which template matches.
```

A vague issue ("search is weird") gets ignored. A clear one with steps to reproduce gets fixed. Good issues are how nothing important slips through the cracks.

## RecipeRoll example

Priya notices that typing `Tomato` returns nothing, but `tomato` works. She pastes that rough note into the prompt, and the AI shapes it into a bug:

- **Title:** Search is case-sensitive and misses capitalized words
- **What happened:** Searching `Tomato` returns no recipes.
- **What I expected instead:** It should find recipes with `tomato`, regardless of capital letters.
- **Steps to reproduce:** 1) Open the search page. 2) Type `Tomato`. 3) See zero results, even though a tomato recipe exists.
- **Where it occurs:** Search by ingredient feature.
- **Severity:** Medium. Users will hit this often, but the app still works.
- **Suggested label:** bug

She then adds it to the [issue log](../templates/ISSUE-LOG.md) and opens an issue using the [bug report template](../.github/ISSUE_TEMPLATE/bug_report.md).

## Watch out

> Watch out: For bugs, the numbered steps to reproduce are the most important part, so make sure they actually trigger the problem. Keep it to one issue per note: if your rough note describes two problems, ask the AI to split it into two issues. And pick the right template, since bugs and feature requests have different shapes.

## You're done when

- [ ] You have a clear title and a filled-in issue in the right format.
- [ ] For a bug, the steps to reproduce actually show the problem.
- [ ] You have added it to the [issue log](../templates/ISSUE-LOG.md) or opened it on GitHub with the matching template.

## Next

Use this prompt as part of [Step 7: Update the roadmap and log issues](../guides/step-7-update-roadmap-and-log-issues.md).

## Related files

- Guide: [Step 7: Update the roadmap and log issues](../guides/step-7-update-roadmap-and-log-issues.md)
- Template: [Issue log](../templates/ISSUE-LOG.md)
- Template: [Bug report template](../.github/ISSUE_TEMPLATE/bug_report.md)
