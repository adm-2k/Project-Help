# Choosing Your Tools

_Last verified: 2026-06. Tool prices and free tiers change often, so re-check the linked sites and update this page each cohort (about quarterly)._

There are a lot of tools out there, and new ones launch every month. You do not need the "best" ones. You need one cheap, easy set that your whole team can agree on and stick with. A team that picks a decent set on Monday and starts building beats a team still comparing options on Friday.

This page helps you pick that set without getting stuck. Read the few questions below, land on a starter set, then dip into the detailed comparison pages only if you want to weigh your options.

---

## A few questions to point you the right way

Answer these together as a team. They route you to the right pieces.

| Question | If yes | If no |
|---|---|---|
| Does your idea need to store data that lasts, like accounts or saved entries? | You need a place to keep that data. See [data-and-backends.md](data-and-backends.md). | Skip the data piece for now. A simple site or tool is enough. |
| Will it ever make money, or hold real people's information? | Plan for a real login and a proper database from the start. Lean toward Supabase. | A lightweight data list like Airtable is fine to begin with. |
| Do you want zero installs, so everyone works in a browser? | Pick a browser-based AI builder. Nobody touches the [command line](../GLOSSARY.md). | A desktop tool is an option if a teammate wants to learn a little code. |

Most non-technical teams answer "yes, no, yes" — they have some data to store, are not charging money yet, and want everyone working in a browser. The starter stack below is built for exactly that team.

---

> Our default starter stack
>
> If you do not want to think hard about this, copy this set. It is opinionated on purpose, and the whole thing can be free.
>
> | Piece | What we suggest | Why |
> |---|---|---|
> | The thing you build with | An *[AI builder tool](../GLOSSARY.md)* that handles git for you: **Lovable** or **Bolt.new** | You describe the app, it builds it, and it saves your work to GitHub without you learning git commands |
> | The shared home for your code | A free **[GitHub](../GLOSSARY.md)** *[repository](../GLOSSARY.md)* | One trusted place everyone works from; your AI builder syncs here automatically |
> | Where it goes live | **Netlify** or **Cloudflare Pages** | Free hosting, plus a live preview link for every *[pull request](../GLOSSARY.md)* so the team can click and check work before it merges |
> | Where data lives (only if you need it) | **Supabase** for accounts and saved data, or **Airtable** for a simple list | Add this only if your answer to the first question above was "yes" |
>
> The whole stack can be free to start. If you outgrow an AI builder's free tier, expect around $25/month for the builder, with the rest still free.

---

## The detailed comparison pages

When you want to weigh options for one piece, open its page. Each one compares the realistic choices for a non-technical team and names a pick.

| Page | What it compares |
|---|---|
| [ai-builders.md](ai-builders.md) | The tools you prompt to write the app: Lovable, Bolt.new, Replit, Cursor, and more |
| [version-control-clients.md](version-control-clients.md) | Friendly ways to use git without typing commands, like GitHub Desktop |
| [hosting-and-deployment.md](hosting-and-deployment.md) | Where your app goes live so real people can use it: Netlify, Cloudflare Pages, and others |
| [data-and-backends.md](data-and-backends.md) | Where accounts and saved data live: Supabase, Airtable, and the trade-offs |
| [coordination-and-pm.md](coordination-and-pm.md) | How the team tracks who is doing what, from a shared board to GitHub Issues |

---

> Going further on GitHub: once your code lives on GitHub, you can also track your team's work there. Turn each task into a GitHub *[Issue](../GLOSSARY.md)* and lay them out on a Projects board, so everyone can see what is to-do, in progress, and done in the same place as the code. The [Break into tasks guide](../guides/step-3-break-into-tasks.md) shows how.
