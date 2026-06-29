# The Upskilling Labs — Team Builder Playbook

**Build real software with your team and AI, without stepping on each other.**

This repo is your team's instruction manual. It shows a small group of people, with no coding experience required, how to take an idea, plan it well, and use AI builder tools like Claude Code and Cursor to build it together, so everyone adds their own piece without overwriting anyone else's work.

You don't need to read it all in one sitting. The first time through, you move through seven steps in order. After that, you loop the last few steps for every new feature.

> New or overwhelmed? Open **[GUIDE-ME.md](GUIDE-ME.md)** and paste it into ChatGPT or Claude. It turns the AI into a guide that reads this playbook and tells you exactly what to do next.

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

Steps ① ② ③ happen once per project. Steps ④ ⑤ ⑥ ⑦ repeat for every feature. Before all of this, [Step 0: Getting comfortable](guides/step-0-getting-comfortable.md) helps a nervous team settle in. When you are ready to show real users, an optional [Step 8: Share it and go live](guides/step-8-share-and-go-live.md) puts it online.

---

## Where am I? What do I do now?

| If your team is… | Go here |
|---|---|
| New to all this and a little nervous | **[Step 0: Getting comfortable](guides/step-0-getting-comfortable.md)** |
| Not sure what AI can and can't do | **[How AI Building Works for Non-Coders](HOW-AI-BUILDING-WORKS-FOR-NON-CODERS.md)** |
| Haven't set up your accounts and tools yet | **[Getting set up](guides/getting-set-up.md)** |
| Wanting an AI to just tell you the next step | **[GUIDE-ME.md](GUIDE-ME.md)** |
| Just starting, and you haven't agreed what you're building | **[Step 1: Write the PRD](guides/step-1-write-the-prd.md)** |
| Holding a draft plan and want to make sure it's solid | **[Step 2: Review the PRD](guides/step-2-review-the-prd.md)** |
| Done planning and want every AI tool to build the same thing | **[Prepare AI-ready deliverables](guides/prepare-ai-ready-deliverables.md)** |
| Done planning, and you need to split the work | **[Step 3: Break into tasks](guides/step-3-break-into-tasks.md)** |
| Handed a task you need to build | **[Step 4: Claim & build on a branch](guides/step-4-claim-and-build.md)** |
| Finished a piece you want in the project | **[Step 5: Open a pull request](guides/step-5-open-a-pull-request.md)** |
| Asked by a teammate to review their work | **[Step 6: Review & merge](guides/step-6-review-and-merge.md)** |
| Just done with something | **[Step 7: Update roadmap & log issues](guides/step-7-update-roadmap-and-log-issues.md)** |
| Ready to put it online for real people | **[Step 8: Share it and go live](guides/step-8-share-and-go-live.md)** |
| Ready to show your work to employers | **[Turn it into a portfolio piece](guides/build-your-portfolio-piece.md)** |
| Not sure which tools to use | **[Choosing your tools](tools/README.md)** |
| Stuck, or something just broke | **[Getting unstuck](guides/getting-unstuck.md)** |
| Not getting good results from the AI | **[Talking to your AI](guides/talking-to-your-ai.md)** |
| Worried about cost or credits | **[Managing cost and credits](tools/managing-cost-and-credits.md)** |
| Nervous about git, branches, or merge conflicts | **[How Git Works for Non-Coders](HOW-GIT-WORKS-FOR-NON-CODERS.md)** |
| Stuck on a word you don't understand | **[Glossary](GLOSSARY.md)** |
| Curious to see one full lap before you start | **[Example walkthrough](examples/EXAMPLE-walkthrough.md)** |

> Tip: First time here? Start with the **[Team Kickoff Checklist](checklists/team-kickoff.md)**. It covers everything to set up before Step 1.

---

## What's in this repo

| Folder | What it holds | When you use it |
|---|---|---|
| **[`guides/`](guides/)** | The step-by-step guides, the heart of the playbook (Step 0 through Step 8, plus getting unstuck) | Follow in order |
| **[`templates/`](templates/)** | Fill-in-the-blank documents (PRD, roadmap, task board, issue log, decision log, AI context, feature spec) | Copy and fill as you go |
| **[`prompts/`](prompts/)** | Eleven copy-paste AI prompts, proven for each step | Whenever you talk to the AI |
| **[`tools/`](tools/)** | Plain comparisons of the cheapest, easiest tools, with a recommended starter stack | When choosing what to build with |
| **[`checklists/`](checklists/)** | Quick "before you do X" checklists | Pin these; glance before acting |
| **[`.github/`](.github/)** | Templates GitHub shows automatically when you open a PR or file an issue | Automatic |
| **[`examples/`](examples/)** | A complete worked example, one team going from idea to merged feature | Read once, early |
| **[`for-facilitators/`](for-facilitators/)** | A guide for the mentor running a cohort | If you are leading a team |

---

## What you'll need

- **A GitHub account** for everyone on the team, and access to your team's repo. (No repo yet? See the [Team Kickoff Checklist](checklists/team-kickoff.md).)
- **An AI builder tool.** This playbook is tool-agnostic, and works with Claude Code, Cursor, and similar tools. The examples name those, but the ideas apply to any AI coding assistant.
- **A visual way to use git** if commands make you nervous. We recommend [GitHub Desktop](https://desktop.github.com/), or you can use your AI tool's built-in git. You will not have to memorize commands. See **[How Git Works for Non-Coders](HOW-GIT-WORKS-FOR-NON-CODERS.md)**.

> New to AI itself, or not set up yet? Read **[How AI Building Works for Non-Coders](HOW-AI-BUILDING-WORKS-FOR-NON-CODERS.md)** for what these tools can and can't do, then follow **[Getting set up](guides/getting-set-up.md)** to create your accounts and tools step by step.

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

1. **Everyone** reads this page, then **[Step 0: Getting comfortable](guides/step-0-getting-comfortable.md)**, skims the **[Glossary](GLOSSARY.md)**, and works through **[Getting set up](guides/getting-set-up.md)** so accounts and tools are ready.
2. Together, work through the **[Team Kickoff Checklist](checklists/team-kickoff.md)**.
3. Read the **[Example walkthrough](examples/EXAMPLE-walkthrough.md)** to see one full lap.
4. Start **[Step 1: Write the PRD](guides/step-1-write-the-prd.md)**, and keep going.

Feeling lost at any point? Open **[GUIDE-ME.md](GUIDE-ME.md)** and let an AI point you to the next step.

---

*Made for The Upskilling Labs. Copy this repo, make it your own, and go build something.*
