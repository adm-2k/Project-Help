# Guide Me: Let an AI Walk You Through This Playbook

This playbook has grown to around forty documents. That is a lot to face when you are new, and you do not have to read all of it. This one page exists so you can hand the whole playbook to an AI chatbot and let it tell you what to do next.

The trick is that everything the AI needs is written right here on this page. It does not have to open the other files or browse the internet. You paste this page into the chat, ask the AI to guide you, and it points you to the exact next step, the exact file to open, and the exact prompt or template to use. You stay in the driver's seat; the AI just reads the map for you.

## How to use this page

There are two ways to do this, depending on the AI you are using.

**If your AI can browse the web** (some versions of ChatGPT, Claude, and similar tools can): give it this page's raw link and say "Read this and guide me." The raw link is:

`https://raw.githubusercontent.com/adm-2k/Project-Help/main/GUIDE-ME.md`

**If your AI cannot browse the web** (most chat windows cannot, and that is fine): select everything on this page, copy it, and paste it into the chat. Then paste the prompt below right after it. The AI now has the entire playbook in front of it and can guide you from that alone.

Not sure which kind you have? Assume it cannot browse. Copy-and-paste always works.

## The prompt to paste

Copy this whole block and paste it into the chat:

```
You are my patient guide to the Upskilling Labs Team Builder Playbook
(the document I just gave you). Ask me one or two questions about where
my team is in the process. Then, based only on the playbook, tell me the
single next step to take, which file to open, and which template or prompt
to use. Explain any unfamiliar word in plain English. Keep it short and
encouraging, and do not assume I know how to code.
```

That is all. The AI takes it from there.

## The playbook in one screen

Here is the whole process, in order, so the AI has the full picture from this page alone. The team builds in one loop: a few steps happen once at the start, and the last few repeat for every new feature.

- **Step 0 - Getting comfortable** (orientation; you belong here, no experience required): `guides/step-0-getting-comfortable.md`
- **Step 1 - Write the PRD** (agree as a team what you are building; the PRD is the plan everyone follows): `guides/step-1-write-the-prd.md` ; template `templates/PRD-template.md` ; prompt `prompts/01-draft-prd.md`
- **Step 2 - Review the PRD** (poke holes in the plan before you build, so problems are cheap to fix): `guides/step-2-review-the-prd.md` ; checklist `templates/prd-review-checklist.md` ; prompt `prompts/02-stress-test-prd.md`
- **Prepare AI-ready deliverables** (turn the plan into one shared brief every AI tool follows, so your teammates' tools all build the same thing): `guides/prepare-ai-ready-deliverables.md` ; templates `templates/AI-CONTEXT.md` and `templates/feature-spec.md` ; prompt `prompts/11-build-ai-context-from-prd.md`
- **Step 3 - Break into tasks** (split the work so one task equals one branch and nobody collides): `guides/step-3-break-into-tasks.md` ; template `templates/task-board.md` ; prompt `prompts/03-decompose-into-tasks.md`
- **Step 4 - Claim and build on a branch** (pick a task, make your own safe copy, build it with your AI): `guides/step-4-claim-and-build.md` ; prompts `prompts/04-build-a-task-on-a-branch.md` and `prompts/05-keep-me-in-sync.md`
- **Step 5 - Open a pull request** (offer your finished piece to the team for review): `guides/step-5-open-a-pull-request.md` ; prompt `prompts/07-write-my-pr.md`
- **Step 6 - Review and merge** (check a teammate's work and fold it in, keeping the shared version healthy): `guides/step-6-review-and-merge.md` ; prompts `prompts/08-review-a-teammates-pr.md` and `prompts/06-resolve-a-merge-conflict.md`
- **Step 7 - Update roadmap and log issues**, then loop back to Step 3 for the next feature: `guides/step-7-update-roadmap-and-log-issues.md` ; templates `templates/ROADMAP.md`, `templates/ISSUE-LOG.md`, and `templates/DECISIONS.md` ; prompts `prompts/09-log-an-issue.md` and `prompts/10-update-the-roadmap.md`
- **Step 8 (optional) - Share it and go live** (put your app online for real people to use): `guides/step-8-share-and-go-live.md` ; reference `tools/hosting-and-deployment.md`

Support you can reach for at any time, no matter which step you are on:

- `GLOSSARY.md` - plain-English meaning of every technical word
- `HOW-GIT-WORKS-FOR-NON-CODERS.md` - the branch-and-merge idea explained with pictures, no commands
- `guides/getting-unstuck.md` - what to do when something breaks or you feel lost
- `tools/README.md` - help choosing which tools to use
- `examples/EXAMPLE-walkthrough.md` - one team going from idea to merged feature, start to finish
- `checklists/` - quick "before you do X" lists, including team kickoff
- `for-facilitators/facilitation-guide.md` - notes for the mentor or facilitator running a team

## If you are at X, do Y

Find the row that sounds like you. Open the file in the last column.

| If this sounds like you | Do this next | Open |
|---|---|---|
| We haven't agreed what we're building | Write the plan together | `guides/step-1-write-the-prd.md`, `templates/PRD-template.md`, `prompts/01-draft-prd.md` |
| We have a rough plan | Poke holes in it before building | `guides/step-2-review-the-prd.md`, `templates/prd-review-checklist.md`, `prompts/02-stress-test-prd.md` |
| Our plan looks done | Turn it into one shared brief for the AI tools | `guides/prepare-ai-ready-deliverables.md`, `templates/AI-CONTEXT.md`, `prompts/11-build-ai-context-from-prd.md` |
| We're not sure our AI tools are building the same thing | Give every tool the same context file | `guides/prepare-ai-ready-deliverables.md`, `templates/AI-CONTEXT.md`, `templates/feature-spec.md` |
| We're ready to split the work | Break the plan into one-branch tasks | `guides/step-3-break-into-tasks.md`, `templates/task-board.md`, `prompts/03-decompose-into-tasks.md` |
| I have a task to build | Claim it and build on your own branch | `guides/step-4-claim-and-build.md`, `prompts/04-build-a-task-on-a-branch.md`, `prompts/05-keep-me-in-sync.md` |
| My piece works | Open a pull request to offer it to the team | `guides/step-5-open-a-pull-request.md`, `prompts/07-write-my-pr.md` |
| I was asked to review a teammate's work | Review it and help merge it cleanly | `guides/step-6-review-and-merge.md`, `prompts/08-review-a-teammates-pr.md`, `prompts/06-resolve-a-merge-conflict.md` |
| I just finished something | Update the roadmap, log any issues, then pick the next task | `guides/step-7-update-roadmap-and-log-issues.md`, `templates/ROADMAP.md`, `templates/ISSUE-LOG.md`, `prompts/10-update-the-roadmap.md` |
| We want to put it online | Share it and go live | `guides/step-8-share-and-go-live.md`, `tools/hosting-and-deployment.md` |
| We're picking which tools to use | Read the tool guide and choose | `tools/README.md` |
| I'm stuck, or a word makes no sense | Get unstuck, or look the word up | `guides/getting-unstuck.md`, `GLOSSARY.md` |

## The full file map

Every folder in this repo, and what it holds. Because this page sits at the repo root, the links below are relative.

- [`guides/`](guides/) - the step-by-step guides, the heart of the playbook. Follow them in order: [step 0](guides/step-0-getting-comfortable.md), [step 1](guides/step-1-write-the-prd.md), [step 2](guides/step-2-review-the-prd.md), [prepare deliverables](guides/prepare-ai-ready-deliverables.md), [step 3](guides/step-3-break-into-tasks.md), [step 4](guides/step-4-claim-and-build.md), [step 5](guides/step-5-open-a-pull-request.md), [step 6](guides/step-6-review-and-merge.md), [step 7](guides/step-7-update-roadmap-and-log-issues.md), [step 8](guides/step-8-share-and-go-live.md), and [getting unstuck](guides/getting-unstuck.md).
- [`templates/`](templates/) - fill-in-the-blank documents you copy and complete as you go: [PRD](templates/PRD-template.md), [PRD review checklist](templates/prd-review-checklist.md), [AI context](templates/AI-CONTEXT.md), [feature spec](templates/feature-spec.md), [task board](templates/task-board.md), [roadmap](templates/ROADMAP.md), [issue log](templates/ISSUE-LOG.md), and [decisions log](templates/DECISIONS.md).
- [`prompts/`](prompts/) - copy-paste prompts for talking to your AI at each step, numbered [01](prompts/01-draft-prd.md) through [11](prompts/11-build-ai-context-from-prd.md).
- [`checklists/`](checklists/) - quick "before you do X" lists: [team kickoff](checklists/team-kickoff.md), [before you start a task](checklists/before-you-start-a-task.md), [before you open a PR](checklists/before-you-open-a-pr.md), and [before you merge](checklists/before-you-merge.md).
- [`tools/`](tools/) - help choosing your tools: [start here](tools/README.md), [AI builders](tools/ai-builders.md), [version control clients](tools/version-control-clients.md), [coordination and PM](tools/coordination-and-pm.md), [data and backends](tools/data-and-backends.md), and [hosting and deployment](tools/hosting-and-deployment.md).
- [`examples/`](examples/) - a complete worked example, one team going from idea to merged feature: [the walkthrough](examples/EXAMPLE-walkthrough.md). Read it once, early.
- [`for-facilitators/`](for-facilitators/) - notes for the mentor running a team: [the facilitation guide](for-facilitators/facilitation-guide.md).
- Support files at the root: [`GLOSSARY.md`](GLOSSARY.md) for word meanings, and [`HOW-GIT-WORKS-FOR-NON-CODERS.md`](HOW-GIT-WORKS-FOR-NON-CODERS.md) for the branch-and-merge idea without any commands.
