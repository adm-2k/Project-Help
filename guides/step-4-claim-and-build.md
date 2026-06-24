# 🍳 Step 4: Claim Your Task and Build It on a Branch

> Pick up your assigned piece, build it with your AI on your own safe workspace, and stay in step with your team — without overwriting anyone.

**🎯 Goal:** Build your one assigned piece, on your own [branch](../GLOSSARY.md), so it works and is saved — without drifting from the plan or touching a teammate's files. **⏰ Time:** A few work sessions, spread over days. **👥 Who:** Each person individually (everyone does this for their own task).

> 💡 Before you start, run through the **[Before You Start a Task checklist](../checklists/before-you-start-a-task.md)**. It's a 60-second sanity check that saves hours.

## Why this matters

A [branch](../GLOSSARY.md) is your own private copy of the project where you can build and experiment without affecting anyone else. That means four people can build four features at the same time and nobody loses work. If you skip the branch and edit the shared copy directly — or go quiet for days — that's when teams clash and work gets lost. This step keeps everyone moving in parallel, safely.

## What you'll do

> ⚠️ New to branches, commits, and pulling? Read **[How Git Works for Non-Coders](../HOW-GIT-WORKS-FOR-NON-CODERS.md)** first. It explains every word below in plain English, with pictures. It's short.

### 1. 🔄 Get everyone's latest work first

Before you create anything, grab the newest version of the shared project. The shared, official copy of the project is called **main**. Pulling main means "download everyone's latest merged work onto my computer."

In **GitHub Desktop**: click the **Fetch origin** button, then **Pull origin** if it offers. In your **AI builder** (Claude Code, Cursor, etc.), just ask it to pull the latest main.

> Optional command-line reference (you can ignore this and use the buttons):
```
git checkout main
git pull
```

> 💡 **Why this matters:** Starting from yesterday's copy means you build on top of work that's already changed. Pulling first means your branch starts from the same place as everyone else's.

### 2. 🌿 Create your branch using the exact name from the task board

Your branch name was decided in Step 3 and written on the **[task board](../templates/task-board.md)**. Use that exact name — don't invent a new one. The convention is `feature/short-description` (lowercase words separated by dashes).

In **GitHub Desktop**: **Current Branch** → **New Branch**, type the name, click **Create Branch**. In your **AI builder**: ask it to create and switch to a new branch with that name.

> Optional command-line reference:
```
git checkout -b feature/your-task-name
```

> ⚠️ Make sure you created the branch *from* an up-to-date main (Step 1 above), not from someone else's branch.

### 3. 💬 Tell the AI exactly what to build

Open the build prompt: **[prompts/04-build-a-task-on-a-branch.md](../prompts/04-build-a-task-on-a-branch.md)**. Fill in the blanks and paste it into your AI builder. Point it at the **[PRD](../templates/PRD-template.md)** and at *your* specific task, and tell it clearly to stay in scope and not touch unrelated files.

A good build instruction always says three things:

1. **What** to build — copy your task's description from the task board.
2. **Where to look** — "Follow the PRD for the rules; build only my task."
3. **What NOT to do** — "Stay strictly in scope. Do not change files outside this feature. If something seems missing, ask me instead of guessing."

### 4. 🧱 Build in small steps and save often

Don't try to build the whole feature in one giant go. Ask the AI for one small, working piece at a time. Each time a small piece works, **save it** — saving a snapshot is called a [commit](../GLOSSARY.md).

In **GitHub Desktop**: your changes appear on the left; type a short message and click **Commit to feature/...**. In your **AI builder**: ask it to commit your changes with a short message.

Keep commit messages short and plain, for example:
```
Add the empty recipe form layout
Make the Save button store the recipe
```

> 💡 **Why this matters:** Small commits are like save points in a game. If something breaks, you can go back one step instead of losing everything.

### 5. ⬆️ Push your branch at least once a day

A [commit](../GLOSSARY.md) saves your work on *your computer*. **Pushing** uploads your branch to GitHub so it's backed up and your team can see it. Push at the end of every working session — at minimum, once a day.

In **GitHub Desktop**: click **Push origin** (the first time it says **Publish branch**). In your **AI builder**: ask it to push your branch.

> Optional command-line reference:
```
git push
```

### 6. 🔁 Pull main regularly and check for overlaps early

Every day or two, bring the team's newly merged work into your branch so you don't drift apart. After pulling main, paste the **[Keep Me In Sync prompt](../prompts/05-keep-me-in-sync.md)** into your AI to spot any overlap with a teammate's work *before* it becomes a problem.

> 💡 **Why this matters:** Catching an overlap on day two is a two-minute chat. Catching it on day ten is a tangle. Small, frequent syncs keep merging painless. (If the AI flags a real clash, that's a normal "[merge conflict](../GLOSSARY.md)" — easy to fix later, covered in Step 6.)

### 7. ✅ Test that your piece actually works

Open the app and use your feature the way a real person would. Don't just trust that the code "looks right" — click the buttons, type real text, and confirm it does what your task said it should. Check it against the success criteria in the PRD.

### 8. 🐛 Jot down bugs and ideas as you go

When you notice a bug, a rough edge, or a "we should do this later" idea, write it straight into the **[ISSUE-LOG](../templates/ISSUE-LOG.md)** so it isn't forgotten. Don't stop your build to fix unrelated things — log it and keep going.

## 🧑‍🍳 RecipeRoll example

Maya owns **Feature A — the "Add a recipe" form**. Here's her Step 4:

1. She opens GitHub Desktop and clicks **Fetch origin**, then **Pull origin**, so she has the team's latest main.
2. She creates a new branch named exactly **`feature/add-recipe-form`** (the name from the task board).
3. She pastes the build prompt, telling the AI: *"Build only the 'Add a recipe' form — title, ingredients, and steps fields, plus a Save button — following the RecipeRoll PRD. Stay in scope. Don't touch the browse page or search; those are teammates' files."*
4. She builds in small steps: first the empty form layout (commit), then making Save store the recipe (commit), each with a short message.
5. At the end of each day she clicks **Push origin** so her branch is backed up on GitHub.
6. Two days in, she pulls main and runs the Keep Me In Sync prompt; the AI confirms she and Sam aren't editing the same files. 👍
7. She tests it: she types a real recipe and clicks Save, confirming it's stored — matching the PRD's success criteria.
8. She notices the form lets you save with an empty title, jots *"Add-recipe form allows empty title — should it require one?"* into the ISSUE-LOG, and keeps building.

## Watch out

> ⚠️ **Common mistakes that bite teams here:**
> - **Building something that isn't in the PRD.** If it's not in your task, don't build it. "Wouldn't it be cool if…" ideas go in the **[ISSUE-LOG](../templates/ISSUE-LOG.md)**, not your branch.
> - **Editing files a teammate owns.** Stay inside your own feature. If you think you need to touch a shared file, message the team first.
> - **Going days without pushing.** Unpushed work isn't backed up and your team can't see it. Push at least once a day.
> - **Building from an old copy.** If you forgot to pull main before branching, your work starts out of date. Pull first.
> - **One giant commit at the end.** Save small and often, so a mistake costs you one step, not your whole day.

## You're done when

- [ ] Your task works when you actually use it in the app (checked against the PRD's success criteria).
- [ ] Your work is committed in small steps with short, clear messages.
- [ ] Your branch is **pushed** to GitHub (your team can see it).
- [ ] You've pulled main recently and there are **no unresolved overlaps** with teammates.
- [ ] Any bugs or "later" ideas you spotted are written in the **[ISSUE-LOG](../templates/ISSUE-LOG.md)**.

## Next

➡️ Your piece works and it's pushed? Time to propose it to the team: **[Step 5: Open a Pull Request](step-5-open-a-pull-request.md)**.

## Prompts & templates you'll use

- 💬 **[prompts/04-build-a-task-on-a-branch.md](../prompts/04-build-a-task-on-a-branch.md)** — tell the AI exactly what to build, in scope.
- 💬 **[prompts/05-keep-me-in-sync.md](../prompts/05-keep-me-in-sync.md)** — catch overlaps with teammates early.
- 📋 **[templates/ISSUE-LOG.md](../templates/ISSUE-LOG.md)** — log bugs and "later" ideas as you go.
- ✅ **[checklists/before-you-start-a-task.md](../checklists/before-you-start-a-task.md)** — the 60-second pre-flight check.
- 📖 **[How Git Works for Non-Coders](../HOW-GIT-WORKS-FOR-NON-CODERS.md)** — branches, commits, and pulling in plain English.
