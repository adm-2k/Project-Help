# 🧠 How Git Works (for Non-Coders)

> A calm, plain-English picture of how git and branches let your whole team build at the same time without ever overwriting each other.

You do not need to be technical to understand this. There is no code in this page, just a few useful pictures. By the end you will know what a [branch](GLOSSARY.md) is, what [main](GLOSSARY.md) is, and why none of this can break anything.

> 💡 **Why this matters:** Git is just a careful system for letting many people change the same project safely. Once you see the pattern, the scary words (branch, merge, conflict) become ordinary and friendly.

## 🎯 The problem git solves

Imagine four people sharing one document.

Maya, Sam, Priya, and Devin all open the same file at the same time. Maya rewrites the top. Sam rewrites the bottom. They both hit save.

Whoever saves last wins. The other person's work vanishes. No warning, no undo.

That is the problem. When a team builds software in one shared place, they need a way to all work at once **without** stomping on each other. Git is that way.

## 💬 The mental model

There are only two ideas to hold in your head.

### 1. "main" is the official version

> [main](GLOSSARY.md) is the one shared, always-working copy of your project that everyone trusts.

Think of `main` as the clean published version of a shared document. Nobody scribbles directly on it. It stays tidy and working at all times.

### 2. A "branch" is your private copy where you build safely

> A [branch](GLOSSARY.md) is your own personal copy of the whole project, split off from `main`, where you can change anything without affecting anyone else.

**Analogy 1 — parallel drafts of one shared document.** When you make a branch, it is like clicking "Make a copy" of the master document so you can scribble, rewrite, and experiment freely. Your scribbles are invisible to everyone else. When your draft is good, you propose folding your changes back into the master. That proposal is called a [pull request](GLOSSARY.md), and a teammate looks it over before it goes in.

**Analogy 2 — separate cutting boards in one kitchen.** `main` is the finished dish everyone will eat. Each cook gets their own cutting board (a branch) to chop and prep on. Maya preps on her board, Sam on his, nobody knocks elbows. When a cook's prep is ready, it gets added to the shared dish. Four cooks, one kitchen, zero chaos.

So in RecipeRoll, our team of four each gets their own branch:

| Person | Feature | Their branch |
| --- | --- | --- |
| Maya | Add a recipe form | `feature/add-recipe-form` |
| Sam | Browse all recipes | `feature/recipe-list` |
| Priya | Search by ingredient | `feature/search-by-ingredient` |
| Devin | Save favorites | `feature/favorites` |

All four build at the same time, each on their own copy, and `main` stays clean and working the whole time.

> 💡 **Why this matters:** Because you work on your own branch, you literally cannot break the shared version or lose a teammate's work. The worst case is that your own private copy gets messy, and that is easy to throw away and start fresh.

## 🔁 The everyday loop, in five plain steps

This is the rhythm your team repeats for every feature. Five steps.

1. **Get the latest `main`.** Pull down everyone's most recent finished work so you start from the current version.
2. **Make a branch.** Split off your own private copy to build on, named like `feature/add-recipe-form`.
3. **Build.** Make your changes with your AI builder (Claude Code, Cursor, etc.). Save your progress as you go.
4. **Open a pull request.** When your feature works, propose merging your branch back into `main` so a teammate can review it.
5. **Merge.** Once approved, your branch folds into `main`. Now your work is part of the official version, and everyone gets it the next time they do step 1.

Here is the whole loop as a picture. Time flows left to right. `main` runs across the top. Branches split off, get built, and merge back.

```
                feature/add-recipe-form
                   o───o───o
                  /         \
main ───o───────o───────────M─────────o───────►
         \                            (latest main,
          o───o───o                    everyone pulls
       feature/recipe-list             this next)
```

- `o` is a saved change (a [commit](GLOSSARY.md)).
- The line splitting downward is making a branch.
- `M` is the merge, where your finished branch joins `main`.
- After the merge, the next person gets that updated `main` when they do step 1 again.

> 💡 **Why this matters:** Every feature follows the exact same five steps. Once your team does it once, every future feature feels familiar.

The detailed walkthroughs live here:

- Steps 1 to 3 (get latest, branch, build): [guides/step-4-claim-and-build.md](guides/step-4-claim-and-build.md)
- Steps 4 and 5 (pull request and merge): [guides/step-6-review-and-merge.md](guides/step-6-review-and-merge.md)

## ⚠️ Merge conflicts, demystified

The phrase "merge conflict" sounds alarming. It is not.

> A [merge conflict](GLOSSARY.md) simply means two people changed the **same line** in the same file, and git is asking you which version to keep.

That is the entire thing. Git is not confused and nothing is broken. Git is just being careful. It refuses to guess between Maya's wording and Sam's wording, so it stops and asks a human.

A few reassurances:

- **It is normal.** On any active team, conflicts happen. They are a routine part of the loop, not a sign anyone did something wrong.
- **It is not dangerous.** Nothing is lost. Both versions are safely sitting there. You are only choosing which to keep, or how to combine them.
- **Your AI builder can resolve it for you.** Paste the conflict into your AI builder (Claude Code, Cursor, etc.) and ask it to walk you through choosing the right version. Use the ready-made prompt: [prompts/06-resolve-a-merge-conflict.md](prompts/06-resolve-a-merge-conflict.md).

So when you see "conflict," read it as "git has a quick question for you." Answer it, save, and carry on.

## 🖱️ You do not have to type commands

You can do all of this with buttons. You never need to memorize a single command.

We recommend either:

- **GitHub Desktop** — a free app with clear buttons for every step, or
- **Your AI builder's built-in git** — Claude Code, Cursor, and similar tools can do every step for you when you ask in plain English.

Here is every common action, what it is called, the GitHub Desktop button, and the underlying command. The command column is **optional reference only** — you can ignore it entirely.

| What you want to do | What it is called | GitHub Desktop button | Underlying command (optional) |
| --- | --- | --- | --- |
| Get the latest `main` | Pull | "Fetch origin" then "Pull origin" | `git pull` |
| Make a branch | Create a branch | "Current Branch" → "New Branch" | `git checkout -b feature/add-recipe-form` |
| Save a change | Commit | Type a summary, click "Commit to ..." | `git commit -m "Add recipe form"` |
| Share your branch | Push | "Publish branch" or "Push origin" | `git push` |
| Propose a merge | Open a pull request | "Create Pull Request" | (done on GitHub.com) |

> 💡 **Why this matters:** The same five actions, every time. Buttons or plain-English requests to your AI builder are all you need. The commands are there only if you ever get curious.

## ➡️ Where to go next

- See the build loop in action: [guides/step-4-claim-and-build.md](guides/step-4-claim-and-build.md)
- See review and merging in action: [guides/step-6-review-and-merge.md](guides/step-6-review-and-merge.md)
- Look up any term in plain English: [GLOSSARY.md](GLOSSARY.md)

You now understand the whole system. Branches are private copies, `main` is the shared official version, and merging is just folding good work back in. Nothing here can lose your teammates' work, and nothing here can break the project. Go build.
