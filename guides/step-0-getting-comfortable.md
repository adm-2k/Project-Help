# Step 0: Getting Comfortable

> Before Step 1, a moment to settle in. If you're nervous about building software, please take the time to read this first. 

## You belong here

We have specifically developed this build cycle to not require a coding background. While it may be beneficial for your team to have people familiar with code, the larger point of building an application is to get you familiar with design process and to give you a sense of empowerment of what you can build and learn by iterating progressively. The people on your team who have never written a line of code in their lives should get the most out of this build cycle if they are invested in learning quickly and being willing to break things and figure out workarounds. If you can describe what you want in plain words, you can build software here.

So take a breath. You're not behind.

## What you actually do here

Here's the honest shape of the work: you describe what you want, the AI does the coding, and you steer and check.

Your group decides what the app should do, who it's for, and whether what came back is any good in meeting your criteria. The AI writes the actual code. Your job is to give it a clear plan, read what it produces, try it out, and say "yes, that's right" or "no, that's not what I meant." You need to think as yourself as a manager or orchestrator, learning as much as possible about different areas, asking questions, and referring to official documentation when needed.

As the team has reiterated, all of the research and resource gathering that you have done is really important for helping to give the model as much context as possible so it can scope out the features with regard to your desired audience. If you are really leaning into the tool, it should allow you to constantly earn dividends from the previous research you've done while using the tool as an assistant.

## Asking questions is the job

When you don't understand something, ask the model! Especially when it is something related to software design, programming, or technical implementation, the likelihood of hallucination is much lower. These models were trained on extensive amounts of code and technical documentation, so if you are prompting in a professional and well-structured way (e.g., "Acting as a software engineer with decades of experience working with startups to implement the initial infrastructure for applications..."), you should be able to get some useful outputs. Likewise, you can always run a "code-checking" skill that looks at what's been generated and makes sure that it conforms to the feature roadmap that is an extension of your PRD.

Just to reiterate, ever confident-looking person around you was once confused by `branch` and `merge` and `pull request.` Do not let these be an impediment to jumping in and learning. The ones who got comfortable are simply the ones who continued using the tools. If you have any questions, asking out loud saves the whole team the time of tripping over the same thing later. Treat your own confusion as useful information, not embarrassment. When none of you are able to answer a particular question or find the answer online, feel free to reach out to me or one of the mentors.

## The AI is a patient tutor

Your AI builder isn't only there to write code. It's also a rather atient teacher. If you need extra explanations, alternative examples, or reference materials, it will can provide and and all of those. This is great for getting a clearer picture around technical jargon or having it map out the architecture, so you can see how parts relate.

For example:

```
You are an professional software engineering and CS instructor with decades ofexperience helping beginners by bringing abstract concepts into concerete examples. I'm a new student who is stuggling with GitHub. Explain what a "pull request" is like I've never heard the term, using a simple everyday comparison.
```

```
What does this error message mean, in plain English? What probably caused it, and what's the safest thing for me to try first?
```

Ask it to slow down. Ask it to use an analogy. Ask it to assume you know nothing.

## How to find your way around

You don't have to hold this whole playbook in your head. A few places will orient you whenever you're lost:

- The [README](../README.md) is a useful map. It shows the whole loop, tells you where you are, and points you to the right step for whatever your team is doing right now.
- The [Glossary](../GLOSSARY.md) is a plain-English dictionary. Any word that looks like jargon, `commit`, `branch`, `repo`, `deploy`, is defined there in one or two friendly sentences.
- [GUIDE-ME](../GUIDE-ME.md) is a shortcut for when you would rather just ask. Paste it into ChatGPT or Claude, and the AI reads the playbook and tells you what to do next, in plain English.

## Your first win

Early on, your team should try to put a tiny page online, something small and real, so you can feel what shipping actually feels like before the stakes get higher. It it is a valuable first step to see something you helped make appear at a real web address, one you can open on your phone, show friends, etc. It is the moment "building software" stops being scary and starts being fun.

There are a variety of tools that you can use, but you can actually prompt your AI Builder to create a static HTML page using Jekyll for GitHub Pages, which is one of the simplest and most basic pages you can create. 

## Next

When you're ready, start with [Step 1: Write the PRD](step-1-write-the-prd.md). You should be working on a collaborative Google Doc that you are shaping out your user research, building out user journeys, and ensuring you have a shared vision of the product and its features. If your team is setting up for the first time, run the [Team Kickoff Checklist](../checklists/team-kickoff.md) together first; it covers everything to get ready, and a mentor can help you through it.
