# Step 8: Share It and Go Live

> When you want real people to use what you built, you put it online and hand them a link. This step is optional, and it's the satisfying one.

**Goal:** put your app on the public web so anyone with the link can use it. · **Time:** about 30 minutes the first time, then automatic. · **Who:** one person sets it up; the whole team benefits.

## Why it matters

While you build, your app runs *locally* ([locally](../GLOSSARY.md)): it lives on your own computer, and only you can see it. You open it at an address like `localhost:3000`, which is your machine talking to itself. That's perfect for building and testing, but you can't send `localhost` to a friend. It only works on the computer it's running on.

To let other people use your app, you *deploy* it ([deploy / ship](../GLOSSARY.md)). Deploying puts your app on a hosting platform that gives you a real web address, like `reciperoll.netlify.app`, that anyone can open from any device. That link is the difference between "I made a thing" and "people are using my thing." This step is the optional last move, for when you're ready for that.

## What to do

You do this once. After it's set up, every push you make updates the live site on its own.

1. **Pick a free host.** Open [`../tools/hosting-and-deployment.md`](../tools/hosting-and-deployment.md) and choose a platform. For most teams, Netlify or Cloudflare Pages is the easy call: free, simple, and fine for projects that might make money. Read the table, pick one, and don't overthink it.

2. **Connect your GitHub repo.** On your chosen host, sign in with GitHub and point it at your team's repository. This is the key move: once the host is connected to your repo, it redeploys your site automatically every time someone pushes to `main` ([main](../GLOSSARY.md)). You don't run a "publish" step ever again; shipping a change just means merging it, the same loop you already know.

3. **Note your free web address.** When the connection finishes, the host hands you a public link, something like `reciperoll.netlify.app`. Write it in your team chat and your README so nobody has to go hunting for it. This is the address you send to the world.

4. **Ask your AI builder to help.** You don't have to figure out the settings alone. Tell your AI builder (Claude Code, Cursor, and the like) which host you chose and ask it to walk you through connecting the repo, choosing the right build settings, and fixing anything that fails on the first try. Paste any error you see straight back to it.

5. **Share the link.** Send it to your testers, your friends, the people you built it for. Watch them use it. This is the moment the project becomes real.

> Going further on GitHub: Once a host is connected to your repo, you get more than one live site. Every pull request gets its own live preview link, a separate web address showing exactly that change, before it merges. Your reviewer clicks the link and tries the real thing in a browser instead of trusting a description. Tie this into your review habit in [Step 5: Open a pull request](step-5-open-a-pull-request.md).

## Example: RecipeRoll

RecipeRoll has worked on `localhost` for two weeks. Maya, Sam, Priya, and Devin can each run it, but nobody outside the team has ever opened it. They decide it's ready for friends to try.

Devin volunteers to set up hosting. He reads [`../tools/hosting-and-deployment.md`](../tools/hosting-and-deployment.md) and picks Netlify, since the team hopes RecipeRoll might one day charge for premium recipe collections, and Netlify allows that on its free tier. He signs into Netlify with GitHub, connects the RecipeRoll repo, and within a few minutes the site is live at `reciperoll.netlify.app`.

He pastes the link into the team chat. Priya opens it on her phone, adds a recipe, and it works, the same app, now on the web. From now on, every time the team merges a feature into `main`, Netlify rebuilds the live site on its own. Nobody runs a publish button again.

Maya sends the link to three friends who like to cook. By that evening, there are recipes in RecipeRoll that none of the team wrote. They shipped.

## Watch out for

- **Vercel's free plan is non-commercial only.** Vercel's free Hobby tier forbids anything that makes money, no payments, ads, affiliate links, or paid client work. If your tool will ever earn a cent, use Netlify or Cloudflare Pages instead, which allow commercial use for free. See the table in [`../tools/hosting-and-deployment.md`](../tools/hosting-and-deployment.md).
- **Deploying makes your code public to the running app.** Once your app is live, anything you put directly in the code, like a password, an API key, or private data, can leak. Never paste secrets into your code. Ask your AI builder how to keep them in environment settings on the host instead, where they stay out of the public site.

## You're done when

- [ ] You picked a free host that fits your project (commercial use, if you'll ever need it).
- [ ] Your GitHub repo is connected, so pushes to `main` redeploy automatically.
- [ ] You have a public web address and shared it with the team.
- [ ] A real person who isn't on the team has opened the link and used your app.

## Next

Go log what comes next. Loop back to [Step 7: Update the roadmap and log issues](step-7-update-roadmap-and-log-issues.md) to capture what your testers found and what you'll build next. And now that you have something real and live, make it work for your career: [Turn your project into a portfolio piece](build-your-portfolio-piece.md).

## Prompts and templates

- Tool guide: [`../tools/hosting-and-deployment.md`](../tools/hosting-and-deployment.md) — the free hosting options compared, with our pick.
- Tool index: [`../tools/README.md`](../tools/README.md) — every tool category in the playbook, in one place.
