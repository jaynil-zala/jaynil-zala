# Hi, I'm Jaynil 👋

### Full-Stack Engineer · AI-Native Product Builder
**Next.js · NestJS · PostgreSQL · LLMs · Meta Graph API · AWS**

I build production software end to end: SaaS platforms, admin panels, marketing sites and the CMS and docs behind them. I take each one from database schema to CI/CD and deployment, and I put AI to work both inside the products and in how I ship them.

For nearly 2 years at **Gothi Tech LLP** I've shipped across these product lines:
- **[Voixt.ai](https://voixt.ai)**, a WhatsApp marketing and commerce SaaS, where I'm the top frontend contributor (1,000+ commits)
<!-- - A family of **device-financing (EMI) platforms** -->
- **Troka**, a workforce-management platform, and **Dr. Protect**, a parental-control app
- **Websites, CMS and docs** for the company, its products and local businesses

> 💡 My day-to-day commits live in private company repos under [`@jaynil-gothitech`](https://github.com/jaynil-gothitech), so this profile's contribution graph shows only part of my work.

---

### 🚀 Voixt.ai: WhatsApp Business marketing & commerce platform

**Meta Suite: WhatsApp, Instagram, Messenger and ads in one tool**
- Business-scoped Facebook and Instagram connect, with token refresh and per-company permission modules
- Real-time **Instagram inbox**, comments, publishing, insights and automations, plus a **Messenger inbox** with saved replies and automation rules
- **Lead Ads → CRM**: Meta lead forms flow into kanban lead boards, and stage changes go back to Meta through the **Conversions API (CAPI)**
- Ads Manager features: campaign creation, placements, audiences, lead forms, and direct-to-S3 video upload

**AI Studio: generative AI inside the product**
- AI-written e-shop product descriptions and AI-generated store categories during onboarding
- **AI image studio**: brand-matched product shots, poster-style template headers and upload enhancement, built through iterated prompt design and stored per company on S3
- **Flow and template assistants** that draft WhatsApp automation flows and message templates
- The money side of AI: a prepaid USD wallet, a rate card, GST/IGST tax rules, FX history, invoices, credit notes and monthly statements

**E-Shop: commerce on WhatsApp and the web**
- A six-stage guided store setup with progress tracking, AI help at each step, and **Razorpay** payment onboarding with a guided webhook setup
- Storefront and website builder with theme previews and go-live checks
- Store analytics: live visitors, intent funnels, hourly revenue rollups, drag-and-drop dashboard layouts, and privacy-safe IP geolocation (the IP itself is never stored)

**Platform, content & growth**
- A developer API with scoped keys, plus WhatsApp OTP send/verify, and lead CRM boards with stage handoff and scoped analytics
- **[voixt.ai](https://voixt.ai)** marketing site (Next.js 15, Tailwind 4): Strapi-powered blog, Meta Pixel with consent, Microsoft Clarity, UTM and visitor tracking, and Meta-compliant privacy, terms and data-deletion pages
- **[docs.voixt.ai](https://docs.voixt.ai)** (Docusaurus): product docs, API reference and product updates
- **Voixt CMS** (Strapi 5): blog content types, AWS S3 uploads and seed scripts
- Internal **Docs Publisher** and **Docs Asset Manager**: local web UIs to edit, preview and publish docs pages and to manage doc images on S3

---

### ⚙️ DevOps, Cloud & Meta Platform Configuration

**CI/CD with GitHub Actions**
- Production deploy pipelines for the Voixt backend, e-shop websites and storefront:
  - build on GitHub Actions, deploy over SSH, and load runtime settings from **AWS Secrets Manager**
  - keep the previous build for rollback
  - reload under **pm2** only after a real health check passes, not merely when the process shows as "online"
- CI that runs Jest in memory-capped workers, boots the compiled build under pm2 and confirms it is up, on pinned runner images
- Staging deploy workflows and scripts for the dashboard, plus branch-sync workflows across five repos

**AWS & servers**
- **S3**:
  - per-company and per-account storage layouts
  - direct-to-S3 and resumable video uploads, with signed read URLs
  - static build uploads for the docs and marketing sites
- pm2 ecosystem configs, Cloudflare geo headers and robots rules, and a scheduled DB-IP GeoIP update for an offline location fallback

**Meta app & platform setup** (Voixt is a Meta Tech Provider)
- **WhatsApp Embedded Signup**, including the v5 rollout behind a per-company switch
- Facebook Login for Business scopes, with each feature's permissions in its own module
- **Webhook subscriptions** for Pages (leadgen, feed), Messenger and Instagram Login, through a durable intake, plus a runner that re-subscribes Pages in one pass
- Graph API version upgrades (up to v26.0), a separate ads-access token, and CAPI events that follow Meta's CRM guide (hashed email and phone)
- **Meta compliance**:
  - a compliance switch covering login scope, `leads_retrieval`, the Shops-ads opt-out and EU political ads
  - a data-deletion status page
  - privacy and terms updates for app review

<!--
### 📱 EMI Management level device-financing platforms

Admin panels for **EMI** products. They lock and manage smartphones sold on EMI, used by a network of distributors, stockists and retailers across India.

**Products:** LegBye · Suvidha4u · Fontech · Infinity · Phonex · Dr. EMI

- Multi-level role system (super admin → distributor → stockist → retailer → salesperson) with permission and accessibility modules
- Device enrollment through **QR and IMEI activation codes**, online and offline keys (v1/v2/v3 settlement logic), key transfer, and offline app download flows
- Customer and device management: global search, persistent filters, exports, a distributor dashboard, and city/state masters
- Payment success and failure flows, **Call2Pay**, **EMI Assist**, policy and wallpaper controls
- Security: log out from all devices on password change, and session-scoped customer data
- **Stack:** React, Vite, MUI, Redux Toolkit, with Next.js for Dr. EMI
-->

---

### 🧩 More products I've built

**Troka: workforce & field-attendance management** · *NestJS + React, built full-stack*
- Multi-company HR platform: companies, clients and sites, employees, teams, designations, roles and admins
- **Location-based attendance**: device registration, location activity tracking on Google Maps and Leaflet, shifts and employee shift assignment
- **Leave management**: leave types and balances, applications and approvals, compensatory leave, a holiday calendar with conflict checks
- **Expenses and conveyance** requests, tasks, a dashboard timeline and reports
- Backend: NestJS, TypeORM, MySQL, JWT/Passport auth, OTP verification, API tokens, Swagger docs, Nodemailer

**Dr. Protect: parental control & family device safety** · *React frontend*
- Parent dashboard to manage family members and child profiles, registered devices, **app usage** insights and app configuration
- JWT auth, admin console, charts (MUI X, ApexCharts) and i18n

---

### 🌐 Websites & CMS

| Site | What I built |
| :--- | :--- |
| **Gothi Tech** | Company website (Next.js, Chakra UI): careers, team, certifications, sitemap, robots.txt, Search Console |
| **DBOMS** | Product website (Next.js 15, Tailwind 4): aviation and compliance pages, booking, HubSpot, Clarity, analytics, plus a **Strapi blog CMS** |
| **Voixt** | Marketing site, docs site and CMS (see above) |
| **Local businesses** | Amrutvana UV Studio, Ekta Mobile, Rex Lights: fast static sites with local SEO, JSON-LD structured data and sitemaps |

<!-- | **EMI brands** | LegBye, Finlock, TechMitsu, PSI Computers, Tsukimitsu | -->

---

### 🤖 AI developer tooling I've built

I treat AI agents as a team, so I built the tools to run that team:

- **Claude Hub**: a self-hosted control center for running many Claude Code sessions in parallel. Each session gets its own model, effort and permission settings. Tool approvals happen in the page, and a live dashboard tracks token and cost analytics across every session. A code knowledge graph is built before each task, and a 3D "office" view shows every agent at work.
- **Flow Control Center**: a multi-agent pipeline (research → instructor → dev → test, checked by a judge agent). It turns a ticket into a plan, waits for my approval, builds on a git branch, and scores each step.
- **Remote GPU agent bridge**: runs coding agents on a remote workstation over Tailscale SSH. A live monitoring dashboard covers system load, pm2 apps and live agent transcripts, and a worktree/port registry stops parallel agents from colliding.
- **Meta-ERP spec**: a complete phase-by-phase spec (P00–P12) for a multi-tenant ERP that customers customize at runtime, written to be built by a coding AI.

---

### 📦 Open Source & Research
- **[env-check-lite](https://www.npmjs.com/package/env-check-lite)** (npm): checks environment variables before `npm run dev` or `build`. It finds the variables your project needs from `.env.example` and by scanning source code, suggests example values, checks Node.js compatibility and fails fast in CI.
- **Research:** co-author of [*Emotion-Based Music Player*](https://www.jetir.org/view?paper=JETIR2404743), published in **JETIR (2024)** ([paper](https://www.jetir.org/papers/JETIR2404743.pdf))

---

### 📊 Tech Stack

| Category | Tools & Technologies |
| :--- | :--- |
| **Languages** | TypeScript, JavaScript (ES6+), SQL, Bash, Python, HTML/CSS |
| **Frontend** | Next.js 15, React 19, Vite, MUI, Tailwind CSS, Chakra UI, Redux Toolkit, Zustand, Framer Motion, React Flow |
| **Backend** | NestJS 11, Node.js, PostgreSQL, MySQL, TypeORM, BullMQ, Redis, Socket.IO, Microservices, JWT/Passport, Swagger |
| **CMS & Docs** | Strapi 5, Docusaurus |
| **AI** | OpenAI API, Claude Code, multi-agent workflows, MCP, prompt engineering |
| **Meta Platform** | WhatsApp Business Platform, Embedded Signup, Graph API, Instagram & Messenger APIs, Marketing API, Conversions API, webhooks, app review & compliance |
| **Integrations** | Razorpay, AWS S3, HubSpot, Google Maps |
| **Cloud & DevOps** | GitHub Actions, AWS (EC2, S3, Secrets Manager), pm2, Cloudflare, Docker, Nginx, Netlify, Tailscale, shell scripting |
| **Growth & SEO** | Technical SEO, JSON-LD, sitemaps, Search Console, Meta Pixel, Microsoft Clarity, consent management |
| **Testing** | Jest, Playwright |
| **Workflow** | Git, Jira, ClickUp, Postman |

---

### 📬 Let's Connect
- **LinkedIn:** [jaynil-zala](https://www.linkedin.com/in/jaynil-zala/)
- **Live product:** [voixt.ai](https://voixt.ai) · [docs.voixt.ai](https://docs.voixt.ai)

*"I build products, not just features. I use code, and AI, to solve business problems."*
