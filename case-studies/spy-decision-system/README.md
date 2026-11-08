# From an algorithmic trading app to AI-assisted research

**Product + Engineer · Fintech · Agent architecture · Evals · Human control**

## Why this matters: protecting capital and reclaiming time

> **“Plan your trade and trade your plan.”**

The principle is simple. Following it consistently—while markets move, emotions rise and everyday responsibilities compete for attention—is harder.

**The financial stakes are substantial.** SEBI found that **93% of individual equity futures and options traders in India incurred losses during FY2022–FY2024**, with aggregate losses exceeding **₹1.8 trillion over three years**. This illustrates the scale of retail-trading losses in that market; it is not a measure of U.S. SPY outcomes or proof that psychology caused those losses. [SEBI study](https://www.sebi.gov.in/media-and-notifications/press-releases/sep-2024/updated-sebi-study-reveals-93-of-individual-traders-incurred-losses-in-equity-fando-between-fy22-and-fy24-aggregate-losses-exceed-1-8-lakh-crores-over-three-years_86906.html)

The personal cost also includes time: hours watching charts, monitoring positions and reviewing decisions. **Time is a resource we cannot replenish.**

My mission is to explore how technology can help people **protect their capital, follow a disciplined process and reclaim time**, while pursuing greater financial independence. I started with my own trading workflow—a problem I cared about enough to build, test and challenge.

## Opportunity discovery and user research

I conducted **user interviews and reviewed discussions and concerns on Reddit, X and other trading communities**, alongside examining my own trading experience.

The need I identified was **maintaining trading discipline without depending on continuous screen monitoring**. This shaped an opportunity to combine approved-rule execution with evidence-based research and clear human control.

My product question became:

> **Can I build a system that follows an approved trading plan while I am away, helps me learn from outcomes, and earns permission to take greater responsibility through measurable evidence?**

Supplemental income is part of the motivation. The product must first demonstrate that its decisions, execution and risk controls deserve trust.

## Why trading, why SPY, and why this project?

I chose SPY for its **high trading volume and access to low-cost options contracts**. My existing algorithmic trading application provided market inputs, signal generation, execution rules and recorded outcomes.

That foundation made this a concrete setting to explore **agent autonomy, measurable outcomes and human control**. I could investigate actual decisions, compare proposed changes with existing strategies and observe where automation needed boundaries.

The progression is **historical evaluation → paper validation → controlled live trading**. Paper trading is a validation stage on the path toward live use. Consistent income, improved profitability and reduced supervision remain outcomes to demonstrate.

## How discovery shaped my product decisions

| Problem or insight | Product decision |
|---|---|
| Continuous monitoring consumes attention | Automate approved rules and surface exceptions requiring review |
| Consistency alone cannot make a weak strategy effective | Evaluate strategy performance independently, including costs and downside |
| Historical patterns can support misleading conclusions | Let AI investigate alternatives; keep calculations reproducible |
| Proposed improvements need a fair comparison | Freeze strategy versions and compare them against existing baselines |
| More powerful models may cost more without improving outcomes | Compare proposal quality, trading results, tokens, latency and cost |
| Delegating execution should preserve accountability | Keep permissions explicit and require human approval for live release |

## My ownership

I owned **problem discovery, scope, architecture, evaluation requirements and acceptance decisions**, and drove AI-assisted implementation—starting in **Bolt** and continuing in **Replit**.

My role as **Product + Engineer** is to connect the mission to evidence: decide what is worth automating, build the experience, measure whether it helps, and keep unsupported conclusions from becoming trading actions.

## 1. Existing: my algorithmic trading application

A **Python/Flask server**, browser dashboard, PostgreSQL database and background workers already supported the trading journey:

**Market data → my algorithm → candidate signals → approved-strategy and risk checks → Alpaca orders → position monitoring and recorded outcomes.**

Alpaca and Finnhub supply market inputs; Alpaca handles paper orders. The server applies approved rules to current conditions—it does not invent a strategy each cycle. Signals and orders are linked by identifiers.

Configured behavior includes **45-second market/signal polling** and **15-second paper-position monitoring**, subject to market hours and operational controls. Price structure, volatility and options context inform the application. A comprehensive news/sentiment input to SPY execution is not established.

## 2. Added: bounded AI research

The research agent examines frozen evidence and experiment memory, selects approved analysis tools, and requests bounded historical replays. Results inform its next tool choice. The **evaluation harness** calculates metrics, checks evidence and records traces; the agent cannot place orders or activate strategies.

```mermaid
flowchart TB
  DATA[Alpaca + Finnhub: market data]
  subgraph APP[EXISTING — Python / Flask application on Replit]
    ALGO[Your algorithm: interpret conditions and generate signals]
    GATE[Approved strategy + entry and risk checks]
    EXEC[Alpaca: paper orders and position monitoring]
    DB[(PostgreSQL: signals, context, orders and outcomes)]
    ALGO --> GATE --> EXEC
    ALGO --> DB
    EXEC --> DB
  end
  DATA --> ALGO
  subgraph AI[ADDED — research and review]
    AGENT[AI research agent: choose next analysis]
    HARNESS[Evaluation harness: analysis + bounded modeled backtest]
    FIXED[Separate fixed research workflow]
    REVIEW[Browser dashboard: findings for my review]
    AGENT -->|Request a test| HARNESS
    HARNESS -->|Results inform next step| AGENT
    AGENT -->|Conclude or abstain| REVIEW
    FIXED --> REVIEW
  end
  DB -->|Frozen evidence and memory| AGENT
  DB --> FIXED
  REVIEW -->|Save experiment history| DB
  style APP fill:#f3f4f6,stroke:#6b7280
  style AI fill:#f3e8ff,stroke:#9333ea
  style HARNESS fill:#dbeafe,stroke:#2563eb,stroke-width:3px
```

The blue box is the **harness**; the two arrows between it and the agent form the **research loop**. Calls, runtime, tokens and estimated cost are bounded; the last available model call is reserved for a conclusion or abstention.

A separate **fixed LangGraph workflow** is configured for after-market research. The model-directed agent is requested explicitly today. Its custom loop uses OpenAI function calling; it is not the scheduled LangGraph path.

**Featured Run #47:** on 36 recorded paper trades, the agent selected a direction comparison that reversed the initial aggregate ranking and exposed missing comparison data. The workflow requested better evidence and prevented activation. [Read the table walkthrough](agent-walkthrough.md). Run #46 remains supporting historical-integration evidence.

## My product and architectural decisions

| Decision | Judgment |
|---|---|
| **Reuse the working app and backtester** | Build on existing infrastructure and integrate research into the user journey. |
| **Separate research from execution** | Give the model investigative flexibility without trading authority. |
| **Keep calculations deterministic** | Make findings reproducible and checkable rather than relying on model-generated numbers. |
| **Retain evidence and rejected questions** | Learn across experiments through database memory, not automatic retraining. |
| **Graduate autonomy by risk** | Today research is advisory. Planned isolated paper experiments can run within my policies; live releases require my explicit approval. |

## Verified results

**60 focused checks passed in Replit**, with real model execution recorded separately. Protected trading state remained unchanged. Earlier failures led to explanation-scope validation and a reserved final conclusion call.

> **Current boundary:** the backtest tool supports one frozen session with synthetic option pricing and explicit, uncalibrated costs. It is not a validated one- or two-year options replay. No calibrated confidence score, profitability improvement, agent superiority or time saving is established. One previously identified workflow-test failure remains disclosed. Core trading logic stays private.

[See the evaluation sheet](evaluation.md) for test scope, failures, datasets and remaining evidence gaps.

## Product evaluation: do better models produce better strategies?

I am extending the evaluation design beyond tool correctness: **can a model propose a strategy change that improves independent outcomes over the existing rules, within approved risk limits?**

The benchmark covers signal quality, execute/skip decisions, option selection, after-cost strategy performance, confidence calibration, tokens, latency and cost. Every result must identify its strategy version, model/configuration, dataset and run date. Private strategies use stable public aliases.

**Implemented:** bounded research, deterministic analysis, recorded traces and control checks. Run #47 used OpenAI **gpt-4.1-mini-2025-04-14** on **November 7, 2026**, with 5,442 tokens, approximately $0.0023 in estimated token cost and 5.21 seconds host execution. It investigated recorded paper outcomes; it did not validate a new strategy.

**Implemented locally and verified:** a versioned registry, bounded proposal validation, deterministic metric library, final-data access controls, comparison reports and offline DeepEval custom-metric integration. The framework passed 65 tests and 616 independent verification assertions.

**Still blocked or planned:** actual current-strategy financial baselines require version-linked data and validated production replay. The execution evaluator currently supports synthetic fixtures only; no new model-generated strategy was evaluated. Replit deployment, provider-generation adapters and Claude/other model comparisons remain planned. Future-model rows are explicitly **not run**.

[See the strategy-and-model benchmark table](strategy-model-benchmarks.md). A newer model earns adoption through measured product improvement, not its release date or reasoning label.

## Planned next: graduated autonomy through the AI SDLC

**Automate isolated paper experiments within policies I approve; require my explicit approval for live promotion.** This maps versioned hypotheses to offline evals, isolated staging, human release review and monitored operation.

Today the app supports one active paper strategy and a pending-version approval path. Automatic experimental admission, multiple isolated candidates, recurring model-directed research and the complete live-release loop remain **planned**. Experimental candidates must not change the active bot or access live credentials.

[Read the roadmap and AI SDLC diagram](roadmap.md), including implementation order and acceptance evidence.

## Explore the evidence

- [Strategy-and-model benchmarks](strategy-model-benchmarks.md): product metrics, model/date records, baseline gaps and future comparisons.
- [Supporting evaluations](evaluation.md): correctness, research behavior, data quality and safety.
- [Real Run #47 walkthrough](agent-walkthrough.md): the question, agent-selected follow-up, evidence and bounded decision.
- [Technical architecture](architecture.md): existing app, agent harness, scheduled workflow and planned boundaries.
- [Planned next and AI SDLC](roadmap.md): policy-controlled experimentation and human-approved live release.
- [Illustrative promotion criteria](promotion-policy.md): fictional examples of risk and evidence gates, not deployed settings.

## License

Copyright © 2026 Poornima. Original case-study text and diagrams: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Private trading strategy, code and data are excluded. Future published code will carry a separate MIT license. See [license scope](../../LICENSE).
