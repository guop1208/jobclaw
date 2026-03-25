# ⚡ Jobclaw

> AI-powered recruiting platform where autonomous agents handle screening and matching — so humans only engage when it truly matters.

![Status](https://img.shields.io/badge/status-demo-ff6b35?style=flat-square)
![License](https://img.shields.io/badge/license-MIT-00d4a0?style=flat-square)
![Powered by Claude](https://img.shields.io/badge/powered%20by-Claude%20AI-8b5cf6?style=flat-square)

---

## What is Jobclaw?

Jobclaw eliminates the most painful parts of hiring and job searching by giving every user — recruiter and job seeker alike — their own AI agent named **Claw**.

- **Job seekers** onboard once via a conversational chat, set their criteria, and wait. Claw screens roles in the background and only surfaces real matches with scored, explainable reports.
- **Recruiters** define their role and ideal candidate profile once. Claw screens applicants automatically, negotiates soft criteria agent-to-agent, and delivers a shortlist — not a pile of CVs.
- **Agent-to-agent negotiation** means compensation ranges, location flexibility, and culture fit are pre-resolved before a human ever gets involved.

---

## Features

- 🤖 **Live AI agent chat** — powered by Claude (Anthropic). Claw onboards users, captures criteria, and answers questions in real time
- 📊 **Multi-dimensional match scoring** — skills, compensation, location, and culture fit scored independently with visual breakdown
- 🔁 **Agent-to-agent negotiation** — agents communicate across the platform to resolve deal-breakers before human handoff
- 👥 **Dual-mode UI** — full separate experiences for job seekers and recruiters in one app
- ⚙️ **Configurable automation** — toggle digest frequency, auto-scheduling, passive sourcing, and preference learning
- 📦 **Zero dependencies** — the demo runs as a single `index.html` file, no build step or server required

---

## Demo

The demo is a fully interactive single-file HTML application. It includes:

| View | Description |
|---|---|
| **Matches / Pipeline** | Scored match cards with agent summaries, criteria pills, and action buttons |
| **Agent Chat** | Live conversation with Claw, powered by the Claude API |
| **Agent Settings** | Toggle automation preferences and review active criteria |

### Run locally

```bash
# Option 1 — just open it
open index.html

# Option 2 — serve it locally
npx serve .
# or
python3 -m http.server 8080
```

Then visit `http://localhost:8080`.

---

## Getting Started with the AI Chat

The match dashboards and settings work fully offline. To activate the live Claw agent:

1. Get an API key from [console.anthropic.com](https://console.anthropic.com)
2. Open the app and navigate to **Agent chat**
3. Paste your API key into the field at the top of the chat page
4. Start the conversation — Claw will guide you through onboarding

> **Note:** Your API key is used directly in the browser and is never stored or transmitted anywhere except to the Anthropic API. For a production deployment, proxy requests through a backend server to keep keys secure.

---

## Project Structure

```
jobclaw/
├── index.html        # Complete standalone demo (HTML + CSS + JS)
├── jobclaw.jsx       # React component version (requires Vite or CRA)
└── README.md
```

The `jobclaw.jsx` file is the React source version of the same app, suitable for integrating into a larger React project.

---

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | Vanilla JS / HTML / CSS (demo), React (component) |
| AI Agent | [Claude API](https://docs.anthropic.com) — `claude-sonnet-4-20250514` |
| Fonts | Bebas Neue, DM Sans, DM Mono via Google Fonts |
| Build | None required for demo — single file |

---

## Roadmap

The demo establishes the core UX. A production build would add:

- [ ] User authentication and persistent profiles
- [ ] Real agent-to-agent communication layer (e.g. WebSockets or job queue)
- [ ] LinkedIn profile import via Chrome extension
- [ ] Job board API integrations (Indeed, Otta, Greenhouse)
- [ ] Preference learning from accept/decline history
- [ ] Email/Slack digest notifications
- [ ] Recruiter ATS integrations
- [ ] Mobile-responsive layout
- [ ] Backend API to proxy Claude calls securely

---

## Contributing

Contributions are welcome. To get started:

```bash
git clone https://github.com/your-username/jobclaw.git
cd jobclaw

# For the plain HTML demo — just open index.html in a browser

# For the React version
npm create vite@latest jobclaw-app -- --template react
cd jobclaw-app
# copy jobclaw.jsx into src/App.jsx
npm install
npm run dev
```

Please open an issue before submitting a large pull request.

---

## License

MIT — free to use, modify, and build on.

---

## Acknowledgements

- AI agent powered by [Anthropic Claude](https://anthropic.com)
- Concept inspired by the inefficiency of modern recruiting workflows — too much screening, not enough signal
- Built as a rapid prototype to explore agentic UX patterns in hiring

---

*Jobclaw — let the agents do the work.*
