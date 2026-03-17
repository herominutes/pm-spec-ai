# SpecAI — PM Agent

> The PM agent that kills bad features before they ship.

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/YOUR_USERNAME/specai-pm-agent&env=ANTHROPIC_API_KEY&envDescription=Your%20Anthropic%20API%20key%20from%20console.anthropic.com&envLink=https://console.anthropic.com)

---

Most features fail not in engineering — they fail in the room where the decision was made. SpecAI is the quality gate between an idea and a roadmap commitment.

---

## Without SpecAI vs With SpecAI

| Without SpecAI | With SpecAI |
|---|---|
| Features approved on gut feel and seniority | Scored defensibility gate — every feature earns its place |
| No baseline metrics — success is undefined at launch | Baselines and KPIs locked in before a line is written |
| Customer evidence is anecdotal, not structured | Direct customer quotes required to proceed |
| Engineering estimates happen after approval | Engineering complexity captured before commitment |
| No post-launch learning loop — same mistakes repeat | Post-launch tracker feeds learnings into future specs |
| Weak features consume 60–70% of build capacity | Only high-conviction features reach engineering |

---

## By the numbers

- **75+** — minimum defensibility score required to proceed
- **5** — structured phases from idea to engineering handoff
- **3** — frameworks scored simultaneously: RICE, ICE, MoSCoW

---

## 5-Phase Flow

| Phase | What happens |
|---|---|
| **Phase 1 — Defensibility** | 6 Socratic questions scored 0–100. Hard gate at 75. Evidence attached per answer. Specific remediation steps for every weak area. |
| **Phase 1b — Customer Voice** | Minimum 3 direct customer quotes required. Before/after narrative. Stakeholder alignment checkboxes. |
| **Phase 1c — Prioritization** | Force rank against active roadmap. Opportunity cost named explicitly. Engineering complexity estimated. Pre-mortem completed. |
| **Phase 2 — Research** | Upload Gong transcripts, Zendesk tickets, competitor URLs, interview notes. 20MB limit. Any format accepted. |
| **Phase 3 — Spec Output** | Full spec with RICE + ICE + MoSCoW scores, Go/No-Go recommendation with top reasons, customer narrative, competitive position, risks, rollback plan. PM approves or rejects. |
| **Phase 4 — Feedback Loop** | Post-launch KPI tracker. Variance analysis. Learning log feeds back into future Phase 1 sessions automatically. |

---

## Key Features

**Evidence-based scoring** — Attach screenshots, PDFs, or transcripts to each answer. Evidence quality raises your score directly.

**Actionable next steps** — Every weak score comes with specific remediation steps — not vague feedback. Named tools, data sources, and people to contact.

**Pre-mortem built in** — Forces PMs to articulate how this fails before committing. Amazon's highest-signal product practice.

**Customer voice required** — Minimum 3 direct customer quotes must be logged before a spec can be approved. No anecdotes.

**Roadmap prioritization** — Features ranked against existing roadmap. Opportunity cost made explicit before approval.

**Learning loop** — Post-launch variance feeds back into Phase 1 automatically. The system gets smarter with every feature shipped.

---

## Built for teams that want every feature to earn its place

Powered entirely by Claude API. Runs in any browser. Deploys to Vercel in under 30 minutes.

- **Zero infra cost** — Vercel free tier is sufficient for 1–10 PMs
- **~$0.10–$0.40 per spec** — Claude API usage only
- **Vercel-ready** — API key secured server-side, never exposed to browser

---

## How to use

### Option A — GitHub Pages (each user brings their own key)
The app shows an API key input at the top of the page. Each user:
1. Gets a free key at [console.anthropic.com](https://console.anthropic.com)
2. Pastes it into the field — stays in their browser only, never stored
3. Uses the full app immediately with no setup

### Option B — Vercel (team shares one key — recommended)
Deploy to Vercel and add your API key as an environment variable. No setup needed for team members.

**Step 1** — Get your API key at [console.anthropic.com](https://console.anthropic.com)

**Step 2** — Upload to GitHub
1. github.com → New repository → `specai-pm-agent` → Public → Create
2. Click **uploading an existing file** → drag all files from this folder → Commit

**Step 3** — Deploy to Vercel
1. vercel.com → Add New Project → select `specai-pm-agent` → Deploy
2. Settings → Environment Variables → add `ANTHROPIC_API_KEY` = your key
3. Deployments → Redeploy

Your live URL: `https://specai-pm-agent.vercel.app`

---

## Tech stack

- **Frontend:** Vanilla HTML/CSS/JS — no frameworks, no build step needed
- **AI:** Claude Sonnet (Anthropic API)
- **Hosting:** Vercel (free tier) or GitHub Pages
- **Cost:** ~$0.10–$0.40 per complete feature spec

---

## Project structure

```
specai-pm-agent/
├── index.html        ← Full app with value prop landing + 5-phase agent
├── api/
│   └── claude.js     ← Vercel server route (API key secured server-side)
├── package.json
├── .env.example
├── .gitignore
└── README.md
```
---

## License & intellectual property
### Copyright © 2026. All rights reserved.

This repository and everything in it — the source code, product architecture, audit engine, scoring logic, prompt design, pricing model, and product strategy — is the original intellectual property of the repository owner. It is published here for two explicit purposes: to attract conversation with investors, EdTech operators, curriculum directors, and potential co-founders who see the commercial potential in this space; and to demonstrate a complete senior product thinking methodology, from problem definition through retention design, metric discipline, validation roadmap, and competitive moat analysis.

This is not open-source software. Publication on GitHub does not constitute a transfer of IP rights or an invitation to commercialise. You may view, study, and reference this work for educational and non-commercial purposes with attribution. You may not use the code, architecture, scoring rubric, or product strategy in any commercial product or service without a separate written agreement with the author.

If you are an investor, operator, or potential co-founder interested in building this — reach out directly.


---

Built with [Anthropic Claude](https://anthropic.com) · Deployed on [Vercel](https://vercel.com)
