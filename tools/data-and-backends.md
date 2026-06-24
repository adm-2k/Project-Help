# Storing Data (Databases and Backends)

_Last verified: 2026-06. Tool prices and free tiers change often, so re-check the linked sites and update this page each cohort (about quarterly)._

Many first MVPs need somewhere to keep information that has to outlive a single visit: user accounts, saved entries, anything a person types in and expects to find again later. That "somewhere" is a *[database](../GLOSSARY.md)*, and the service that holds it is often called a *[backend](../GLOSSARY.md)*. This page lists the beginner-friendly options that have a free tier, so your team can start without paying anything.

## Do you even need one?

Not every app does. Here is the simple test:

- If users **save things or log in** — accounts, posts, bookmarks, orders, comments — then yes, you need a place to store data.
- If your app is **purely informational** — a landing page, a brochure site, a one-page tool that does not remember anything between visits — you can skip this for now and add it later if your idea grows.

When in doubt, ask whether anything a user does should still be there tomorrow. If the answer is yes, you need one of the tools below.

## The realistic choices

| Tool | Free tier | Non-coder friendly | Best for |
|---|---|---|---|
| Airtable | Free: 5 editors, 1,000 records per base, 2 GB attachments | Highest — works like a spreadsheet | A simple data list, a directory, or content the team edits by hand |
| Supabase | Free: 500 MB database, 1 GB file storage, ~50,000 monthly users, 2 projects | High — visual dashboard, though a real database underneath | The default for an app that needs accounts and saved data |
| Firebase (Firestore) | Free Spark plan: 1 GB stored, 50,000 reads/day, 20,000 writes/day | High — visual console | General app data, but free file Storage was removed in Feb 2026, so it is weaker for image-heavy apps now |
| Neon | Free: 0.5 GB per project, scales to zero | Medium — a developer database you query with SQL | When a developer is helping |

## Our pick

Choose **Supabase** if your app needs accounts or saved data. It gives you a real database and a login system, but wraps them in a visual dashboard you can click around in, so it does not feel like developer territory on day one.

Choose **Airtable** if you only need a shared, editable data list. It feels exactly like a spreadsheet, so the whole team can add and fix data by hand with no learning curve.

Most *[AI builder tools](../GLOSSARY.md)* connect to Supabase easily. You usually do not have to set up the wiring yourself: ask your AI builder to "connect this app to Supabase and store the data there," and it will handle the plumbing for you.

> Tip: pick your data tool BEFORE you build much. Moving data from one tool to another later is slow and error-prone, so a five-minute decision now saves you a painful migration after you have real users.
