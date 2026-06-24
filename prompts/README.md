# Prompt Library — Your Team's Reusable AI Skills

> This folder holds ready-made prompts: copy-paste starting points you fill in and hand to your AI builder at each step.

Think of each prompt as a small skill your whole team shares. Instead of inventing what to say to the AI every time, you grab the right one, fill in the blanks, and go. Everyone gets consistent results.

## How to use these prompts

Every prompt works in any AI builder — Claude Code, Cursor, ChatGPT, and others. The steps are always the same:

1. Open the prompt file for the step you're on (the table below links each one).
2. Copy the text inside the fenced code block (the part between the lines of three backticks).
3. Replace every `[BRACKETED PART]` with your real details.
4. Paste it into your AI builder and send it.
5. Read what comes back, ask follow-up questions, and refine.

A *prompt* is the message you send to your AI. Your *AI builder* is the tool you're working in. If a term here is unfamiliar, check the [glossary](../GLOSSARY.md).

## Optional: save prompts as reusable skills in your tool

Once a prompt works well for your team, you can save it inside your tool so it's one click away next time. This is optional; copy-paste works fine.

- Claude Code: save a prompt as a reusable *skill* or a *slash command* so you can trigger it by name.
- Cursor: save the prompt as a *rule* so it's always available in your project.

Either way, the idea is the same: turn a prompt you trust into a button you can reuse.

## Golden rules of prompting for building

These six habits are the difference between a confused AI and a helpful one.

| Rule | What it means |
| --- | --- |
| Give context | Point the AI at your [PRD](../templates/PRD-template.md) and tell it what you're building. The more it knows, the better it helps. |
| Be specific | Vague in, vague out. Say exactly what you want, for whom, and what "done" looks like. |
| Ask for small steps | Request one small, reviewable change at a time, not a whole app at once. Small steps are easy to check and easy to undo. |
| Ask it to explain | Have the AI explain what it's doing and why, in plain English. If the explanation doesn't make sense to you, ask again. |
| Always review the output | The AI is a fast assistant, not a final authority. Read everything it produces before you accept it. |
| Say what NOT to touch | Tell the AI which files or features to leave alone. That keeps it from breaking a teammate's work. |

> Watch out: Never paste in passwords, private keys, or other secrets. Treat anything you send as if someone else could read it.

## The 11 prompts

Use them roughly in order; they follow the build steps.

| # | Prompt | What it does |
| --- | --- | --- |
| 01 | [Draft the PRD](01-draft-prd.md) | Turn your rough notes into a clear product plan. |
| 02 | [Stress-test the PRD](02-stress-test-prd.md) | Have the AI poke holes in your plan before you build. |
| 03 | [Decompose into tasks](03-decompose-into-tasks.md) | Break the plan into small, branch-sized jobs for the team. |
| 04 | [Build a task on a branch](04-build-a-task-on-a-branch.md) | Build your feature safely on your own branch. |
| 05 | [Keep me in sync](05-keep-me-in-sync.md) | Pull in teammates' changes so you don't fall behind. |
| 06 | [Resolve a merge conflict](06-resolve-a-merge-conflict.md) | Calmly fix the spot where two edits overlap. |
| 07 | [Write my pull request](07-write-my-pr.md) | Draft a clear summary of your change for review. |
| 08 | [Review a teammate's PR](08-review-a-teammates-pr.md) | Give kind, useful feedback on someone's work. |
| 09 | [Log an issue](09-log-an-issue.md) | Capture a bug or idea so it isn't forgotten. |
| 10 | [Update the roadmap](10-update-the-roadmap.md) | Keep your plan current as features ship. |
| 11 | [Build AI context from the PRD](11-build-ai-context-from-prd.md) | Turn your PRD into a shared context file and feature specs your AI tools follow. |

> Tip: A prompt's output is a strong first draft, not the final word. Your judgment, and your team's, decides what stays.
