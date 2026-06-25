# Turn Your Project Into a Portfolio Piece

> A finished thing you can explain, and prove you helped build, beats a stack of certificates. This guide turns the project you just shipped into evidence employers can see.

You did the hard part already. You took an idea, wrote a plan, split the work, built a feature on your own [branch](../GLOSSARY.md), reviewed a teammate's [pull request](../GLOSSARY.md), and shipped something real. That is exactly what hiring managers are trying to find out about you, and most candidates can only talk about it in the abstract.

A certificate says you sat through a course. A working project says you can ship something, make decisions, work on a team, and explain your choices. The difference matters more every year. This guide does not ask you to learn anything new. It helps you package what you already have so the right people notice it.

> Tip: Do this while the project is fresh. The decisions and the small dramas (the bug, the scope cut, the merge conflict) are vivid now and fuzzy in three months. Capture them today.

## Your README is your front door

When someone clicks your project on GitHub, the `README.md` is the first and often the only thing they read. A hiring manager will give it about twenty seconds before deciding whether to keep going. So your README is not documentation. It is a one-page case study with your name on it.

Most beginner READMEs read like setup instructions: "Run `npm install`, then `npm start`." That answers a question nobody asked. Rewrite yours as a case study using the template at [`../templates/case-study-README.md`](../templates/case-study-README.md). Copy it, fill in your real details, and lead with the story, not the commands.

In the first twenty seconds, a hiring manager is scanning for four things. Put all four near the top:

- **What it does** — one plain sentence a non-technical person understands. "A friendly place to save your recipes and discover your friends'."
- **A live link or a screenshot** — proof it is real, not a folder of files. A link they can click beats a paragraph describing what they would see.
- **Your role** — what *you* did on a team, in one line. Not "we built," but "I led the plan and owned the add-a-recipe form."
- **The decisions you made** — one or two real choices and the trade-off behind each. This is the part that separates you from someone who only followed a tutorial.

> Watch out: Setup instructions still belong in the README, just lower down. A reader who wants to run it will scroll. A reader deciding whether you are worth a call will not.

## Tell the story: problem, approach, outcome

A good case study has a shape. Three beats, in order, and you can write each in a few sentences.

**Problem.** Who was stuck, and why did it matter? Name a real person or a real frustration, not "users want a better experience." The more specific, the more it sounds like you understood the point of the work.

**Approach.** What did you build, and what were the interesting choices? This is where you show judgment. Mention a trade-off you made on purpose, including what you decided *not* to build. Saying "we left accounts and photos for later so we could ship the core" tells a reader you can scope work, which is rarer and more valuable than knowing any tool.

**Outcome.** What actually shipped, and what did you learn? "Deployed live, three friends added recipes the first evening" beats "successfully completed the project." If you would do something differently next time, say so. It reads as honest and self-aware, never as weakness.

Here is the shape filled in for RecipeRoll:

> Home cooks keep recipes scattered across screenshots, bookmarks, and texts, and can never find the one they want when they are standing in the kitchen. Our four-person team built RecipeRoll, a simple web app to save recipes and search them by ingredient. We deliberately scoped v1 down to add, browse, and search, and left accounts, photos, and ratings for later, so we could actually ship. We made a real call early on, allowing duplicate recipe names to keep the first version simple, and logged why. It went live in two weeks, and by launch evening there were recipes in it that none of us had written.

Notice how short that is, and how much it tells you: the problem is concrete, the scope decision shows judgment, and the outcome is real. That is the whole job.

## Write resume bullets that show impact

A resume bullet has a job: in one line, show that you did something real and it mattered. The formula:

**Strong verb + what you did + the result or skill it shows.**

The weak versions are vague and passive. The strong versions claim a specific action and attach an outcome. Three rewrites, all from RecipeRoll:

- Weak: "Helped make a recipe website."
  Strong: "Led the product requirements and shipped the add-and-search flow of a four-person, AI-built web app, deployed live with a preview link for every change."

- Weak: "Worked on the search feature with the team."
  Strong: "Caught a case-sensitivity bug in code review that hid matching recipes, logged it, and confirmed the fix before it reached the live site."

- Weak: "Used GitHub for version control."
  Strong: "Coordinated four parallel features using branches and pull-request reviews, keeping the main version working throughout a two-week build."

Each strong version names a verb (led, caught, coordinated), a concrete thing you did, and what it produced or proved. None of them inflate. They just stop hiding the good parts.

> Watch out: Claim your real role, and only your real role. If you led the plan, owned one feature, and reviewed pull requests, say exactly that. And state plainly that your team used AI builders to write the code. In 2026 that is a strength, not a secret. Employers know these tools exist and increasingly expect you to use them well. What sinks a candidate is the gap that opens in an interview when "I built a recipe app from scratch" meets "walk me through how the search function works." Claim what you did, name your tools, and you will never have to backfill a story you cannot defend.

## Prepare two or three interview stories (STAR)

When an interviewer asks "tell me about a time you...", they want a small, true story with a shape. *STAR* is that shape:

- **Situation** — the context, in a sentence.
- **Task** — what you needed to do or decide.
- **Action** — what *you* did (not the team, you).
- **Result** — how it turned out, and what you learned.

Prepare two or three of these before any interview, so you are not inventing them on the spot. Here is the template:

> **Situation:** While building [project], we hit [the moment].
> **Task:** I needed to [decide / fix / resolve] [the thing].
> **Action:** I [the specific steps you personally took].
> **Result:** [What happened], and I learned [the takeaway].

The good news: you already produced the evidence. Your [decisions log](../templates/DECISIONS.md), your pull requests, and your [issue log](../templates/ISSUE-LOG.md) are the receipts behind these stories. An interviewer who senses you are reading from a real record, not a script, trusts you more. Three examples, each drawn from a real RecipeRoll artifact:

**A scope decision (from the decisions log).**
> **Situation:** While planning RecipeRoll, our reviewer asked what should happen when two recipes share a name, like two "Banana Bread" entries.
> **Task:** I had to decide whether to handle duplicate names now or save it for later, without stalling the build.
> **Action:** I weighed the options with the team, chose to allow duplicates in v1 to keep it simple, and wrote the decision and the reasoning in our decisions log so nobody would reopen it.
> **Result:** We shipped on time, and when the question came up again later we had the answer on record. I learned that writing a decision down is what makes it stick.

**Catching a bug in review (from the issue log).**
> **Situation:** I was reviewing the search feature before it merged.
> **Task:** I needed to confirm it actually worked, not just trust the description.
> **Action:** I tested it the way a real user would and found that searching "Tomato" missed a recipe saved as "tomato." I logged it as a bug with steps to reproduce, and checked the fix before approving.
> **Result:** The case-sensitivity bug never reached our users. I learned that reviewing means trying the thing, not skimming it.

**Resolving a disagreement or a conflict.**
> **Situation:** Two of us had changed the same part of the project, and the work would not combine cleanly.
> **Task:** We needed to merge both pieces without losing either person's work or stalling everyone else.
> **Action:** I walked through the conflict with my AI builder, compared both versions line by line, kept the parts that mattered from each, and confirmed the result still ran before merging.
> **Result:** Both features landed and the main version stayed working. I learned that a [merge conflict](../GLOSSARY.md) is a normal, fixable conversation, not a disaster.

> Tip: Open the actual files before your interview. Re-reading your real decisions log and issue log refreshes the small details (dates, who raised what) that make a story sound lived rather than rehearsed.

## Show, don't tell: the demo

Telling someone your app works is fine. Letting them watch it work is far better. Give them both a live link and a short recording.

The live link is the strongest proof you have. If you shipped using [Step 8: Share it and go live](../guides/step-8-share-and-go-live.md), you already have a public web address. Put it at the top of your README and in your resume header. A link that opens in one click does more than any paragraph.

A recording covers the case where the link is down or the interviewer is offline. Record a two-minute screen walkthrough, with or without your voice. What to show:

- The one thing that matters, done start to finish. For RecipeRoll: add a recipe, then find it by searching one of its ingredients. The core promise, working.
- The live version, not your local one, so it is obviously real.

What to skip:

- Setup, installs, sign-in screens, and anything slow. Cut straight to the value.
- Apologies and throat-clearing. No "this part is a bit rough." Show the part that works and stop.

Two tight minutes that show the app doing its job beats ten rambling ones that show everything.

## Talking about it elsewhere

**On LinkedIn,** keep it short, specific, and honest. A post or a project entry like: "I led the product plan and built the add-and-search flow of RecipeRoll, a recipe app my four-person team shipped using AI builders. Live here: [link]. The most useful thing I learned was cutting scope to actually ship." It names your role, names your tools, and links to proof. That is everything a reader needs.

**In a cover line,** weave the same truth into a sentence: "I recently helped a small team take a recipe app from a one-page plan to a live product, where I led the requirements and owned the add-a-recipe feature; we used AI builders to write the code and standard team practices to keep the work safe and reviewable." One sentence, real role, real tools, real outcome.

## Honesty and integrity

Represent your work exactly as it happened. You led the plan or you did not. You owned a feature or you helped with one. Your team used AI builders or it wrote every line by hand. Say the true version every time, in your README, your resume, your interviews, and your posts.

This is not only the right thing, it is the smart thing. Interviews are designed to find the seam between what you claimed and what you can defend, and a stretched claim almost always tears there. The candidate who says "I led the requirements, owned one feature, and our team used AI builders to write the code" sounds exactly as capable in the interview as on paper, because there is no gap to fall into. Integrity reads as confidence. It tells an employer you will represent their work honestly too. That signal is worth more than any line you could have inflated.

## You're ready to show this when

- [ ] Your case-study README is done, using [`../templates/case-study-README.md`](../templates/case-study-README.md), with what it does, your role, and your decisions near the top.
- [ ] You have a live link or a two-minute recording (ideally both).
- [ ] You have three resume bullets in the verb-plus-action-plus-result shape.
- [ ] You have two STAR stories prepared and rehearsed out loud.
- [ ] You can explain, off the top of your head, one real decision you made and one thing you would do differently next time.

## Related

- Template: [`../templates/case-study-README.md`](../templates/case-study-README.md) — turn your repo's README into a case study.
- Guide: [Step 8: Share it and go live](../guides/step-8-share-and-go-live.md) — get the live link that anchors your demo.
- Example: [The whole RecipeRoll journey](../examples/EXAMPLE-walkthrough.md) — the real artifacts your stories come from.
- Home: [The playbook README](../README.md) — the full map of every step.
