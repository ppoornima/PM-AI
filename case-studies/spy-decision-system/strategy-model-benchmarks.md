# Strategy-and-model benchmarks

**Local implementation verified November 7, 2026 · Real strategy-performance baselines blocked by data**

## Product question

Which model and reasoning configuration produces strategy proposals that improve independent trading outcomes over my existing strategy, within the same risk and research budget?

I define application-specific benchmarks because general model scores cannot establish this product outcome. Published evaluation practices inform the methodology; baseline results and acceptance gates must be measured and defined for this application. A benchmark dataset, a baseline result and an advancement threshold are separate things.

## Benchmark dimensions

| Dimension | Comparison / metric | Current evidence |
|---|---|---|
| Signal quality | Predefined outcome/horizon; precision, coverage and missed opportunities | No complete versioned predictive benchmark established |
| Execute or skip | After-cost improvement over existing policy on matched opportunities and risk | No validated policy-improvement result |
| Option selection | Eligible point-in-time contracts; spread, liquidity, exposure and outcome against predefined selection baseline | Historical quote-path and execution assumptions remain limiting |
| Full strategy | Net expectancy, drawdown, tail losses, exposure, regime consistency and uncertainty versus baseline | Historical setup exploration exists; current-version benchmark not established |
| Confidence | Calibration of defined trade probabilities; separate uncertainty in strategy-level results | No calibrated strategy-confidence score |
| Model efficiency | Exact model/configuration, tokens, scoped cost and end-to-end latency | Individual OpenAI run measurements available below |
| Trust and safety | Calculation, provenance, permissions and failure handling | Implemented checks; see supporting evaluations |

A losing trade is not automatically an incorrect decision. Policy correctness and outcome performance are measured separately. Skipped trades and alternative contracts require modeled counterfactuals; they are not recorded executions.

## Recorded model runs

Dates below are America/Los_Angeles run dates. The date embedded in a model ID is its version, not the execution date.

| Provider / exact model | Run date | Scope | Tokens | Estimated model-token cost | Duration | Strategy improvement |
|---|---|---|---:|---:|---|---|
| OpenAI / gpt-4.1-mini-2025-04-14 | Nov 7, 2026 | Run #47: recorded-paper investigation | 5,442 | $0.0022692 | 5.193s agent; 5.21s host | Not evaluated; no new strategy tested |
| OpenAI / gpt-4.1-mini-2025-04-14 | Nov 6, 2026 | Run #46: one-session modeled replay | 6,902 | $0.0028892 | 10.924s loop; 11.543s overall | Not evaluable from zero trades |
| Anthropic / Claude version to select | Not run | Future comparison | — | — | — | Not run |
| OpenAI / other version or configuration to select | Not run | Future comparison | — | — | — | Not run |

Reasoning configuration has not been established in this public summary; it must not be inferred as low/high from model names. No input/output/reasoning token split is asserted here. Cost excludes hosting, data and human review. Single-run timings are not latency distributions. Future provider evaluations are deferred until the user chooses to run them.

## Verified strategy inventory and benchmark status

The registry contains 16 entries spanning strategies, components, catalogue descriptions and historical candidates—not 16 independently executing strategies. The active paper composite has an inspection-time source/configuration fingerprint; entries were paused and live execution was not verified.

| Public alias / role | Verified operating status | Current-version financial benchmark | OpenAI candidate comparison | Claude candidate comparison |
|---|---|---|---|---|
| SPY Paper Baseline | Active paper composite; entries paused | **Blocked by data** | Not run | Not run |
| Structural Strategy A | Enabled component of that composite | **Blocked by data** | Not run | Not run |
| Structural Strategy B | Enabled component of that composite | **Blocked by data** | Not run | Not run |
| Structural Strategy C | Enabled component of that composite | **Blocked by data** | Not run | Not run |
| Other screening, historical and catalogue entries | Defined/informational or historical; no verified separate execution | No validated matched baseline | Not run | Not run |
| Newly proposed strategy versions | No new model-generated candidate evaluated in this milestone | Not run | Not run | Not run |

**Why blocked:** 188 orders lack strategy-version tags; one labeled order lacks a contemporaneous exact source/configuration fingerprint. Full version-linked opportunities, eligible intraday option chains, complete costs, marked-to-market equity and exact execution/risk replay parity are not established. Today's fingerprint cannot be applied retroactively.

Run #47's historical setup alias does not establish the performance of the current Strategy A version. Its results remain exploratory. The report preserves 190 archived backtest configurations and 25 archived experiment variants without relabeling them as current baselines.

## Implemented locally

- Immutable registry, versioned rubrics, source/configuration fingerprints, dataset lineage and auditable attempt records.
- Bounded structured hypothesis validation. Currently supported changes are limited entry-admission predicates; exits, option policy and risk inherit the frozen baseline.
- Candidate/batch freezing, overlap/reuse checks for final evaluation data and scoped development-data access.
- Deterministic metric library and synthetic matched-policy evaluator, with explicit missing-data states.
- Local CLI and reproducible HTML/CSV reports, including 64 strategy/configuration cells and historical model telemetry.
- DeepEval 4.3.3 in an isolated environment; six positive/negative custom-metric fixture cases covering end-to-end, trajectory and component contracts. No hosted upload or LLM judge.

**Verification:** 65 framework tests and 616 independent assertions passed on review. Saved DeepEval fixture results record no provider calls. These validate implementation behavior, not profitable trading. Trading state and protected source remained unchanged in the saved before/after evidence.

## Remaining work

No new provider run or model-generation adapter was added. The working financial execution adapter is **synthetic-fixture only**; real-strategy execution adapters remain blocked pending independent parity and data validation. The package is local, not deployed in Replit. Broader proposal types, provider comparisons, recurring operation and automatic promotion remain planned.

## Intended comparison process

Research brief and development evidence → bounded model proposal → frozen strategy version → deterministic independent evaluation versus baseline → isolated paper evidence → human live-release review.

The registry preserves strategy and rubric versions, model/configuration, prompts/tools/harness versions, datasets, market conditions, execution assumptions, budgets, attempted hypotheses, evaluation dates and evidence status. Private rules stay private; public results use stable aliases.

Evaluate the model as a researcher separately from the resulting deterministic strategy. A runtime model choosing individual trades would be a separate architecture and benchmark. No model receives final evaluation feedback while revising a candidate; attempted hypotheses and reused periods must be tracked. Repeated model trials measure consistency, not additional independent market evidence.

Use explicit statuses such as **not run**, **blocked by data**, **not applicable**, **exploratory**, and **validated for a stated scope**. An unavailable metric is never zero. Baselines and advancement criteria are recorded before candidate evaluation; fictional policy examples are not executable settings.

## Role of DeepEval

DeepEval's custom-metric integration is implemented and fixture-tested locally. Its current rubrics check evidence contracts; they do not certify free-text scientific reasoning or financial performance. Deterministic financial metrics remain separate. Provider-backed quality grading and repeated real-model comparisons have not run.

[DeepEval documentation](https://deepeval.com/docs/evaluation-introduction) · [Supporting evaluations](evaluation.md) · [Run #47](agent-walkthrough.md) · [Roadmap](roadmap.md)
