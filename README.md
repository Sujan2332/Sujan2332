<div align="center">

<br/>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=28&duration=3000&pause=1500&color=A78BFA&center=true&vCenter=true&width=680&height=50&lines=Sai+Sujan+S;Full-Stack+Engineer+%E2%80%94+React+%C2%B7+Node+%C2%B7+AWS;Bengaluru%2C+India" alt="typing animation" />

<p><sub>Production commerce systems, real-time infrastructure, and interfaces built to be measured, not just shipped.</sub></p>

<br/>

<a href="https://sai-sujan-s-portfolio.onrender.com/"><img src="https://img.shields.io/badge/PORTFOLIO-sai--sujan--s--portfolio.onrender.com-A78BFA?style=for-the-badge&logoColor=white" alt="Portfolio"/></a>
<a href="https://github.com/Sujan2332"><img src="https://img.shields.io/badge/GITHUB-Sujan2332-000000?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"/></a>
<a href="https://www.linkedin.com/in/sai-sujan-s/"><img src="https://img.shields.io/badge/LINKEDIN-sai--sujan--s-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>

</div>

<br/>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%" height="2px"/>

## Profile

My work sits at the point where frontend engineering meets production accountability — interfaces built by someone who also owns what happens when checkout breaks at scale. React and Astro depending on whether the win is interactivity or shipped-KB; Node and Express underneath when the frontend needs a backend that isn't someone else's black box; MongoDB when the data model is document-shaped and shouldn't pretend otherwise.

The throughline across client work and personal projects: systems that have to be *correct under load*, not just correct in a demo. A checkout module doesn't get to fail quietly. A file-upload pipeline doesn't get to lose a user's photo because two requests raced. A chat app doesn't get to drop a message because the socket reconnected mid-send. That's the standard I build to whether the audience is a paying client or nobody but future-me.

<br/>

## Engineering Philosophy

<table>
<tr><td width="50%" valign="top">

**Own the failure path, not just the happy path.**
An upload pipeline is judged by what happens on a duplicate key, a dropped connection, or a malformed file — not by the demo where everything works.

</td><td width="50%" valign="top">

**The invisible work is the deliverable.**
Accessibility, SEO metadata, reduced-motion states, and load-time budgets ship with the feature, not after it.

</td></tr>
<tr><td width="50%" valign="top">

**State that's user-aware beats state that's generic.**
File paths, cache keys, and access rules are derived from *who's asking*, not bolted on as an afterthought — cheaper to reason about, harder to get wrong.

</td><td width="50%" valign="top">

**A rebuild beats a patch when the foundation is the bug.**
A migration that keeps a bad architecture just relocates the debt. Sometimes the ground-up rebuild is the faster path to done.

</td></tr>
</table>

<br/>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%" height="2px"/>

## Production & Commerce Engineering

Client-side production work, described at the level that's shareable outside an NDA:

- **Checkout & account ownership at scale** — full module ownership on a large-scale retail platform: 800+ user stories delivered, 300+ defects resolved, across the account and checkout surfaces users actually complete purchases on.
- **B2B SaaS marketing platform** — a 60+ page Astro build engineered around Core Web Vitals and technical SEO from the metadata layer up, not retrofitted after launch.
- **Ground-up platform rebuild** — Astro/GCP, chosen deliberately over a migration once the existing foundation stopped being worth carrying forward.

Recognized with a team Spot Award — first recipient across seniority levels on the team — and moved into a billing-critical role on the strength of that checkout work before the project was shelved following a company acquisition, not due to the engineering.

<br/>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%" height="2px"/>

## Project Spotlight

<table>
<tr>
<td width="50%" valign="top">

### <a href="https://github.com/Sujan2332/Something">Something</a>
A full-stack social platform — profiles, media posts, likes, comments — with file storage engineered directly on AWS S3 rather than local disk.

`React` `Node.js` `Express` `MongoDB` `AWS S3` `JWT`

**Why it's interesting:** the S3 key strategy is context-aware, not a flat upload bucket. Signup-time uploads land in a temp path before the user record exists; post-auth profile photos resolve to a deterministic per-username key that overwrites in place. That distinction — generated key vs. looked-up key — is decided per-request based on auth state, using `multer-s3` streamed directly to an `S3Client`, with per-user identity resolved from Mongo before the object key is even generated.

</td>
<td width="50%" valign="top">

### <a href="https://github.com/Sujan2332/ChatSphere">Chat-Sphere</a>
Real-time chat application rebuilt from a single Replit monorepo into a properly separated client/server architecture.

`React` `Express` `MongoDB` `Socket.IO`

**Why it's interesting:** the hard part wasn't the socket logic — it was the deployment topology. Splitting a pnpm monorepo into independently deployable services surfaced TypeScript and ESM interop issues that only exist once client and server stop sharing a process boundary.

</td>
</tr>
<tr>
<td width="50%" valign="top">

### <a href="https://github.com/Sujan2332/BMS-Alerter">BMS-Alerter</a>
A Telegram bot that watches BookMyShow for a specific film, theatre, and time window, and alerts the moment tickets go live.

`Node.js` `Puppeteer` `Telegram Bot API`

**Why it's interesting:** the actual engineering problem wasn't parsing showtimes — it was staying invisible to Cloudflare's bot detection. Solved with stealth-mode headless Chrome, session capture and replay, and a fallback in-page fetch path, running continuously on a free-tier host.

</td>
<td width="50%" valign="top">

### <a href="https://github.com/Sujan2332/Portfolio">Portfolio</a>
Personal site taken through a full audit pass — fabricated content stripped, vague skill percentages replaced with honest categorical tiers, a real contact form wired in.

`React` `TypeScript` `Vite` `Tailwind`

**Why it's interesting:** shipped with a skip link, reduced-motion support, JSON-LD, and a sitemap — the parts of a portfolio site that never show up in a screenshot but are the actual difference between "built" and "finished."

</td>
</tr>
</table>

<br/>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%" height="2px"/>

## Cloud & Infrastructure

AWS isn't a badge on this profile — it's the storage layer in production code. **Something**'s upload pipeline runs through the AWS SDK v3 `S3Client` and `multer-s3`, with IAM-scoped credentials resolved from environment config and object keys generated per-request rather than per-upload — the kind of detail that only matters once real users are overwriting each other's files.

<div align="center">
<img src="https://skillicons.dev/icons?i=aws,nodejs,express,mongodb,jest&theme=dark" />
</div>

<br/>

## Development Workflow

<table>
<tr><td width="50%" valign="top">

**Build & Test**
Vite for the frontend build loop; Jest for unit coverage where the logic is worth protecting from regressions, not everywhere by default.

</td><td width="50%" valign="top">

**Ship & Track**
Git and GitHub for version control and review; Jira for planning and defect tracking on client engagements; Postman for API contract verification before a frontend ever touches an endpoint.

</td></tr>
</table>

<div align="center">
<img src="https://skillicons.dev/icons?i=vite,git,github,jira,postman,npm&theme=dark" />
</div>

<br/>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%" height="2px"/>

## Stack

<table>
<tr>
<td valign="top" width="25%">

**Frontend**

<img src="https://skillicons.dev/icons?i=react,astro,ts,js,html,css&theme=dark" />

</td>
<td valign="top" width="25%">

**Backend**

<img src="https://skillicons.dev/icons?i=nodejs,express,mongodb&theme=dark" />

</td>
<td valign="top" width="25%">

**Cloud & Testing**

<img src="https://skillicons.dev/icons?i=aws,jest&theme=dark" />

</td>
<td valign="top" width="25%">

**Deployment**

<img src="https://skillicons.dev/icons?i=vercel,render,netlify&theme=dark" />

</td>
</tr>
</table>

<br/>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%" height="2px"/>

## Now Building

Currently working on **Vastra Atelier** — an e-commerce UI for a luxury saree brand spanning a full product-listing → product-detail → account journey, across a three-way light/dark/ivory theme system. The interesting constraint isn't any single page — it's keeping one component tree honest across three visual identities without duplicating logic per theme.

```
[ shipped ]    checkout & account ownership on a large-scale retail platform
[ shipped ]    S3-backed media pipeline with context-aware key generation
[ shipped ]    real-time chat infra rebuilt into a separated client/server architecture
[ building ]   multi-theme design system architecture (Vastra Atelier)
[ exploring ]  server components & partial hydration in Astro/Next
[ exploring ]  queue-backed automation beyond single-process bots
```

<br/>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%" height="2px"/>

## Analytics

<div align="center">

<img src="https://github-readme-stats.vercel.app/api?username=Sujan2332&show_icons=true&count_private=true&hide_border=true&theme=dark&bg_color=00000000&title_color=A78BFA&icon_color=A78BFA&text_color=C9C9C9" height="165"/>
<img src="https://github-readme-streak-stats.herokuapp.com/?user=Sujan2332&hide_border=true&background=00000000&ring=A78BFA&fire=A78BFA&currStreakLabel=A78BFA" height="165"/>

<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Sujan2332&layout=compact&hide_border=true&theme=dark&bg_color=00000000&title_color=A78BFA&text_color=C9C9C9&langs_count=8" width="48%"/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=Sujan2332&theme=react-dark&hide_border=true&bg_color=00000000&color=A78BFA&line=A78BFA&point=ffffff" width="100%"/>

</div>

<details>
<summary><b>Contribution snake</b> — animated commit history</summary>
<br/>

<img src="https://raw.githubusercontent.com/Sujan2332/Sujan2332/output/github-contribution-grid-snake.svg" width="100%"/>

</details>

<br/>

<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png" width="100%" height="2px"/>

## Let's Build Something

Open to Frontend and Full-Stack roles on product-focused teams — especially where the interface is core product surface, not a layer bolted onto someone else's backend.

<div align="center">

<a href="https://sai-sujan-s-portfolio.onrender.com/"><img src="https://img.shields.io/badge/Portfolio-000000?style=for-the-badge&logo=vercel&logoColor=A78BFA" /></a>
<a href="https://github.com/Sujan2332"><img src="https://img.shields.io/badge/GitHub-000000?style=for-the-badge&logo=github&logoColor=white" /></a>
<a href="https://www.linkedin.com/in/sai-sujan-s/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>

<br/><br/>

<sub>Profile views: <img src="https://komarev.com/ghpvc/?username=Sujan2332&style=flat-square&color=A78BFA&label=" height="14"/></sub>

</div>
