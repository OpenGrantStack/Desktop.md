# Desktop.md
- Next.js project  
- Components, lib, pages, styles, types  
- Connects Open Collective → GitHub Organization → Your domain  
- Intended to run at opengrantstack.publicvm.com

Here is a polished, production‑ready README you can drop directly into the repo that will host your ZIP.

---

🌐 OpenGrantStack Dashboard
A unified dashboard connecting Open Collective, GitHub, and your public domain.

This repository contains the full Next.js dashboard used to power the OpenGrantStack ecosystem. It integrates contribution data, funding activity, and repository events into a single, real‑time interface.

The project is packaged as package.zip for easy distribution and deployment.

---

📦 What’s Inside package.zip

The ZIP contains the complete Next.js application:

Project Structure
`
/components     → Reusable UI components  
/lib            → API clients, helpers, webhook utilities  
/pages          → Next.js routes, including API endpoints  
/styles         → Global and module CSS/Tailwind styles  
/types          → TypeScript interfaces for GitHub, OC, and events  
`

Core Features
- GitHub Organization Integration  
  Pulls repository events, contributions, PRs, issues, and metadata from:  
  https://github.com/OpenGrantStack

- Open Collective Integration  
  Syncs financial activity, contributions, and supporters from:  
  https://opencollective.com/opengrantstack

- Custom Domain Ready  
  Designed to deploy at:  
  https://opengrantstack.publicvm.com

- Webhook Support  
  Includes API routes for:  
  - GitHub Webhooks  
  - Open Collective Webhooks  
  - Custom internal events  

---

🚀 Getting Started

1. Download the Dashboard
Download and extract:

`
package.zip
`

Place the extracted folder into your development environment.

---

🛠️ Installation

Inside the extracted project folder:

`bash
npm install
npm run dev
`

The dashboard will start at:

`
http://localhost:3000
`

---

🔗 Required Environment Variables

Create a .env.local file with:

`
GITHUB_ORG=OpenGrantStack
GITHUBAPPID=yourappid
GITHUBPRIVATEKEY=yourprivatekey
OC_SLUG=opengrantstack
OCAPIKEY=yourockey
NEXTPUBLICSITE_URL=https://opengrantstack.publicvm.com
`

(You can add more based on your webhook secrets.)

---

🌉 Webhook Endpoints

The dashboard exposes:

GitHub Webhook
`
/api/webhooks/github
`

Open Collective Webhook
`
/api/webhooks/opencollective
`

Custom Internal Webhook
`
/api/webhooks/custom
`

Each endpoint validates signatures and stores events for display in the dashboard.

---

🌐 Deployment

This project is designed for:

- Vercel (recommended)  
- Node server  
- Docker  
- PublicVM hosting (your current target)

Once deployed, the dashboard becomes available at:

`
https://opengrantstack.publicvm.com
`

---

📊 Dashboard Features

- Real‑time event feed  
- Funding activity from Open Collective  
- GitHub contribution timeline  
- Repository stats  
- Supporter and contributor lists  
- Webhook logs  
- Organization‑wide insights  

---

🧩 Troubleshooting

If the dashboard doesn’t load:

- Check .env.local for missing keys  
- Ensure GitHub App is installed on your organization  
- Verify Open Collective webhook is pointing to your domain  
- Confirm your hosting provider supports Node/Next.js  

---

🏢 About OpenGrantStack

OpenGrantStack is a transparent, open‑source funding and governance ecosystem.  
This dashboard unifies your financial and technical activity into one place for contributors, reviewers, and operators.

---
