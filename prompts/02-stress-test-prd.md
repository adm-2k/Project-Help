# 🔎 Prompt 02 — Stress-Test the PRD

> Have the AI act as a skeptical senior product manager and poke holes in your plan before you build anything.

**When to use:** After you have a draft PRD, before you break it into tasks. This is Step 2.

## ✅ Before you start

- Have your draft [PRD](../templates/PRD-template.md) ready to paste (the output from [Prompt 01](01-draft-prd.md)).
- Open the [PRD review checklist](../templates/prd-review-checklist.md) so you can check the AI's findings against it.
- Be ready to make changes — the point is to improve the plan, not defend it.

> 💡 **Why bother?** Catching a problem in the plan takes a minute. Catching it after you've built the wrong thing takes days. See the [glossary](../GLOSSARY.md) if any term is new.

## 💬 The prompt

Copy this, replace the `[BRACKETED PART]`, and paste it into your AI builder.

```
You are a skeptical, experienced senior product manager doing a tough but fair
review of this PRD. Your job is to find problems BEFORE we build.

Here is the PRD:
[PASTE YOUR DRAFT PRD HERE]

Please review it and point out:
1. Vague terms — words that could mean different things to different people.
2. Hidden assumptions — things we're taking for granted that might not be true.
3. Missing edge cases — situations the plan doesn't account for.
4. Scope that's too big for v1 — anything that should move to "Later".
5. Unanswered questions — decisions we haven't actually made yet.

For each problem, give a concrete suggested fix in one sentence.

Then finish with: "Top 3 risks" — the three things most likely to cause us
trouble, in priority order.

Be direct and specific. Don't be polite at the expense of being useful.
```

## 💡 Tips

- Don't fix everything blindly. For each suggestion, decide as a team: change the plan, or note it as a deliberate choice.
- Deliberate choices belong in your [decisions log](../templates/DECISIONS.md) so no one re-litigates them later.
- If the AI is too gentle, reply: "Be harsher. Assume this plan has serious flaws and find them."

## 🎯 What good output looks like

- Names specific words and lines, not generic advice.
- Each problem comes with a one-sentence fix you could actually do.
- A clear "Top 3 risks" list you can act on first.

> ⚠️ **Watch out:** The AI doesn't get the final say. Some "problems" may be fine for v1 on purpose. Your team decides what to act on.

## ➡️ Next

Use this in [Step 2: Review the PRD](../guides/step-2-review-the-prd.md), then move on to [Step 3: Break into tasks](../guides/step-3-break-into-tasks.md).
