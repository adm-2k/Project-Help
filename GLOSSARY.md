# Glossary — Plain-English Dictionary

> Keep this open in a tab while you work. You do not need to memorize anything here. Glance back whenever a word looks unfamiliar.

This is the dictionary for the whole playbook. Every other guide links here the first time it uses a technical word. None of these terms are as scary as they sound, and each one comes with an everyday comparison.

Terms are in alphabetical order.

> Going further on GitHub: when you want hands-on practice, GitHub Skills offers free, professional-grade courses at https://skills.github.com, and you can keep the one-page command reference handy from the Git cheat sheet at https://education.github.com/git-cheat-sheet-education.pdf.

---

**AI builder tool**
A program that writes and edits software for you when you describe what you want in plain English. Think of it as a capable assistant who can talk an idea through and do the typing. This playbook stays tool-agnostic and says "your AI builder (Claude Code, Cursor, etc.)" — use whichever one your team picked. It is the tool you will reach for on almost every page.

**AI context file**
A short file in your project that tells any AI builder the essentials: what you are building, where the plan lives, and the house rules to follow. You write it once, then save it under the name your tool reads automatically, `CLAUDE.md` for Claude Code, `AGENTS.md` for many other tools, or a rules file for Cursor. It is how every teammate's AI builds toward the same goal instead of drifting apart. Set one up in [guides/prepare-ai-ready-deliverables.md](guides/prepare-ai-ready-deliverables.md).

**Backend**
The behind-the-scenes part of an app that stores and serves data: accounts, saved entries, and the like, as opposed to the screens you see. Think of a restaurant kitchen behind the dining room. Not every first project needs one; if your app saves things or lets people log in, it does. Options are compared in [tools/data-and-backends.md](tools/data-and-backends.md).

**Branch**
A safe, separate copy of the project where you can make changes without touching anyone else's work. Picture each person getting their own photocopy of a shared notebook to scribble in; nobody's notes mess up anyone else's until you decide to combine them. Each teammate builds their own feature on their own branch, so you can all work at the same time without stepping on each other. See the picture-friendly explanation in [HOW-GIT-WORKS-FOR-NON-CODERS.md](HOW-GIT-WORKS-FOR-NON-CODERS.md).

**Clone**
Making your own full copy of a project from GitHub onto your computer so you can work on it. Like downloading a shared document so you have it locally, except it stays connected to the original. Cloning is how you get the project onto your machine the first time.

**Codebase**
All the files that make up your software: the words, the logic, the bits and pieces that run the app. Think of it as the full manuscript of a book, every chapter and footnote together.

**Commit**
A saved snapshot of your changes with a short note describing what you did. Like hitting save on a document, but you also leave a sticky note saying "added the recipe form." Commits let you and your team see the history of what changed and roll back if needed. Many small commits beat one giant one.

**Database**
An organized place where an app keeps information that needs to last, like a giant, searchable spreadsheet the app reads from and writes to. Saved recipes, user accounts, and favorites all live in one. Beginner-friendly options are compared in [tools/data-and-backends.md](tools/data-and-backends.md).

**Default branch**
The one official, trusted branch that everyone's finished work eventually flows back into. On most projects it is called `main` (see **main** below). Think of it as the master copy of the shared notebook that everyone agrees is the real one.

**Deploy / ship**
Putting your software somewhere real people can use it, often a website. "Ship it" means "make it live," like sending a finished newsletter to subscribers instead of leaving the draft on your desk. Building is half the work; shipping is when your app becomes real for actual users.

**Diff**
A side-by-side view of exactly what changed: what was added, what was removed. This is the "track changes" of code, showing the before and after. When you review a teammate's work, the diff is what you actually read to understand what they did.

**Fork**
Your own separate copy of someone else's project on GitHub, which you can change freely. Like taking a recipe and making your own version of it in your own cookbook. Most small teams work with branches inside one shared project and won't need forks, but you may see the word.

**Free tier**
The free level of a paid online service, enough to build and run a small project at no cost. Most tools in this playbook have one. Watch the limits (how much you can use before it asks you to pay), and note that some free tiers forbid commercial use, meaning anything that makes money. See [tools/README.md](tools/README.md).

**Git**
The behind-the-scenes system that tracks every change, every branch, and every version of your project over time. It is like an *Undo you can never lose* — an extremely thorough memory that never forgets who changed what and when. You rarely talk to git directly; your AI builder or GitHub Desktop does it for you. For a calm, no-jargon mental model, read [HOW-GIT-WORKS-FOR-NON-CODERS.md](HOW-GIT-WORKS-FOR-NON-CODERS.md). You don't need to master git. Trust it as your safety net.

**GitHub**
A website where your project lives online so your whole team can share it, see each other's work, and keep one trusted copy. Think of it as *Google Docs for code*: a shared place to work on the same project, plus tools for reviewing and discussing changes. It is your team's home base, where branches, pull requests, and issues all live.

**GitHub Desktop**
A free app with simple buttons for the most common git actions, so you don't have to type any commands. Like a remote control for git: click `Commit`, click `Push`, done. It is the gentlest way to do git. Whenever this playbook shows a git command, you can usually click a button in GitHub Desktop instead.

**Issue**
A written note on GitHub describing a bug to fix or an idea to build, so nothing gets forgotten. Like a ticket on a help desk or a card on a to-do board. Our running example logs this one: "Search is case-sensitive, so typing `Tomato` misses `tomato`." Issues keep your team's bugs and ideas in one trackable place instead of scattered across chats.

**Localhost**
Your app running only on your own computer, where only you can see it, usually at an address like `localhost:3000`. Like a dress rehearsal in an empty theater before opening night. To let other people use it, you deploy it (see **Deploy / ship**). [Step 8](guides/step-8-share-and-go-live.md) covers going from localhost to a shareable link.

**main**
The usual name for the **default branch**, the one trusted, official version of your project that finished work merges back into. Think of `main` as the "real" copy everyone agrees on.

> Watch out: you generally don't build directly on `main`. You build on your own branch, then merge into `main` after review.

**Merge**
Combining the changes from one branch into another, so two streams of work become one. Like taking everyone's separate notes and blending them back into the master notebook. Merging is how your finished feature joins the rest of the team's work.

**Merge conflict**
What happens when two people changed the very same lines and git can't tell which version to keep, so it asks a human to choose. Think of two editors who both rewrote the same sentence; someone picks the final wording. Conflicts are normal, and they are fixable, especially with your AI builder helping. We walk you through one in [HOW-GIT-WORKS-FOR-NON-CODERS.md](HOW-GIT-WORKS-FOR-NON-CODERS.md).

**Milestone**
A named group of work that marks a meaningful point, like "v1 launch." Think of it as a finish line you are all running toward together. Milestones help your team agree on what "done enough to ship" looks like.

**MVP (Minimum Viable Product)**
The smallest version of your app that is genuinely useful: the core, with the nice-to-haves saved for later. Like opening a café with great coffee and a few pastries before adding a full lunch menu. In our running example, the RecipeRoll MVP is add a recipe, browse all recipes, and search by ingredient. Accounts, photos, and ratings are saved for later. A tight MVP is how a small team actually finishes and ships.

**Owner**
The one person responsible for a particular feature or task. Like the lead chef for one dish: others can help, but one person makes sure it gets done. In RecipeRoll, Maya owns the "Add a recipe" form, Sam owns "Browse all recipes," Priya owns "Search by ingredient," and Devin owns "Save favorites." Clear ownership means nothing falls through the cracks and no two people accidentally build the same thing.

**PRD (Product Requirements Document)**
A short, plain document that says what you are building, for whom, and what counts as success, before anyone writes a line of code. Like a recipe card for the whole project: ingredients, steps, and what the finished dish should look like. A clear PRD prevents confusion and rework, and it is the most useful thing you can do before building. Learn to write one in [guides/step-1-write-the-prd.md](guides/step-1-write-the-prd.md).

**Preview deployment**
A private, live web version of one pull request, with its own link, created automatically by hosts like Netlify, Vercel, and Cloudflare Pages. It lets your reviewer click and try a change before it merges, instead of imagining how it works. A small thing that makes team review far easier. See [tools/hosting-and-deployment.md](tools/hosting-and-deployment.md).

**Prompt**
The instructions you type to your AI builder telling it what you want. Like a clear request to a skilled assistant: the more specific and friendly, the better the result. Good prompts are the main way you talk to your AI builder, so this playbook hands you tested ones to copy and paste — see [prompts/README.md](prompts/README.md).

**Pull**
Bringing the latest changes from GitHub down to your computer, so your copy is up to date. Like refreshing a shared document to see everyone's recent edits. Pulling often keeps you in sync with your team and prevents surprises later.

**Pull request (PR)**
A formal way of saying "I've finished my work on my branch. Please review it and merge it in." It bundles up your changes so a teammate can look them over before they join `main`. Think of it as handing in your draft chapter with a note: "ready for your eyes." Pull requests are how your team reviews and approves each other's work safely. Open your first one with [guides/step-5-open-a-pull-request.md](guides/step-5-open-a-pull-request.md).

**Push**
Sending your saved commits from your computer up to GitHub, so your team can see them. The opposite of **pull**, like uploading your edits back to the shared folder. Until you push, your work lives only on your machine; pushing shares it and backs it up.

**Repository (repo)**
The whole project folder living on GitHub: all the files, the full history, every branch. Think of it as the master binder that holds the entire project. "The repo" is shorthand for "our project on GitHub," and you will hear it constantly.

**Roadmap**
A living list of what is done, what is in progress, and what is coming next. Like a journey map showing where you have been and where you are heading. The roadmap keeps everyone pointed at the same destination and shows progress at a glance.

**Scope**
The agreed boundary of what you will and won't build right now. Like deciding the guest list for a dinner party: you can't invite everyone, so you choose on purpose. In RecipeRoll, accounts, photos, ratings, and comments are deliberately out of scope for v1.

> Watch out: "scope creep" is when little extras quietly pile on until nothing ships. Naming your scope out loud protects your launch.

**Source of truth**
The one document everyone, and every AI tool, treats as correct when they disagree. In this playbook it is your `PRD.md` plus the [AI context file](guides/prepare-ai-ready-deliverables.md). Keep it in one place and keep it current, so teammates and their AI builders all aim at the same goal.

**Spec (feature spec)**
A short, one-page description of a single feature: what it does, who it is for, the files it touches, and when it is done. It gives your AI a tight, unambiguous brief for one task. See [templates/feature-spec.md](templates/feature-spec.md).

**Stack**
The set of tools you choose to build with, stacked together: an AI builder, a place to host the app, and somewhere to store data. You do not need the "best" stack, just one cheap, easy set your team agrees on. [tools/README.md](tools/README.md) recommends a starter stack.

**Terminal / command line**
A plain text window where you type commands to your computer instead of clicking buttons. It looks bare and old-fashioned, but it is another way to give instructions. You can do almost everything in this playbook without it, since GitHub Desktop and your AI builder cover the basics. We show commands only as optional reference.

**Test**
A small automatic check that confirms a piece of your app does what it should. Like a taste-test before serving: if something is off, the test catches it before your users do. Tests give you confidence that new changes didn't quietly break something that used to work.

---

Back to the [README](README.md) for the full map of the playbook.
