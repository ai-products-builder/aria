# ARIA — AI Resource & Investment Aggregator

> **Score, prioritize, and prove the value of every enterprise AI initiative — with executive-ready reporting built in.**

ARIA is an enterprise AI portfolio management platform that gives AI program leaders a single source of truth for every initiative — from first idea through go-live to realized ROI. It enforces a structured lifecycle, automates scoring and prioritization, and closes the loop between what AI was supposed to deliver and what it actually did.

## Live demo

| Module | Link |
| --- | --- |
| **Portfolio Dashboard** | [aria-dashboard.html](https://ai-products-builder.github.io/aria/aria-dashboard.html) |
| **Use Case Intake** | [index.html](https://ai-products-builder.github.io/aria/index.html) |
| **Repository** | [aria-repository.html](https://ai-products-builder.github.io/aria/aria-repository.html) |

The dashboard includes an **executive briefing** — a one-click summary formatted for leadership and board-level communication — and an **AI chatbot** for querying portfolio data and initiative status in natural language.

---

## Why I built this

Enterprise technology programs have always struggled with the same governance gap: initiatives get submitted informally, prioritization is negotiated rather than scored, and when leadership asks what the investment actually delivered — nobody has a clean answer. AI has made this problem bigger and faster-moving than ever.

ARIA is the governance layer built specifically for that gap. It's designed for the AI program leader who is being asked to run a portfolio like a business but given no infrastructure to do it.

---

## The problem

Enterprise AI programs are scaling fast, but most organizations still can't answer the questions leadership asks most:

- Which AI initiatives are delivering measurable business value?
- Are we investing in the right use cases across the right business lines?
- How do we prioritize when everything feels urgent and resources are finite?
- What is our realized vs. projected ROI across the full AI portfolio?

Without a governance layer, AI runs in silos. Business lines submit use cases informally. Prioritization is not analytical. Costs scatter across budgets. No one can prove whether the investment paid off.

**ARIA is the governance layer enterprise AI programs are missing.**

---

## How ARIA is different

Most organizations try to solve this with Jira boards, spreadsheets, or generic PPM tools like Planview or ServiceNow. These fail because they weren't built for AI:

| Gap | Generic PPM / Spreadsheets | ARIA |
| --- | --- | --- |
| AI-specific scoring | ❌ Manual, inconsistent | ✅ Claude-powered, weighted across 6 dimensions |
| Benefits realization | ❌ Forgotten post-go-live | ✅ Automated 30/60/90-day KPI reviews with escalation |
| Shadow AI detection | ❌ None | ✅ Flags unregistered tools at intake |
| Executive reporting | ❌ Manual exports, slide decks | ✅ Live dashboard + one-click board-ready exports |
| Lifecycle enforcement | ❌ Honor system | ✅ Hard gate criteria; no auto-advancing |

---

## What ARIA does

ARIA lets teams log, score, track, and report on AI initiatives across every business line. It uses Claude AI to automatically evaluate each use case across six dimensions, then surfaces a ranked portfolio view that helps leadership make faster, better-funded decisions.

| Dimension | What it measures |
| --- | --- |
| **Strategic fit** | Alignment to business goals and long-term strategic priorities |
| **Expected impact** | Revenue upside, cost savings, efficiency gain, or risk reduction |
| **Feasibility** | Technical readiness, data availability, and execution complexity |
| **Cost** | Total investment required — build, license, and run-state |
| **Resource availability** | Whether the people and budget needed are available now |
| **Risk** | Regulatory, data, model, and operational risk exposure |

Every initiative gets a composite score. The portfolio view ranks them, surfaces trade-offs, and generates the reports leadership actually needs — without requiring a data analyst to produce them.

---

## Key features

- **Structured intake** — Standardized submission form captures business context, sponsor, KPIs, cost estimates, and risk flags. No freeform submissions, no missing fields.
- **Claude-powered scoring** — Automatic evaluation of strategic fit, feasibility, and ROI using Claude AI. Configurable weights per the AI CoE's priorities.
- **8-stage lifecycle engine** — Enforced gate criteria at every stage transition. Use cases can't auto-advance; an owner must confirm exit criteria are met.
- **Portfolio dashboard** — Ranked view of all active initiatives with adoption metrics, stage status, and realized vs. projected value.
- **Benefits realization tracking** — Automated 30/60/90-day post-Live KPI reviews assigned to named owners. Escalates automatically if missed.
- **Vendor & tool registry** — Tracks every AI tool and vendor in use, linked to dependent initiatives. Detects shadow AI on submission.
- **External benchmarking** — Compares AI investment performance to industry peers to give leadership context for ROI figures.
- **Executive report export** — One-click dashboard, scorecard, and ROI reports formatted for senior leadership and board-level communication.

---

## Built for

- **AI program leaders** managing multi-initiative portfolios across business lines
- **AI Centers of Excellence** responsible for prioritization, governance, and value measurement
- **Strategy and finance teams** needing defensible visibility into AI investment performance
- **CTOs, CDOs, and CIOs** reporting AI value to executive leadership and the board

---

## Platform architecture

ARIA is organized into six layers, each with a distinct responsibility.

[![ARIA Platform Architecture](docs/architecture/aria-architecture.svg)](docs/architecture/aria-architecture.svg)

| Layer | Responsibility |
| --- | --- |
| **1. Intake** | Structured submission · Claude-powered scoring · Approval routing |
| **2. Lifecycle** | 8-stage pipeline · Enforced gate criteria · Staleness alerts |
| **3. Repository** | Use case records · Vendor registry · KPIs · Audit trail |
| **4. Intelligence** | Adoption · Impact · Cost/ROI · Benefits realization · Benchmarking |
| **5. Reporting** | Dashboard · Scorecard · Adoption report · ROI & benchmark report |
| **6. Governance** | Review committees · Approvals · Change control · Escalation |


---

## Core modules

### 1. Intake

Every use case enters ARIA through a standardized intake form. The form captures:

- Problem statement and business line
- Executive sponsor and named owner
- Estimated cost, effort, and timeline
- Expected business impact and success KPIs
- Data requirements and risk flags

Submissions are automatically scored by the prioritization engine across six dimensions: strategic fit, expected impact, cost, feasibility, resource availability, and risk. Each dimension is rated 1–5 with configurable weights. The engine produces a composite score, surfaces trade-offs, and routes the submission to the appropriate reviewers — AI CoE, finance, or risk — via a configurable approval workflow.

---

### 2. Lifecycle stage engine

Every use case progresses through eight defined stages. Transitions require explicit gate actions — no auto-advancing, no skipping. An authorized owner must confirm exit criteria before a stage moves forward.

| Stage | Description | Gate to exit |
| --- | --- | --- |
| **Ideation** | Intake submitted | Sponsor identified, problem statement defined |
| **Assessment** | Feasibility, cost, and risk evaluated | Prioritization score confirmed, go/no-go decision made |
| **Approved** | Budget and resources formally committed | Team assigned, KPIs locked |
| **In development** | Build underway, tracked in PM tool | UAT passed, pilot environment ready |
| **Piloting** | Limited rollout, KPIs actively monitored | KPI threshold met, scale approved by sponsor |
| **Live** | Full production rollout | 90-day benefits review completed |
| **Scaled** | Rolled out across BU or firm-wide | Value sustained, transitioned to routine operations |
| **Retired** | Decommissioned or superseded | Lessons captured, record archived |

**Staleness alerts** trigger automatically when a use case in any active stage (Assessment through Scaled) has not been updated in 60 days. The record owner is notified in their configured collaboration tool. The AI CoE sees a portfolio-level flag on the dashboard.

---

### 3. Repository

The repository is the authoritative record for every use case, active or archived. Each record contains:

- **Core metadata** — name, description, business line, BU, sponsor, owner
- **Stage and status** — current lifecycle stage, last updated timestamp, full gate history
- **KPIs and success metrics** — defined at intake, tracked from piloting through live
- **Financial data** — projected cost, actual spend, projected ROI, realized ROI
- **Documentation links** — linked assets, decision records, architecture docs, meeting notes
- **Taxonomy** — function, technology type, data domain, risk classification
- **Audit trail** — immutable log of every change, decision, and gate action

#### Vendor & tool registry

A linked entity within the repository. Every use case references the AI tools and vendors it depends on. The registry tracks vendor name, contract status and renewal date, license count and cost, risk classification, and the full list of dependent use cases — enabling impact analysis before any contract decision. Any tool submitted that is not already in the registry triggers a shadow AI flag for AI CoE review.

---

### 4. Intelligence layer

Eight modules read continuously from the repository and produce the signals that feed reporting and escalation:

| Module | What it tracks |
| --- | --- |
| **Adoption monitor** | User counts, rollout %, change management milestones by BU |
| **Impact tracker** | Realized business value vs. projections made at intake |
| **Cost & ROI engine** | Actual spend vs. budget, payback period, ROI % over time |
| **Benefits realization** | 30/60/90-day post-Live KPI validation with owner accountability |
| **Strategic alignment** | Use case mapping to firm strategic pillars; flags drift when priorities shift |
| **External benchmarking** | AI investment performance vs. industry peers and sector medians |
| **Risk & compliance** | Model drift, data governance issues, regulatory exposure flags |
| **Resource tracker** | Headcount allocation, budget committed, tooling usage across the full portfolio |

#### Benefits realization process

Going Live is the starting gun, not the finish line. When a use case moves to Live, ARIA automatically creates three scheduled review tasks assigned to the named benefits realization owner:

- **Day 30** — early signal check
- **Day 60** — trend confirmation
- **Day 90** — formal KPI validation against intake projections

If the owner does not complete a task within a 5-business-day grace period, it escalates automatically to the AI CoE and the business sponsor. Actual KPI values are logged against projections and feed directly into the ROI engine and reporting layer. This is the mechanism that closes the loop between what was promised and what was delivered.

---

### 5. Reporting

| Report | Primary audience | Cadence |
| --- | --- | --- |
| **Executive dashboard** | C-suite, AI steering committee | Live / real-time |
| **Portfolio scorecard** | Business line leads, AI CoE | Monthly |
| **Adoption report** | Change management, HR, BU leads | Monthly |
| **ROI & benchmark report** | CFO, finance, board | Quarterly |

All reports render natively in ARIA and are available as a live data feed to connected BI tools. The benchmark report contextualizes internal ROI figures against external peer data — giving leadership the "compared to what?" that raw numbers alone can't provide.

---

### 6. Governance

ARIA enforces process integrity at every layer:

- **AI review committee** — defines and adjusts prioritization weights, approves high-cost or high-risk use cases, conducts quarterly portfolio reviews
- **Approval workflows** — configurable multi-step approvals for stage transitions, budget commitments, and vendor additions
- **Change control** — scope changes to approved use cases require a formal re-assessment gate before proceeding
- **Escalation paths** — automated escalation for stale records, missed benefits reviews, budget overruns, and risk threshold breaches
- **Audit trail** — immutable, timestamped log of every decision, change, approval, and gate action across the platform

---



## Prioritization framework

The scoring engine evaluates every submitted use case across six dimensions. Weights are fully configurable by the AI CoE to reflect the firm's current strategic priorities.

| Dimension | What it measures |
| --- | --- |
| **Strategic fit** | Alignment to the firm's long-term strategic pillars |
| **Expected impact** | Revenue upside, cost savings, efficiency gain, or risk reduction |
| **Feasibility** | Technical complexity, data readiness, and team capability |
| **Cost** | Total investment required — build, license, and run-state |
| **Resource availability** | Whether the people and budget needed are available now |
| **Risk** | Regulatory, data, model, and operational risk exposure |

Each dimension is scored 1–5. The engine produces a weighted composite score, flags significant trade-offs (e.g. high impact paired with high risk and low feasibility), and surfaces these before the submission reaches human reviewers.

---

## Success metrics

ARIA measures its own effectiveness as a platform. Targets are grounded in AI CoE operational benchmarks and enterprise program management standards.

| Metric | Target | Rationale |
| --- | --- | --- |
| % of AI initiatives submitted through formal intake | 100% | Full portfolio visibility is the baseline for any governance |
| Time from submission to prioritization decision | < 10 business days | Matches typical investment committee cadence in enterprise orgs |
| % of use cases with KPIs defined at intake | 100% | No KPIs = no accountability; enforced at form level |
| % of post-Live benefits reviews completed on time | > 90% | Lagging indicator of program discipline and owner accountability |
| Portfolio-level realized vs. projected ROI ratio | Tracked quarterly | Establishes trend data; target tightens as the program matures |
| % of AI tools in registry vs. found in shadow AI audits | Trending to 100% | Shadow AI is the leading governance risk in scaling programs |

---

## Roles & access

| Role | Access |
| --- | --- |
| **Business line submitter** | Submit and view their own use cases |
| **Business line lead** | View all use cases in their BU; approve stage transitions |
| **Benefits realization owner** | Complete assigned post-Live review tasks |
| **AI CoE member** | Full portfolio read access; configure prioritization weights |
| **AI CoE admin** | Full admin — users, workflows, integrations, registry |
| **Finance** | Cost, ROI, and budget views across the full portfolio |
| **Executive / board** | Dashboard and scorecard — read-only |

All roles are provisioned via SSO and synced from the firm's identity provider. Role assignment is managed in the IdP; ARIA does not maintain a separate user directory.

---

## Tech stack

| Layer | Technology |
| --- | --- |
| **Frontend** | React |
| **AI engine** | Claude API (Anthropic) — scoring, evaluation, report generation |
| **Storage** | Persistent key-value store |
| **Reporting** | Markdown · PDF export |

> **Note:** ARIA is designed for enterprise deployment. Production infrastructure choices — database, auth, CI/CD, cloud provider — are configurable based on the organization's environment and security requirements.

---

## Repository structure

```
/
├── docs/
│   └── architecture/        aria-architecture.svg — platform layer diagram
├── aria-dashboard.html      Executive portfolio dashboard
├── aria-intake-form.jsx     Structured use case intake form
├── aria-repository.html     Use case repository and vendor registry
├── index.html               Platform entry point
└── INTAKE-README.md         Intake module documentation
```

---

## Roadmap

### ✅ Built & live

| Module | What's working |
| --- | --- |
| **Intake form** | 7-step structured submission · auto-generated use case ID · 5 ROI calculator types · Claude-powered scoring on submit · edit mode |
| **Use case repository** | Split-panel list + detail view · search and filter · score breakdown · re-score · edit · live Supabase data |
| **Portfolio dashboard** | Metric cards · stage breakdown · investment by business line · recommendation split · ranked initiatives table |
| **Executive briefing** | One-click Claude-generated narrative across all portfolio initiatives · accessible from dashboard |
| **Ask ARIA chatbot** | Natural language portfolio queries · conversation history · quick reply chips · accessible from dashboard |
| **Claude prioritization engine** | Scoring across 6 dimensions · composite score · recommendation · rationale · flags · executive summary |

---

### 🔜 Coming soon

| Module | Description |
| --- | --- |
| **Approval routing** | Route submissions to AI CoE, Finance, and Risk for review |
| **Lifecycle stage transitions** | Enforced gate criteria · no auto-advancing · gate history |
| **Staleness alerts** | Auto-flag initiatives with no updates in 60+ days |
| **Vendor registry UI** | Track every AI tool in use · contract status · shadow AI management |
| **Adoption monitor** | User counts · rollout % · change management milestones by BU |
| **Impact tracker** | Realized vs. projected value post-launch |
| **Benefits realization scheduler** | Automated Day 30/60/90 KPI reviews · owner accountability · escalation |
| **Portfolio scorecard** | Monthly report for business line leads and AI CoE |
| **ROI & benchmark report** | Quarterly report for CFO and board · external peer benchmarking |
| **PDF / Excel export** | Download reports for offline sharing |
| **Governance workflow engine** | Approval workflows · escalation paths · audit trail |

---



```bash
# Clone the repo
git clone https://github.com/ai-products-builder/aria.git
cd aria
```

Open `index.html` in your browser to launch the platform. The intake form (`aria-intake-form.jsx`), dashboard (`aria-dashboard.html`), and repository (`aria-repository.html`) can be run independently or served together.

Full module documentation: [`INTAKE-README.md`](INTAKE-README.md)

---

## About the author

**Preethi Sannathi** — AI & Data Platform Product Leader

Product leader focused on AI and data platforms, working across AI Centers of Excellence, cross-functional product teams, and executive stakeholders to translate AI investment into measurable business value. ARIA is built to solve the portfolio governance gaps that show up consistently in enterprise AI programs at scale.

[linkedin.com/in/preethi-sannathi](https://linkedin.com/in/preethi-sannathi) · [github.com/ai-products-builder](https://github.com/ai-products-builder)

---

*AI scoring engine powered by Claude (Anthropic) · Designed for enterprise AI program leaders*
