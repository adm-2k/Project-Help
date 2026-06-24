# 🔎 Prompt: Review a teammate's pull request

> Get a careful, friendly first read of a teammate's work so your review comments are specific, helpful, and kind.

When a teammate opens a **pull request** (a request to add their work to the shared project), someone reviews it before it joins the main project. This prompt turns your AI builder into a thoughtful reviewing partner that helps you spot issues and word your feedback well.

## ⏱️ Before you start

- Open the pull request on GitHub. Read its **description** (what the author says it does) and look at its **diff** (the list of changed lines, shown in red and green).
- Know what the task was meant to do, so you can check the work against it. The original task lives on your [task board](../templates/task-board.md).

> 💡 **Tip:** You are not expected to catch everything. Your job is a kind, useful first pass — the AI helps you be specific instead of vague.

## 💬 The prompt

Copy this into your AI builder. Paste in the PR description and the diff (or point your AI tool at the branch).

```
Act as a careful, friendly code reviewer for a teammate who is not a
senior engineer. Your tone should be warm and encouraging — the kind of
review a teammate is happy to receive. Assume good intent. Never be
harsh or nitpicky for its own sake.

Here is what the task was supposed to do:
[paste the task description]

Here is the pull request description and the changed code:
[paste the PR description and the diff]

Please review and tell me:

1. Does it do the task? Say clearly whether the change accomplishes
   what the task asked. Note anything missing.
2. Likely bugs: point out anything that looks like it could break or
   behave wrong, and explain why in plain English.
3. Unclear names: flag any names of things that are confusing, and
   suggest clearer ones.
4. Missing pieces: note anything that seems half-done, untested, or
   forgotten.

Then write 3 to 6 specific review comments I could post, each in this
shape: a kind opening, the exact spot it refers to, and a concrete
suggestion. Lead with anything you genuinely liked.

If the change looks good, say so plainly — do not invent problems.
```

> 🎯 **Why this matters:** Reviews are where the team catches small problems early and where teammates feel supported. Specific, kind comments build trust; vague or harsh ones do the opposite.

## 👀 After the AI replies

1. Read the AI's findings, but stay in charge — you decide which comments to post. The AI can be wrong or overly cautious.
2. Drop any comment that does not really matter for **v1** (your first working version).
3. Post the comments you agree with on the PR, on the exact lines they refer to.
4. If everything looks good, say so and approve it — see [Step 6: Review and merge](../guides/step-6-review-and-merge.md).

## ⚠️ Watch out

> - **Do not paste the AI's comments without reading them.** It sometimes flags non-issues or misreads intent. You are the human reviewer.
> - Keep feedback about the code, not the person. "This name could be clearer" — never "you did this wrong".
> - Approving is not a rubber stamp. If you genuinely cannot tell whether it works, ask the author to walk you through it.

## ✅ You're done when

- [ ] You know whether the PR does what the task asked.
- [ ] You have posted specific, kind comments (or a clear approval).
- [ ] Any real bugs or missing pieces are raised for the author.

## ➡️ Next

Use this prompt as part of [Step 6: Review and merge](../guides/step-6-review-and-merge.md).

## 📎 Related files

- Guide: [Step 6: Review and merge](../guides/step-6-review-and-merge.md)
- Template: [Task board](../templates/task-board.md)
