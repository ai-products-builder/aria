# Aria — AI ROI Analyzer
> Score, prioritize, and track enterprise AI initiatives by strategic fit, feasibility, and ROI — with executive-ready reporting built in.

---

## The Problem

Enterprise AI programs are scaling fast — but most organizations don't have a systematic way to answer the questions that matter most to leadership:

- Which AI initiatives are delivering measurable business value?
- Are we investing in the right use cases?
- How do we prioritize across competing AI projects?
- What's the realized vs. projected ROI across our AI portfolio?

Aria solves this. It's the portfolio governance layer that enterprise AI programs are missing.

---

## What Aria Does

Aria is an AI-native portfolio management tool built for enterprise AI program leaders. It lets teams log, evaluate, and track AI initiatives across business lines — and uses Claude AI to automatically score each use case across three dimensions:

| Dimension | What it measures |
|---|---|
| Strategic Fit | Alignment with business goals and long-term priorities |
| Feasibility | Technical readiness, data availability, and execution complexity |
| Estimated ROI | Projected value delivery relative to cost and effort |

Each initiative is ranked in a prioritized portfolio view, and the platform generates executive-ready reports that communicate adoption, impact, and investment allocation to senior leadership.

---

## Key Features

- **AI Use Case Intake** — Structured form to log new AI initiatives with business context, owner, status, and success metrics
- **Claude-Powered Scoring** — Automatic evaluation of each use case on strategic fit, feasibility, and ROI using Claude AI
- **Portfolio Dashboard** — Ranked view of all initiatives with adoption metrics and realized vs. projected value
- **Investment Allocation View** — Visualize where AI spend is going and identify reallocation opportunities
- **Executive Report Export** — One-click summary report formatted for senior leadership and board-level communication
- **Post-Implementation Tracking** — Log realized outcomes against projected ROI over time

---

## Built For

- Enterprise AI program leaders managing multi-initiative portfolios
- Product managers responsible for AI adoption and ROI measurement
- Strategy and finance teams needing visibility into AI investment performance
- CTOs and CDOs reporting AI value to executive leadership

---

## Tech Stack

- **Frontend** — React
- **AI Engine** — Claude API (Anthropic)
- **Storage** — Persistent key-value store
- **Reporting** — Markdown / PDF export

---

## Getting Started

```bash
# Clone the repo
git clone https://github.com/ai-products-builder/aria

# Install dependencies
npm install

# Add your Anthropic API key
echo "ANTHROPIC_API_KEY=your_key_here" > .env

# Run locally
npm start
```

---

## Roadmap

- [ ] Multi-user workspace support for enterprise teams
- [ ] Slack and email alerts for initiative status changes
- [ ] Integration with Jira and Asana for implementation tracking
- [ ] Benchmarking against industry AI adoption data
- [ ] Custom scoring frameworks by industry vertical

---

## Why I Built This

As a data and AI platform product leader, I've seen firsthand how enterprise AI programs struggle with the same measurement gap — lots of initiatives, no clear way to track which ones are working or how to prioritize the next wave. Aria is the tool I wished existed.

---

## Author

**Preethi Sannathi** — AI & Data Platform Product Leader
[linkedin.com/in/preethi-sannathi](https://linkedin.com/in/preethi-sannathi) · [github.com/ai-products-builder](https://github.com/ai-products-builder)

---

*Built with Claude AI · Designed for enterprise AI program leaders*
