# SpecAI — PM Agent

> An AI-powered product management tool that kills bad features before they ship.

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/YOUR_USERNAME/specai-pm-agent&env=ANTHROPIC_API_KEY&envDescription=Your%20Anthropic%20API%20key%20from%20console.anthropic.com&envLink=https://console.anthropic.com)

---

## What it does

SpecAI is a 5-phase AI agent that forces product managers to defend every feature proposal before it reaches engineering. Built with Next.js and powered by Claude, it eliminates gut-feel roadmap decisions by enforcing evidence, customer voice, and structured reasoning at every step.

**The problem it solves:** Most features fail not in engineering — they fail in the room where the decision was made. Weak customer evidence, no baselines, no engineering signal, no post-launch accountability. SpecAI gates all of it.

---

## 5-Phase Flow

| Phase | What happens |
|---|---|
| **Phase 1 — Defensibility** | 6 Socratic questions scored 0–100. Hard gate at 75. Evidence attached per answer. Specific remediation steps for weak areas. |
| **Phase 1b — Customer Voice** | Minimum 3 direct customer quotes required. Before/after narrative. Stakeholder alignment checkboxes. |
| **Phase 1c — Prioritization** | Force rank against active roadmap. Opportunity cost named. Engineering complexity estimated. Pre-mortem completed. |
| **Phase 2 — Research** | Upload any format — Gong transcripts, Zendesk exports, competitor URLs, interview notes. 20MB limit. |
| **Phase 3 — Spec Output** | Full spec with RICE + ICE + MoSCoW scores, Go/No-Go recommendation with top reasons, customer narrative, competitive position, risks, rollback plan. PM approves or rejects. |
| **Phase 4 — Feedback Loop** | Post-launch KPI tracker. Variance analysis. Learning log feeds back into future Phase 1 sessions automatically. |

---

## CPO-Level Features

- **Scored defensibility gate** — 75+ required to proceed (configurable per session)
- **Evidence per question** — screenshots, PDFs, exports attached directly to each answer
- **Customer voice required** — 3 minimum direct quotes before spec is generated
- **Pre-mortem built in** — Amazon's highest-signal practice. Assume failure, write the headline
- **Force ranking** — this feature vs your active roadmap, explicit opportunity cost
- **Engineering signal** — T-shirt size, risk level, dependency mapping before commitment
- **Review date commitment** — PM is on record with a post-launch return date
- **Learning loop** — Phase 4 variance analysis feeds into future Phase 1 sessions
- **Notion export** — spec structured to map directly to Notion blocks
- **Vercel-ready** — API key secured server-side, never exposed to browser

---

## Tech Stack

- **Frontend:** Next.js 14 + vanilla CSS
- **AI:** Claude Sonnet (Anthropic API) via server-side API route
- **Hosting:** Vercel (free tier)
- **Cost:** ~$0.10–$0.40 per feature spec in API usage

---

## Deploy to Vercel (no coding required)

### Step 1 — Get your API key
1. Go to [console.anthropic.com](https://console.anthropic.com)
2. Create an account and generate an API key
3. Copy the key (starts with `sk-ant-...`)

### Step 2 — Upload to GitHub
1. Go to [github.com](https://github.com) → sign in or create free account
2. Click **New repository**
3. Name it `specai-pm-agent`, set to Public, click **Create repository**
4. Click **uploading an existing file** and upload all files from this folder

### Step 3 — Deploy to Vercel
1. Go to [vercel.com](https://vercel.com) → sign in with GitHub
2. Click **Add New Project** → select `specai-pm-agent`
3. Click **Deploy** — Vercel auto-detects Next.js
4. Go to **Settings → Environment Variables**
5. Add: `ANTHROPIC_API_KEY` = your key from Step 1
6. Go to **Deployments** → Redeploy

**Your live URL is now active.**

---

## Local Development

```bash
# Install dependencies
npm install

# Set up environment
cp .env.example .env.local
# Add your API key to .env.local

# Run locally
npm run dev
# Open http://localhost:3000
```

---

## Security

- API key lives only in Vercel environment variables
- All Claude calls route through `/api/claude` server-side
- Users never see or have access to your key
- Key is not present anywhere in client-side code or page source

---

## Project Structure

```
specai-pm-agent/
├── pages/
│   ├── index.js          # Full 5-phase PM agent UI
│   └── api/
│       └── claude.js     # Secure server-side Claude API route
├── package.json
├── .env.example
├── .gitignore
└── README.md
```

---

## Built by

Conceived and designed as an AI-native product management tool demonstrating how Claude can enforce product quality gates, synthesize multi-source research, and generate production-ready feature specs.

Powered by [Anthropic Claude](https://anthropic.com) · Deployed on [Vercel](https://vercel.com)

