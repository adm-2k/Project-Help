# How AI Building Works (for Non-Coders)

> A plain-English picture of what your AI builder actually does, so its strengths and its slip-ups stop catching you off guard.

You are going to spend a lot of time talking to a tool that writes code for you. It helps to know what kind of tool it is. Not the wiring underneath, just its nature: what it is good at, where it goes wrong, and how to get the best out of it. Once you have that picture, the surprises mostly stop.

## It predicts, it does not know

An *[AI builder](GLOSSARY.md)* (Claude Code, Cursor, and the like) works by predicting the next bit of text. You give it words, and it produces the words and code that most plausibly come next, based on the enormous pile of writing and code it learned from. That is the whole engine: very good pattern-matching, one piece at a time.

This matters because it is not a search engine and not an oracle. It does not look anything up unless you hand it the information, and it does not "check" its answer against the real world. It produces what sounds right.

Picture an extremely well-read improv partner. Ask them anything and they will always say something, fluently and with confidence, building on whatever you just said. They have read more than anyone you know. But they are performing the next line, not consulting a record. Most of the time the line is excellent. Sometimes it is pure invention delivered in the same easy voice. Your job is to know which is which.

> Tip: If you want it to use a specific fact, file, or decision, put that information in front of it. It cannot reach for what you did not give it.

## It can be confidently wrong

When an AI builder states something untrue as if it were fact, that is called a *[hallucination](GLOSSARY.md)*. It can invent a feature, a setting, a menu item, a tool, or a plain fact, and present it with total confidence. This is not lying and it is not a glitch. It is the same engine doing the same thing it always does: producing what sounds right. For this tool, sounding right and being right are two different things, and it cannot tell them apart on its own.

Here is what that looks like on RecipeRoll. You ask it to add a `Save to favorites` button. It replies, cheerfully, "Done, I have added the favorites button to each recipe card." You read that and assume favorites now works. But when you open the app, there is no button anywhere. Or you ask how to deploy and it tells you to run a tool that does not exist, named so convincingly that you go looking for it.

The takeaway is one habit, and it is the most important one in this whole document: judge the AI by what the app actually does when you try it, not by what it says it did. Its words are a claim. The running app is the truth.

So after it tells you it built something, go check. Open the app and use the feature. Walk through [guides/step-4-claim-and-build.md](guides/step-4-claim-and-build.md) to see how a task gets built and verified, and run [checklists/before-you-open-a-pr.md](checklists/before-you-open-a-pr.md) before you call any piece of work done.

## It has a short memory

Your AI builder can only think about so much at once. The amount it can hold in mind at one time is its *[context window](GLOSSARY.md)*. In a short exchange this never comes up. But in a long session, as the conversation grows, the earliest details slide out of view. It starts forgetting decisions you made an hour ago, and it can begin contradicting itself, undoing a choice it agreed to earlier or rebuilding something a different way.

Picture a brilliant collaborator with no long-term memory. Each time you turn to them, they are sharp and capable, but they only know what is on the desk in front of them right now. Clear the desk and that knowledge is gone. They are not being careless. They simply cannot hold yesterday, or even the top of today's conversation, once it scrolls away.

You work with this, not against it:

- **Keep each task small.** A short, focused job fits comfortably in what it can hold.
- **Re-give it the plan and context.** When you start something, paste in the relevant piece of the plan again. Repeating yourself is not wasted effort here; it is how you keep the desk stocked.
- **Start a fresh session when it drifts.** If it begins contradicting itself or losing the thread, that is your signal. Open a new session and bring the plan back with you.

The fix for a short memory is one written-down plan it can re-read. Keep that plan somewhere stable and feed it back in as you go. [guides/prepare-ai-ready-deliverables.md](guides/prepare-ai-ready-deliverables.md) shows how to write context the AI can actually use, and a shared AI context file gives the whole team one place to point it.

## What it is great at, and what it is shaky at

The same nature that makes it fast also makes it unreliable in specific ways. Knowing the split lets you lean on it where it is strong and stay watchful where it is not.

| Great at | Shaky at |
| --- | --- |
| First drafts of almost anything | Knowing your specific project without being told |
| Boilerplate and routine setup | Staying consistent across a long session |
| Explaining code or an error in plain English | Exact facts, names, numbers, and versions |
| Repetitive edits across many files | Anything you did not actually give it |
| Turning a clear description into working code | Judgment calls about security |
| Summarizing something long | Knowing what your users really need |

The pattern across the right-hand column is worth saying out loud: it is shaky wherever the right answer depends on knowing your world or on being exactly correct. So those are the moments to slow down, supply the details, and check the result yourself.

## How to work with it well

Everything above points to the same handful of habits. None of them are technical.

- **Give it context.** It cannot use what you did not hand it. Start tasks with the relevant plan, file, or decision in front of it.
- **Ask for small steps.** One clear task at a time fits its memory and is easy for you to check.
- **Verify by trying it.** Trust the running app, not the AI's description of what it did.
- **Start fresh when it drifts.** Contradictions and lost threads mean the session is full. Open a new one and bring the plan along.
- **Remember you are the decider.** It drafts, explains, and builds. You judge what is right, what is safe, and what your users actually need. That call is always yours.

Work this way and the tool becomes what it should be: a fast, tireless partner that you keep pointed in the right direction.

## Related

- [HOW-GIT-WORKS-FOR-NON-CODERS.md](HOW-GIT-WORKS-FOR-NON-CODERS.md) — the companion picture of how your team builds together safely
- [guides/talking-to-your-ai.md](guides/talking-to-your-ai.md) — how to ask for what you want and get it
- [guides/getting-unstuck.md](guides/getting-unstuck.md) — what to do when the AI or the project is stuck
- [GLOSSARY.md](GLOSSARY.md) — any term on this page, in plain English
