# Case Study README Template

> Your project's front door, written so it doubles as a portfolio piece. This becomes the `README.md` of your product repo, the first thing anyone sees, and the page a hiring manager reads to decide whether you can build and ship.

A `README.md` is the page GitHub shows automatically when someone opens your repository. Most are dry. Yours does double duty: it explains the product to a curious visitor, and it tells the story of what you built and the calls you made along the way. One file, two jobs.

**How to use this template.** Copy everything below the line into a file called `README.md` in the root of your *product* repo ([repository (repo)](../GLOSSARY.md)), the app you built, not this playbook. Then work through it section by section. Each section has an _italic instruction_ telling you what to write, followed by a quoted RecipeRoll example showing one way to do it. Replace both with your own words and delete the instruction lines as you go. A few sections also carry a short _What this signals to an employer:_ note, so you can see why that part is worth getting right.

This template pairs with [../guides/build-your-portfolio-piece.md](../guides/build-your-portfolio-piece.md), which walks through turning a finished project into something you can show off. Fill this in, then read that guide for how to talk about it.

Keep it honest and keep it tight. A reader should understand what you made, who it is for, and what you did in about two minutes.

---

# RecipeRoll

_State your product's name as an H1, then one plain sentence that says what it is and who it helps. No jargon. If a stranger can repeat it back after reading once, you nailed it._

> RecipeRoll is a friendly place to save your recipes and discover your friends'.

## Live demo

_Link to the deployed app so a reader can try it in one click, then leave a spot for a picture or a short recording. A working link plus a screenshot is the single most convincing thing on this page; it proves the thing is real. If you haven't put it online yet, see [../guides/step-8-share-and-go-live.md](../guides/step-8-share-and-go-live.md) for how to get a free public link._

> **Try it:** https://reciperoll.netlify.app
>
> `![RecipeRoll home page - a grid of recipe cards](docs/screenshot-home.png)`
>
> _Replace the line above with your own screenshot or a short screen recording. A 15-second clip of the main feature in action beats a wall of text._

## The problem

_In plain words, say who this is for and the everyday pain it takes away. Skip the grand mission statement. Name a real person and a real annoyance._

> Recipes you actually cook end up scattered: a screenshot here, a text from your sister there, a bookmark you'll never find again. RecipeRoll is for small groups of friends who cook and want one shared place to keep the recipes they love and see what everyone else is making. No more "send me that thing you made last week."

## What it does

_List the v1 features as a short, scannable list. These are the things that work today, not the dream version. Keep it to what you actually shipped._

> Version one (v1) lets you:
>
> - **Add a recipe** with a title, ingredients, and steps.
> - **Browse** every recipe the group has saved, newest first.
> - **Search** by ingredient, so "what can I make with chickpeas?" has an answer.

## How it's built

_Describe the tools and the setup plainly, the way you'd explain it to a friend who isn't technical. Name the kind of each tool, not just brand names. For the full menu of options and why teams pick them, point to [../tools/README.md](../tools/README.md)._

> RecipeRoll was built with an *AI builder* ([AI builder tool](../GLOSSARY.md)), which writes and edits the code from plain-English descriptions of what we wanted. The pieces:
>
> - **AI builder** — Claude Code, used by every teammate to do the actual building.
> - **Code home** — a GitHub repo, where all the work lives and comes together.
> - **Hosting** — Netlify's free tier, which puts the app online and rebuilds it automatically on every change, with a separate preview link for each [pull request](../GLOSSARY.md).
> - **Data store** — a lightweight hosted database ([database](../GLOSSARY.md)) holding the saved recipes.
>
> The whole [stack](../GLOSSARY.md) is free. See [../tools/README.md](../tools/README.md) for the options we weighed.

## My role and the team

_Be honest about who did what. Name your own contribution clearly and specifically, then credit your teammates. State plainly that the team used AI builders; that's normal and expected here, not something to hide._

> RecipeRoll was built by a team of four: Maya, Sam, Priya, and Devin. We each owned a feature and built it on our own [branch](../GLOSSARY.md), all of us working with AI builders to write the code.
>
> **My part (Maya):** I owned the *add a recipe* feature end to end, the form, the save, and the confirmation message, and I wrote the feature spec it was built from. I also reviewed Sam's browse-page pull request before it merged.

> _What this signals to an employer:_ that you can own a piece of real work, name your contribution without overclaiming, and credit a team honestly. Saying "I used an AI builder" is a plus, not a confession; it shows you can direct a modern tool to ship something that works.

## Key decisions and trade-offs

_Pick two or three real choices you faced and explain what you decided and why. The point isn't that you made the "right" call; it's that you made a call on purpose, with a reason, and knew what you were giving up. If you keep a [decision log](DECISIONS.md), pull the best ones from there._

> - **We allowed duplicate recipe names in v1.** Blocking duplicates meant building a check and an error message, and two people really might both have a "Banana Bread." We let them coexist to ship sooner, and noted we'd revisit it if it got confusing.
> - **We left accounts and photos for later.** Logins and image uploads are both real work, and neither is needed to prove the core idea: a shared, searchable recipe box. Cutting them kept v1 small enough to finish.
> - **We searched by ingredient, not by full text.** Ingredient search covered the question people actually ask ("what can I make with what's in the fridge?") and was simpler to get right than searching every word in every recipe.

> _What this signals to an employer:_ judgment. Anyone can add features; deciding what to leave out, and being able to explain why, is the harder and more valuable skill. This section shows you can scope work and reason about trade-offs.

## What I learned

_A few honest sentences. What surprised you, what was harder than expected, what you'd do differently. Real and specific beats polished and vague. It's fine, good even, to admit something didn't go smoothly._

> I learned that the slow part isn't the code, it's deciding what to build. Our first draft of the add-recipe form tried to do too much, and trimming it down taught me more than adding to it would have. I also learned to write a clear spec before asking the AI to build: the sharper my description, the closer the first result landed, and the less time I spent going back and forth.

> _What this signals to an employer:_ growth and self-awareness. A candidate who can name what they learned, and what they'd change, is someone who will keep getting better. Honesty here reads as confidence, not weakness.

## What's next

_Where you'd take it. The "Later" list, the features you parked, the things real users asked for. This shows the project is a living idea, not a one-off assignment._

> The Later list, roughly in order:
>
> - **Accounts**, so recipes belong to a person and groups stay private.
> - **Photos** on each recipe.
> - **Favorites and star ratings**, so the best recipes rise to the top.
> - **Full-text search** across steps and notes, not just ingredients.
>
> Early testers asked for photos first, so that's where we'd start.

## Run it locally (optional)

_A couple of plain steps for a curious visitor who wants to run the app on their own computer ([localhost](../GLOSSARY.md)). Keep it to the real commands. If you're not sure what they are, ask your AI builder to fill them in for your project._

> ```
> # 1. Copy the project to your computer
> git clone https://github.com/your-team/reciperoll.git
> cd reciperoll
>
> # 2. Install what it needs
> npm install
>
> # 3. Start it
> npm run dev
> ```
>
> Then open the address it prints (usually `localhost:3000`) in your browser. To save recipes you'll need the data store connected; see the notes in `.env.example`.

---

Filling this in for the first time? Read [../guides/build-your-portfolio-piece.md](../guides/build-your-portfolio-piece.md) for how to turn this page into a portfolio piece you're proud to send.
