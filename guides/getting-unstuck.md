# Getting Unstuck

> Something broke, or a word stopped making sense, and you're not sure what to do. This page is for that exact moment.

## Getting stuck is normal

Everyone gets stuck. Experienced developers get stuck several times a day; they've just learned that being stuck is a normal part of the work, not a verdict on whether they're any good at it. The same is true for you.

Most of what stops you will turn out to be small: a typo, a missing step, a setting in the wrong place. The fix is often a minute or two of work once you know what's wrong. The trick isn't to never get stuck. It's to have a calm, repeatable way to get unstuck. That's what this page gives you.

## Ask your AI to explain the error

When you see an error message, your first move is almost always the same: hand the whole thing to your AI builder and ask it to translate. Don't try to decode the error alone, and don't paste only the last line; copy all of it.

Paste this, with your error in place of the brackets:

```
Here is an error I'm getting:

[paste the entire error message here]

Explain this error in plain English, what likely caused it, and the
safest way to fix it, step by step. I am not a programmer.
```

Read what comes back, try the first suggested step, and report what happened. Nine times out of ten, this is the whole story.

## Try the rubber-duck habit

Programmers have an old trick: explain your problem, out loud, to a rubber duck on the desk. It sounds silly, and it works. The act of putting the problem into plain words, "I expected X, I clicked here, instead Y happened," forces you to slow down and lay out the steps, and you often spot the answer mid-sentence.

You don't need a duck. Explain it out loud to yourself, type it into a notes file, or write it as a message to a teammate. Many a question gets answered before it's ever sent, just by the work of writing it down clearly.

## Check the glossary

Sometimes you're not stuck on a broken thing; you're stuck on a word. A teammate says "rebase your branch" or the screen says "merge conflict," and the sentence might as well be in another language.

Before you spiral, open the [Glossary](../GLOSSARY.md). It defines the words this playbook uses in one or two plain sentences each. A word you understand is far less scary than a word you don't.

## Know the escalation path

When the AI doesn't solve it, you don't keep grinding alone. The team has an order to follow, so help is always one clear step away:

1. **Ask the AI.** Paste the error, ask it to explain and fix. Most things stop here.
2. **Ask your buddy.** A second pair of eyes catches what you've been staring past. Your teammate may have hit the same wall yesterday.
3. **Ask the team channel.** Post the problem and what you've already tried. Someone has likely seen it.
4. **Bring it to office hours.** For anything still stuck, your mentor's office hours are the backstop. That's what they're for; nobody minds.

The rule of thumb: try the step you're on for a little while, and if you're still stuck, move up a level. Don't burn an afternoon fighting alone in step one.

## When to log it instead of fighting it

Not everything needs to be solved the moment you find it. If something is broken but not blocking you, or if it's an idea for later rather than a problem for now, the right move is to write it down and keep going, not to drop everything and chase it.

Log it as an issue. Add a row to the [ISSUE-LOG](../templates/ISSUE-LOG.md), or use the [log an issue](../prompts/09-log-an-issue.md) prompt to turn a rough note into a clear entry. A logged problem is a problem the team can see and pick up; a problem you fought silently and forgot is gone. Logging it is progress, not giving up.

> Watch out: Never paste secrets into a chatbot. Passwords, API keys, private personal data, none of it should go into your AI builder or any chat tool, even when you're asking for help. Strip those out of an error before you paste it. When in doubt, leave it out.

## When the AI goes in circles

Sometimes the AI gets into a loop. You say "that's still broken," it changes something, and the same problem comes back, or a new one appears. You can feel it digging a deeper hole. The moment to notice is when two or three rounds of "fix it" have left you no better off.

When that happens, stop repeating "still broken." It rarely helps, because a long, muddled conversation is exactly when the AI's short memory works against it (see [How AI Building Works for Non-Coders](../HOW-AI-BUILDING-WORKS-FOR-NON-CODERS.md)). Reset instead:

1. **Start a fresh session.** Open a new chat so the AI is not dragging along all the confused back-and-forth.
2. **Re-give it the context.** Point it at your `PRD.md` and the one thing you are trying to do right now.
3. **Ask for one small step.** Narrow the request right down: a single, clearly described change.
4. **Simplify the goal.** If a feature keeps fighting you, ask for a simpler version first, then build it up.

> Tip: A fresh, well-aimed ask beats ten rounds of "no, still wrong." When in doubt, start over clean. See [Talking to your AI](talking-to-your-ai.md) for how to phrase it.

## Your safety net: go back to what worked

Here is the most reassuring fact in the whole playbook: you can almost always return to the last version that worked. Nothing you try is truly risky, because your project keeps save points.

Every time you or your AI builder make a [commit](../GLOSSARY.md), you create a save point you can come back to. If a change made things worse, you do not have to fix it forward. You can restore the last good save point and start again from there. You do not need to memorize commands: in GitHub Desktop you can undo recent changes with a click, or you can simply ask your AI builder, "put this back to the last committed version." For the calm, full picture, see [How Git Works for Non-Coders](../HOW-GIT-WORKS-FOR-NON-CODERS.md).

The habit that makes this work: commit often while things are working, so you always have a recent, safe place to fall back to. Knowing you can undo is what makes experimenting feel safe instead of scary.

## You've got this

Being stuck feels worse than it is. Almost every problem you'll hit has been hit before, has a name, and has a fix, and you have an AI tutor, a buddy, a team, and a mentor all within reach. Work the steps, stay calm, and you'll be moving again sooner than you think.

When you're ready to get back to it, return to the [README](../README.md) to find your place in the loop, or open [GUIDE-ME](../GUIDE-ME.md) and let an AI point you to the next step.
