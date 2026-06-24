# Prompt: Write my pull request

> Turn the changes on your branch into a clear pull request description your teammates can review quickly.

A *pull request* (PR) is how you ask your team to look at your work and add it to the shared project. This prompt asks your AI builder to write the PR description for you, in the exact shape your team expects.

## Before you start

- Your work is saved and *pushed* (sent up to GitHub) on your *branch* (your own safe copy of the project). If you are not sure, see [Step 5: Open a pull request](../guides/step-5-open-a-pull-request.md).
- You know which task or *issue* (a logged bug or to-do) this work relates to, so you can name it.
- You have the [pull request template](../.github/PULL_REQUEST_TEMPLATE.md) open in another tab so you can see the shape you are aiming for.

> Tip: You do not have to write a word yourself. Let the AI draft it, then read it the way a teammate would and fix anything that does not match what you actually did.

## The prompt

Copy this into your AI builder (Claude Code, Cursor, and the like). Fill in the parts in [BRACKETS].

```
You are helping me write a pull request description for my teammates,
who are not all technical. Be clear, plain, and friendly.

First, look at the changes on my current branch compared to the main
branch (the diff). Summarize what I actually changed.

Then write a pull request description using exactly these sections:

- What this does: 2 to 4 plain-English sentences. No jargon.
- Related task/issue: [paste the task name or issue number, e.g. "Feature A: Add a recipe form" or "Closes #12"]
- How to test it: numbered steps a non-technical teammate can follow to see it working.
- What to watch for: anything unfinished, any decision I made, or any place I am unsure.
- Screenshots needed?: tell me yes or no, and if yes, exactly which screens to capture.

Keep it short. Use bullet points and numbered steps. Do not invent
changes I did not make — only describe what is in the diff.
```

A good PR description means your reviewer understands your work in under a minute, which gets your feature merged faster and with less back-and-forth.

> Tip: In the "Related task/issue" line, writing `Closes #12` tells GitHub to close issue 12 automatically the moment your PR is merged. One less thing to remember.

## After the AI replies

1. **Read** the "What this does" section. Does it match what you set out to build? Trim anything that sounds too technical.
2. **Check** that the "Related task/issue" line points at the right task.
3. **Try** the "How to test it" steps yourself. If you cannot follow them, your reviewer cannot either, so ask the AI to simplify.
4. **Capture** any screenshots that are needed and drag them into the PR on GitHub.
5. **Paste** the final text into the PR description box and open the PR.

## Watch out

> Watch out: An empty or vague description like "fixed stuff" forces your reviewer to guess. Always say what changed and how to test it. The AI can only see what is committed and pushed, so if something is missing from the summary, you probably have unsaved work to go back and save. And do not let the AI claim work you did not do; if it lists a change you do not recognize, ask it to recheck the diff.

## You're done when

- [ ] You have a PR description with all five sections filled in.
- [ ] The related task or issue is named.
- [ ] The "How to test it" steps work when you try them.
- [ ] Screenshots are added if they were needed.

## Next

Use this prompt as part of [Step 5: Open a pull request](../guides/step-5-open-a-pull-request.md).

## Related files

- Guide: [Step 5: Open a pull request](../guides/step-5-open-a-pull-request.md)
- Template: [Pull request template](../.github/PULL_REQUEST_TEMPLATE.md)
