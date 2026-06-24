# AI Builder Tools

_Last verified: 2026-06. Tool prices and free tiers change often, so re-check the linked sites and update this page each cohort (about quarterly)._

An *[AI builder tool](../GLOSSARY.md)* is the thing you prompt to write your app. You describe what you want in plain English, and it does the typing. The tools below differ mostly in how much they hide from you: some run entirely in a browser and save your work to GitHub on their own, others are code editors that expect you to drive a little.

This page compares the realistic choices for a non-technical team. The "Handles git for you?" column matters most: if a tool manages *[branches](../GLOSSARY.md)* and *[pull requests](../GLOSSARY.md)* for you, nobody on your team needs to learn git commands.

| Tool | Cost (free tier -> first paid) | Ease for non-coders | Where it runs | Handles git for you? | Best for |
|---|---|---|---|---|---|
| Lovable | Free: 5 credits/day (about 150/mo) -> Pro $25/mo | High | Browser | Yes — two-way GitHub sync, branches and PRs | Non-coders who want a deployed full-stack app from a description |
| Replit (Agent) | Free limited tier -> Core $25/mo | High | Browser cloud editor, plus deploy | Yes — integrated GitHub | Fast prototypes, all-in-one |
| Bolt.new | Free: 1M tokens/mo (300K/day cap) -> Pro $25/mo | High | Browser | Yes — full GitHub integration, auto commit and push | Quick full-stack apps from a prompt |
| v0 (by Vercel) | Free: $5 credits + 7 messages/day | Medium-High | Browser | Yes — Git panel and GitHub sync | Generating polished screens, not whole apps on its own |
| Cursor | Free Hobby tier -> Pro $20/mo | Medium | Desktop app (a code editor) | No — you manage git | People willing to learn a bit of code |
| Claude Code | Pro $20/mo (Max $100-200) | Medium | Terminal, desktop, or editor | Yes — full git automation (commit, branch, PR) | Larger or existing codebases |
| Windsurf (now Devin Desktop) | Free light tier -> Pro $20/mo | Low-Medium | Desktop app | Partial | Developer-oriented work |

## Our pick for a first MVP

For a first *[MVP](../GLOSSARY.md)*, pick **Lovable** or **Bolt.new**. Both follow the same friendly loop: you describe the app, you get a deployed app back, and your work syncs to GitHub on its own. That last part is what makes them right for a non-technical team. You never touch a git command, your code still lands in your shared *[repository](../GLOSSARY.md)*, and your teammates can see it. Either one gets a small team from idea to something live faster than the desktop editors, which expect you to know your way around code.

> Watch out: do NOT build your project on Firebase Studio. It is being shut down in March 2027, and you do not want to move a half-built app off a dying tool mid-project. Also, the browser AI builders bill by usage (often measured in tokens or credits), so a heavy day of building can cost more than the headline monthly price suggests. Set a budget before you start, and check your usage as you go.

Whichever tool you pick, point it at your shared plan so everyone builds the same thing, not four different versions of it. See [Prepare AI-ready deliverables](../guides/prepare-ai-ready-deliverables.md) for how to hand your AI builder a plan it can actually follow.
