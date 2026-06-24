# Facilitation Guide (for Mentors)

## Who this is for

This is the one page written for you, the mentor or facilitator running a cohort. Everything else in this playbook is written for the participants on the teams. So when you read the guides, the checklists, and the templates, read them as your people will read them: as a learner being walked through a step. This page sits beside all of that and tells you how to run the room, so that nervous, non-technical participants feel engaged and seen from day one.

## The teaching method: show, then share the wheel

The most reliable way to teach something that looks scary is gradual release. You do it first, then you do it together, then they do it alone. Three beats, every time:

1. **I do.** You demo the step live, narrating your thinking. Mistakes and all.
2. **We do.** The group tries it together, with you steering but their hands on the wheel.
3. **You do.** Each team runs the step on their own while you circulate.

Two concrete examples tied to the playbook:

- **Writing the PRD.** Open prompt `01-draft-prd.md` on a shared screen and write a PRD live for a throwaway idea, talking through every choice. Then, as a group, draft one together for a second toy idea, with participants calling out what goes in each section. Only then send teams to [Step 1: Write the PRD](../guides/step-1-write-the-prd.md) for their own project. By the time they start, they have watched it happen and done it once with help.
- **Opening a pull request.** Demo one PR end to end yourself, including the part where you click the live preview link. Then have the whole group watch one volunteer open theirs while you coach. After that, teams open their own following [Step 5: Open a pull request](../guides/step-5-open-a-pull-request.md).

> Tip: Narrate the boring parts out loud. When you pause to re-read a prompt or undo a wrong click, you show that hesitation is normal, not a sign you don't belong.

## Make it safe to not know

People who are new to this arrive certain that everyone else already gets it. Your main job is to prove that wrong, fast.

- **Stand up a dedicated questions channel.** Name it something inviting, like a `#stuck` channel, and say plainly that posting there is the job, not a failure at the job. A question asked early saves an afternoon lost later.
- **State the norm out loud.** "There is no such thing as a dumb question here" only works if you say it on day one and then mean it every time someone tests it. The first nervous question sets the tone for the whole cohort. Answer it warmly.
- **Model it yourself.** Share something you had to look up this week, including the search you typed and the answer you found. When the person leading the room admits to not knowing things, everyone else exhales.

Point people who freeze to [Getting unstuck](../guides/getting-unstuck.md). Make sure they know that going there is the expected move, not a detour.

## Pair people up (the buddy system)

Nobody should face a blank screen alone in week one. Pair participants and have them work in the driver/navigator pattern borrowed from programmers:

- **Driver** has hands on the keyboard and types or prompts.
- **Navigator** reads ahead, watches for mistakes, and keeps an eye on the plan.

They swap often, every fifteen or twenty minutes, so both get a turn at each role. Pair a nervous participant with a steadier one rather than two nervous people together, and rotate pairs across the cohort so confidence spreads instead of pooling. The quiet person who would never raise a hand in front of the room will happily ask their buddy.

## Give everyone a role

A coding project can make non-coders feel like spectators. Roles fix that by handing each person a real piece of the work that is theirs to own and that others can see. Suggested roles for a team:

| Role | Owns |
|---|---|
| Product lead | The PRD, scope decisions, and "are we building the right thing" |
| Tester / QA | Clicking through each pull request preview and reporting what breaks |
| Designer | Layout, wording, and how the thing looks and feels |
| Scribe | Notes, and recording decisions in the team's decision log |
| Release captain | Shepherding merges and getting the app live |

Rotate roles across the cohort so everyone tries a few weeks in different seats. The point is not coverage; it is being seen. A person who owns testing, and whose name is on the bug that got caught before launch, knows they mattered to the build. That ownership is what turns a nervous attendee into a contributor.

## The first win (week one)

End the first session with everyone having shipped something real. Run a 30-minute exercise: every team puts a one-page "hello from [team name]" site online using a free host from the [tools list](../tools/README.md).

It does not need to be pretty. A heading, a sentence, and the team's name is enough. What matters is that a real, public URL exists that they made and can text to a friend.

Why bother before any real building starts? Because the scariest word for a new participant is "deploy," and an early, low-stakes win quietly retires that fear. Once a team has put something live and watched it work, "we can't do this" stops being the background hum. They have already done the hardest-sounding part once.

## Demo days

Hold short, low-stakes show-and-tell sessions where each team shares the live preview link from one of their pull requests and everyone in the cohort clicks it and reacts.

Keep them brief, a few minutes per team, and keep the bar low: a half-finished feature shown live beats a polished slide. This is the single best tool you have for making people feel seen. There is a particular lift a participant gets from watching twenty people open the thing they built and say "oh, nice." It also quietly reinforces the pull-request workflow, because the preview link they are showing off is the same link a reviewer uses to check work before it merges. Showing off and good practice turn out to be the same habit.

## A suggested rhythm

A simple week-by-week shape. Treat it as a starting point and stretch or compress it to fit your cohort.

| Week | Focus |
|---|---|
| 1 | Orientation and the first win: tools, roles, and a one-page site live for every team |
| 2 | Write the PRD, then review it as a team |
| 3 | Prepare the shared AI deliverables and split the work into tasks |
| 4 | Build and review cycles |
| 5 | Build and review cycles (repeat as needed) |
| 6 | A demo day |
| 7 | Final showcase |

Build/review weeks are the loop, so repeat weeks 4 and 5 as many times as your timeline allows. A short cohort might fold the PRD and task-splitting into one week; a longer one might run four or five build weeks with a demo day in the middle.

## Retros that surface feelings, not just tasks

A retrospective that only lists what got done misses the point for a group this new. What you most need to hear is how people are feeling, because that is where you will catch someone slipping into "I'm the one who doesn't get it" before they go quiet for good. Ask:

- What felt good this week?
- What felt confusing or where did you get stuck?
- What would help you next week?

Let the room sit with each question rather than rushing to the next. Then record the decisions and improvements that come out of it, so the next week actually changes and people see that speaking up moved something.

## Point people to the right place

Keep these pointers handy so you can route people in the moment:

- **Someone is overwhelmed.** Send them to [GUIDE-ME](../GUIDE-ME.md) for a calm, single next step.
- **A brand-new participant.** Start them at [Step 0: Getting comfortable](../guides/step-0-getting-comfortable.md), then the [Team Kickoff Checklist](../checklists/team-kickoff.md).
- **A team setting up its shared plan.** Walk them through [Prepare your AI-ready deliverables](../guides/prepare-ai-ready-deliverables.md) so the whole team and the AI start from the same picture.
