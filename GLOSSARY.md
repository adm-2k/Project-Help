# 📖 Glossary — Plain-English Dictionary

> Keep this open in a tab while you work. You do not need to memorize anything here — just glance back whenever a word looks unfamiliar.

This is the friendly dictionary for the whole playbook. Every other guide links here the first time it uses a technical word. None of these terms are as scary as they sound, and we explain each one with an everyday comparison.

Terms are listed in alphabetical order.

---

**AI builder tool**
A program that writes and edits software for you when you describe what you want in plain English. Think of it as a very capable assistant who can both talk things through and do the typing. Throughout this playbook we stay tool-agnostic and say "your AI builder (Claude Code, Cursor, etc.)" — use whichever one your team picked.

> 💡 Why you care: this is the main tool you'll use to actually build features, so you'll see its name on almost every page.

**Branch**
A safe, separate copy of the project where you can make changes without touching everyone else's work. Imagine each person gets their own photocopy of a shared notebook to scribble in; nobody's notes mess up anyone else's until you decide to combine them.
See the gentle, picture-friendly explanation in [HOW-GIT-WORKS-FOR-NON-CODERS.md](HOW-GIT-WORKS-FOR-NON-CODERS.md).

> 💡 Why you care: each teammate builds their own feature on their own branch, so you can all work at the same time without stepping on each other.

**Clone**
Making your own full copy of a project from GitHub onto your computer so you can work on it. Like downloading a shared document so you have it locally, except it stays connected to the original.

> 💡 Why you care: cloning is how you get the project onto your machine the very first time.

**Codebase**
All the files that make up your software — the words, the logic, the bits and pieces that run the app. Think of it as the full manuscript of a book: every chapter and footnote together.

**Commit**
A saved snapshot of your changes, with a short note describing what you did. Like hitting "save" on a document, but you also leave a sticky note saying "added the recipe form."

> 💡 Why you care: commits let you and your team see the history of what changed and roll back if needed. Many small commits are better than one giant one.

**Default branch**
The one official, trusted branch that everyone's finished work eventually flows back into. On most projects it is called `main` (see **main** below). Think of it as the master copy of the shared notebook that everyone agrees is the real one.

**Deploy / ship**
Putting your software somewhere real people can use it (often a website). "Ship it" just means "make it live." Like sending a finished newsletter out to subscribers instead of keeping the draft on your desk.

> 💡 Why you care: building is only half the fun — shipping is when your app becomes real for actual users.

**Diff**
A side-by-side view of exactly what changed: what was added, what was removed. Like "track changes" in a word processor, showing the before and after.

> 💡 Why you care: when you review a teammate's work, the diff is what you actually read to understand what they changed.

**Fork**
Your own separate copy of someone else's project on GitHub, which you can change freely. Like taking a recipe and making your own personal version of it in your own cookbook. Most small teams work with branches inside one shared project and won't need forks — but you may see the word.

**Git**
The behind-the-scenes system that tracks every change, every branch, and every version of your project over time. Think of it as an extremely thorough memory that never forgets who changed what and when. You rarely talk to git directly — your AI builder or GitHub Desktop does it for you.
For a calm, no-jargon mental model, read [HOW-GIT-WORKS-FOR-NON-CODERS.md](HOW-GIT-WORKS-FOR-NON-CODERS.md).

> 💡 Why you care: git is the safety net that makes teamwork (and undoing mistakes) possible. You don't need to master it — just trust it.

**GitHub**
A website where your project lives online so your whole team can share it, see each other's work, and keep one trusted copy. Think of it as the shared cloud folder for your code, plus tools for reviewing and discussing changes.

> 💡 Why you care: GitHub is your team's home base — it's where branches, pull requests, and issues all live.

**GitHub Desktop**
A free app with simple buttons for the most common git actions, so you don't have to type any commands. Like a friendly remote control for git: click "commit," click "push," done.

> 💡 Why you care: it's the gentlest way to do git. Whenever this playbook shows a git command, you can usually click a button in GitHub Desktop instead.

**Issue**
A written note on GitHub describing a bug to fix or an idea to build, so nothing gets forgotten. Like a ticket on a help desk, or a card on a to-do board.
Our running example logs this one: "Search is case-sensitive, so typing Tomato misses tomato."

> 💡 Why you care: issues keep your team's bugs and ideas in one tidy, trackable place instead of scattered across chats.

**main**
The usual name for the **default branch** — the one trusted, official version of your project that finished work merges back into. Think of `main` as the "real" copy everyone agrees on.

> ⚠️ Watch out: you generally don't build directly on `main`. You build on your own branch, then merge into `main` after review.

**Merge**
Combining the changes from one branch into another, so two streams of work become one. Like taking everyone's separate notes and carefully blending them back into the master notebook.

> 💡 Why you care: merging is how your finished feature joins the rest of the team's work.

**Merge conflict**
What happens when two people changed the very same lines and git can't tell which version to keep, so it asks a human to choose. It's completely normal and easy to fix — think of two editors who both rewrote the same sentence; someone just picks the final wording.
We walk you through it gently in [HOW-GIT-WORKS-FOR-NON-CODERS.md](HOW-GIT-WORKS-FOR-NON-CODERS.md).

> 💡 Why you care: conflicts sound scary but they're routine and quick to resolve, especially with your AI builder helping. Don't fear them.

**Milestone**
A named group of work that marks a meaningful point, like "v1 launch." Think of it as a finish line you're all running toward together.

> 💡 Why you care: milestones help your team agree on what "done enough to ship" looks like.

**MVP (Minimum Viable Product)**
The smallest version of your app that's genuinely useful — the core, with the nice-to-haves saved for later. Like opening a café with great coffee and a few pastries before adding a full lunch menu.
In our running example, the RecipeRoll MVP is: add a recipe, browse all recipes, and search by ingredient. Accounts, photos, and ratings are saved for "Later."

> 💡 Why you care: a tight MVP is how a small team actually finishes and ships something real.

**Owner**
The one person responsible for a particular feature or task. Like the lead chef for one dish — others can help, but one person makes sure it gets done.
In RecipeRoll, Maya owns the "Add a recipe" form, Sam owns "Browse all recipes," Priya owns "Search by ingredient," and Devin owns "Save favorites."

> 💡 Why you care: clear ownership means nothing falls through the cracks and no two people accidentally build the same thing.

**PRD (Product Requirements Document)**
A short, plain document that says what you're building, for whom, and what counts as success — before anyone writes a line of code. Like a recipe card for your whole project: ingredients, steps, and what the finished dish should look like.
Learn to write one in [guides/step-1-write-the-prd.md](guides/step-1-write-the-prd.md).

> 💡 Why you care: a clear PRD prevents confusion and rework. It's the single most useful thing you can do before building.

**Prompt**
The instructions you type to your AI builder telling it what you want. Like a clear request to a skilled assistant: the more specific and friendly, the better the result.
This playbook gives you ready-made prompts to copy and paste — see [prompts/README.md](prompts/README.md).

> 💡 Why you care: good prompts are the main way you "talk" to your AI builder, so we hand you tested ones for every step.

**Pull**
Bringing the latest changes from GitHub down to your computer, so your copy is up to date. Like refreshing a shared document to see everyone's recent edits.

> 💡 Why you care: pulling often keeps you in sync with your team and prevents surprises later.

**Pull request (PR)**
A polite, formal way of saying "I've finished my work on my branch — please review it and merge it in." It bundles up your changes so a teammate can look them over before they join `main`. Think of it as handing in your draft chapter with a note: "ready for your eyes."
Open your first one with [guides/step-5-open-a-pull-request.md](guides/step-5-open-a-pull-request.md).

> 💡 Why you care: pull requests are how your team reviews and approves each other's work safely. They're the heart of good teamwork.

**Push**
Sending your saved commits from your computer up to GitHub, so your team can see them. The opposite of **pull** — like uploading your edits back to the shared folder.

> 💡 Why you care: until you push, your work only lives on your machine. Pushing shares it (and backs it up).

**Repository (repo)**
The whole project folder living on GitHub: all the files, the full history, every branch. Think of it as the master binder that holds the entire project.

> 💡 Why you care: "the repo" is just shorthand for "our project on GitHub." You'll hear it constantly.

**Roadmap**
A simple, living list of what's done, what's in progress, and what's coming next. Like a journey map showing where you've been and where you're heading.

> 💡 Why you care: the roadmap keeps everyone pointed at the same destination and shows progress at a glance.

**Scope**
The agreed boundary of what you will and won't build right now. Like deciding the guest list for a dinner party: you can't invite everyone, so you choose on purpose.
In RecipeRoll, accounts, photos, ratings, and comments are deliberately out of scope for v1.

> ⚠️ Watch out: "scope creep" is when little extras quietly pile on until nothing ships. Naming your scope out loud protects your launch.

**Terminal / command line**
A plain text window where you type commands to your computer instead of clicking buttons. It looks bare and old-fashioned, but it's just another way to give instructions.

> 💡 Why you care: you can do almost everything in this playbook without it — GitHub Desktop and your AI builder cover the basics. We only show commands as optional reference.

**Test**
A small automatic check that confirms a piece of your app does what it should. Like a taste-test before serving: if something's off, the test catches it before your users do.

> 💡 Why you care: tests give you confidence that new changes didn't quietly break something that used to work.

---

⬅️ Back to the [README](README.md) for the full map of the playbook.
