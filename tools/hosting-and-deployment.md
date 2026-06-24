# Hosting and Deployment (Putting It Online for Free)

_Last verified: 2026-06. Tool prices and free tiers change often, so re-check the linked sites and update this page each cohort (about quarterly)._

While you build, your app usually runs *locally*, meaning only you can see it, on your own computer. To let anyone else use it, you *deploy* it (see [deploy / ship](../GLOSSARY.md)): you put it on a hosting platform that gives you a public web address you can share. Several platforms do this for free, and most of them redeploy your site automatically every time you push to GitHub, so the live version stays current with no extra steps.

Here are the common free options, checked in June 2026.

| Platform | Free tier | What it can host | Auto-deploy from GitHub? | Live preview link per pull request? | Commercial use allowed on free? | Free web address |
| --- | --- | --- | --- | --- | --- | --- |
| Vercel | Hobby | Static sites, frontend frameworks, and serverless full-stack | Yes | Yes | No (personal/non-commercial only) | `project.vercel.app` |
| Netlify | Starter | Static, frontend, and serverless functions | Yes | Yes | Yes | `site.netlify.app` |
| Cloudflare Pages | Free (unlimited bandwidth) | Static and full-stack via Functions | Yes | Yes | Yes | `project.pages.dev` |
| GitHub Pages | Free (public repos) | Static only (no server or database) | Yes (`main` only) | No | Yes | `username.github.io` |
| Render | Free | Full-stack apps, backends, and databases | Yes | Yes | Yes | `service.onrender.com` |
| Railway | No real permanent free tier | Full-stack apps and databases | Yes | Yes | Yes | `service.up.railway.app` |

A couple of rows need a footnote:

- **Render** free sites go to sleep after about 15 minutes of no traffic, so the first visitor after a quiet spell waits 10 to 30 seconds for the site to wake up. A free database on Render also expires after 30 days, so it suits trying things out, not a long-lived launch.
- **Railway** does not have a true permanent free tier in 2026. You get a one-time `$5` trial credit, then a small monthly credit, and free usage is blocked during peak daytime hours. Treat it as a paid option you can sample, not a free home for your project.

> Watch out: Vercel's free Hobby plan is for non-commercial, personal projects only. No payments, ads, affiliate links, or paid client work are allowed on it. If your tool will ever make money, use Netlify or Cloudflare Pages, which allow commercial use on their free tier.

## Our pick

For most teams, **Netlify** or **Cloudflare Pages** is the easiest call. Both are free, both are safe for commercial use, and both give every pull request its own live preview link.

Use **Vercel** if your project is non-commercial and built with Next.js, where Vercel shines. Use **GitHub Pages** only for a plain static site with no server or database behind it.

> Tip: That live preview link per pull request is a gift for a team. Each teammate's change gets its own web address to click and test, the real thing in a browser, before it merges into the shared app. It turns "does this work?" into something anyone can check, not just the person who built it. See [Step 5: Open a pull request](../guides/step-5-open-a-pull-request.md) and [Step 8: Share and go live](../guides/step-8-share-and-go-live.md).
