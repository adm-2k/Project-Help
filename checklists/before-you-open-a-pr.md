# 🎯 Before You Open a Pull Request

> A quick check to run before you ask the team to review your work, so your pull request is clean, small, and easy to say yes to.

**Goal:** Make your pull request painless for a teammate to review and merge. **Time:** about 10 minutes. **Who:** each person, when their task is finished.

## 💬 Why this matters

A pull request (PR) is simply you saying "here's my finished piece — please check it and add it to the shared version." A small, tested, well-described PR gets reviewed in minutes and keeps `main` working. A messy one creates confusion and delays everyone. This list gets yours into great shape.

> 💡 **Tip:** A pull request is not scary — it's just a polite request to merge your branch. See the [glossary](../GLOSSARY.md) if the words feel new.

## ✅ Before you open the PR

- [ ] Your piece **actually works** and you tested it yourself (you clicked through it and saw it do the right thing)
- [ ] **Only your task's changes** are included — nothing unrelated snuck in
- [ ] You **pulled the latest `main` into your branch** and resolved any conflicts (a conflict is normal and fixable, see [the conflict prompt](../prompts/06-resolve-a-merge-conflict.md))
- [ ] You **updated the [ROADMAP](../templates/ROADMAP.md) or [ISSUE-LOG](../templates/ISSUE-LOG.md)** if this task changed either of them
- [ ] Your PR is **small and focused** — one task, not three
- [ ] You **wrote a clear description** of what changed and why — let [the PR prompt](../prompts/07-write-my-pr.md) help you
- [ ] You **linked the related task or issue** and **requested a reviewer**

> ⚠️ **Watch out:** Resist the urge to "just fix one more thing" while you're here. Extra, unrelated changes make a PR slow and risky to review. Keep it to your one task.

## 🍳 RecipeRoll example

Sam finishes Feature B, the "Browse all recipes" list page, on `feature/recipe-list`. He opens the page himself and confirms the recipes show up. He checks that only the list-page files changed, pulls the latest `main` into his branch (no conflicts this time), and uses the PR prompt to write: "Adds the Browse all recipes page that lists every saved recipe by title." He links the task board row, requests Maya as reviewer, and opens the PR.

## ➡️ You're done when

- [ ] Every box above is checked and your PR is ready to open

When all boxes are checked, follow **[Step 5: Open a pull request](../guides/step-5-open-a-pull-request.md)**.
