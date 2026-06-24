# The Upskilling Labs — Team Builder Playbook

**Build real software with your team and AI, without stepping on each other.**

This repo is your team's instruction manual. It shows a small group of people, with no coding experience required, how to take an idea, plan it well, and use AI builder tools like Claude Code and Cursor to build it together, so everyone adds their own piece without overwriting anyone else's work.

You don't need to read it all in one sitting. The first time through, you move through seven steps in order. After that, you loop the last few steps for every new feature.

---

## The big picture: one loop, seven steps

```
        ┌──────────────────────────────────────────────────────────┐
        │                                                          │
        ▼                                                          │
  ① WRITE THE PRD ──▶ ② REVIEW THE PRD ──▶ ③ BREAK INTO TASKS      │
   (agree the plan)    (poke holes in it)   (one task = one branch) │
                                                  │                 │
                                                  ▼                 │
  ⑦ UPDATE ROADMAP ◀── ⑥ REVIEW & MERGE ◀── ⑤ OPEN A PR ◀── ④ CLAIM │
     & LOG ISSUES        (keep main healthy)   (propose it)   & BUILD
        │                                                  (on a branch)
        └──────────────── pick the next task, loop ────────────────┘
```

Steps ① ② ③ happen once per project. Steps ④ ⑤ ⑥ ⑦ repeat for every feature.

---

## Where am I? What do I do now?

| If your team is… | Go here |
|---|---|
| Just starting, and you haven't agreed what you're building | **[Step 1: Write the PRD](guides/step-1-write-the-prd.md)** |
| Holding a draft plan and want to make sure it's solid | **[Step 2: Review the PRD](guides/step-2-review-the-prd.md)** |
| Done planning, and you need to split the work | **[Step 3: Break into tasks](guides/step-3-break-into-tasks.md)** |
| Handed a task you need to build | **[Step 4: Claim & build on a branch](guides/step-4-claim-and-build.md)** |
| Finished a piece you want in the project | **[Step 5: Open a pull request](guides/step-5-open-a-pull-request.md)** |
| Asked by a teammate to review their work | **[Step 6: Review & merge](guides/step-6-review-and-merge.md)** |
| Just done with something | **[Step 7: Update roadmap & log issues](guides/step-7-update-roadmap-and-log-issues.md)** |
| Nervous about git, branches, or merge conflicts | **[How Git Works for Non-Coders](HOW-GIT-WORKS-FOR-NON-CODERS.md)** |
| Stuck on a word you don't understand | **[Glossary](GLOSSARY.md)** |
| Curious to see one full lap before you start | **[Example walkthrough](examples/EXAMPLE-walkthrough.md)** |

> Tip: First time here? Start with the **[Team Kickoff Checklist](checklists/team-kickoff.md)**. It covers everything to set up before Step 1.

---

## What's in this repo

| Folder | What it holds | When you use it |
|---|---|---|
| **[`guides/`](guides/)** | The seven step-by-step guides, the heart of the playbook | Follow in order |
| **[`templates/`](templates/)** | Fill-in-the-blank documents (PRD, roadmap, task board, issue log, decision log) | Copy and fill as you go |
| **[`prompts/`](prompts/)** | Ten copy-paste AI prompts, proven for each step | Whenever you talk to the AI |
| **[`checklists/`](checklists/)** | Quick "before you do X" checklists | Pin these; glance before acting |
| **[`.github/`](.github/)** | Templates GitHub shows automatically when you open a PR or file an issue | Automatic |
| **[`examples/`](examples/)** | A complete worked example, one team going from idea to merged feature | Read once, early |

---

## What you'll need

- **A GitHub account** for everyone on the team, and access to your team's repo. (No repo yet? See the [Team Kickoff Checklist](checklists/team-kickoff.md).)
- **An AI builder tool.** This playbook is tool-agnostic, and works with Claude Code, Cursor, and similar tools. The examples name those, but the ideas apply to any AI coding assistant.
- **A visual way to use git** if commands make you nervous. We recommend [GitHub Desktop](https://desktop.github.com/), or you can use your AI tool's built-in git. You will not have to memorize commands. See **[How Git Works for Non-Coders](HOW-GIT-WORKS-FOR-NON-CODERS.md)**.

---

## The five rules that make team-building-with-AI work

These come up again and again. Learn them, and the rest is detail.

1. **The plan is sacred.** The PRD is your single source of truth, and the AI is only as good as the plan you hand it. (Steps 1–2)
2. **One task, one owner, one branch.** Small pieces that don't touch the same files won't collide. (Step 3)
3. **Pull before you push.** Get everyone's latest work before you share yours. (Steps 4–5)
4. **Main always works.** Never merge something broken into the shared version. (Step 6)
5. **If it happened, write it down.** Roadmap, issues, and decisions keep the team, and the AI, in sync. (Step 7)

---

## The running example: RecipeRoll

Throughout this playbook, one imaginary team of four, **Maya, Sam, Priya, and Devin**, builds **RecipeRoll**, a simple app for sharing recipes. You'll see their PRD, their tasks, their branches, and their pull requests in every guide, so you always have a concrete picture of what good looks like. Read the whole story in the **[example walkthrough](examples/EXAMPLE-walkthrough.md)**.

---

## Quick start for a brand-new team

1. **Everyone** reads this page and skims the **[Glossary](GLOSSARY.md)**.
2. Together, work through the **[Team Kickoff Checklist](checklists/team-kickoff.md)**.
3. Read the **[Example walkthrough](examples/EXAMPLE-walkthrough.md)** to see one full lap.
4. Start **[Step 1: Write the PRD](guides/step-1-write-the-prd.md)**, and keep going.

---

*Made for The Upskilling Labs. Copy this repo, make it your own, and go build something.*
