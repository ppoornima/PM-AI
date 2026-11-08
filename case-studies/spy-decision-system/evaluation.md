# Supporting research and system evaluations

**Evidence through November 7, 2026 · Framework documented; repeated-trial benchmark planned**

**Primary product evaluation:** [strategy-and-model benchmarks](strategy-model-benchmarks.md) test whether proposed changes improve independent trading outcomes. That framework is implemented and verified locally; actual current-strategy financial baselines remain blocked by missing data and replay parity. No new model comparison has run.

This page records supporting evaluations of whether the agent helps me make a justified research decision while respecting trading boundaries. Agent quality, strategy performance and user usefulness are separate outcomes: a good investigation may conclude that a strategy should not advance.

## Supporting framework

Each dimension uses **Pass / Fail / Insufficient evidence / Not tested**. Safety failures cannot be averaged away by a high overall score. These grading conventions are proposed; the existing checks are not yet a unified automated scorecard.

| Dimension | Question | Evaluation method |
|---|---|---|
| **Evidence** | Is the information suitable for this question? | Check provenance, timestamps, fill linkage, missing data and exclusions. |
| **Analysis** | Are calculations and comparisons valid? | Recompute metrics; check comparable groups and unsupported claims. |
| **Investigation** | Did the next analysis resolve an important uncertainty? | Review the selected tool and the additional evidence it produced. |
| **Decision and safety** | Was the conclusion justified and within permissions? | Check the recommendation, abstention and protected system state. |
| **Usefulness and efficiency** | Did this help me decide what to do next at reasonable cost? | Owner review, corrections, time and comparison with the fixed workflow. |

Code checks calculations and permissions. A human-reviewed rubric for investigation quality and usefulness is planned; model-assisted grading would require calibration against human judgments.

## Implemented versus planned

| Implemented and verified | Planned |
|---|---|
| Deterministic calculations, evidence checks and control tests | A versioned task set with expected outcomes defined before runs |
| Tool traces, recorded results and protected-state comparisons | Repeated trials and consistent rubric scoring |
| Run #46: zero-trade modeled replay and abstention | Matched-task comparison against a capable fixed workflow |
| Run #47: recorded paper outcomes and a useful follow-up | Measured review effort, corrections, reliability and total cost |
| Advisory research with no strategy activation | Policy-controlled isolated paper experiments and human-approved live release |

## Evidence available now

| Example | What was verified | What it does not establish |
|---|---|---|
| **Run #47 — recorded paper outcomes** | 36 trades across 12 sessions; real agent-selected direction comparison; unchanged trading state. 30 focused tests and 191 independent verification assertions passed. | Current-strategy profitability, causality or repeated-run reliability. |
| **Run #46 — historical integration** | Two modeled replays, 390 bars each, zero trades and abstention. 60 focused checks passed at that milestone. | Useful trade-performance analysis or realistic executable-options validation. |

These counts cover different scopes and overlap; they are not additive or model-quality success rates. The 191 assertions verify one frozen Run #47, not 191 experiments. Earlier failures and one known pre-existing workflow-test failure remain in the [detailed evidence record](evaluation-evidence.md).

Run #47 used four model calls and approximately **$0.0023 in estimated model-token cost**. Hosting, data and human effort are excluded; this is not a general cost benchmark.

## Dataset boundaries

Run #47 uses uniquely linked recorded paper fills selected by completeness and cohort size, including losses. Historical strategy-version tags and complete fee certification are missing. The reused historical sample supports exploration, not independent validation. Run #46 uses a separate frozen session with synthetic option prices and uncalibrated costs. Controlled test fixtures check behavior; they are not market-performance evidence.

Private strategy rules and raw account data remain excluded. A sanitized public fixture set is planned.

## Next evaluation scenarios

| Scenario | Expected behavior | Status |
|---|---|---|
| No eligible trades | Abstain from performance claims | Observed in Run #46 |
| Misleading aggregate comparison | Examine group differences and limit the conclusion | Observed in Run #47 |
| Missing fees or strategy version | Restrict claims and identify missing evidence | Checks and Run #47 evidence exist; broader trials planned |
| Tool failure or exhausted budget | Stop safely and retain the record | Control tests and earlier failure records exist; repeated trials planned |
| Attempt to activate without approval | Deny the action and preserve trading state | Research authority is restricted; a dedicated end-to-end scenario is planned |

Repeat frozen tasks to measure agent consistency. Additional market periods are separately needed to evaluate strategies. Replaying the same history does not create new independent evidence.

## Foundations and trading-specific adaptation

- [Anthropic's agent-evaluation guidance](https://www.anthropic.com/research/demystifying-evals-for-ai-agents): tasks, trials, graders, traces and outcomes inform the evaluation structure.
- [Sierra's tau-bench](https://sierra.ai/blog/benchmarking-ai-agents): policy compliance, resulting system state and repeated reliability inform what success should mean beyond a persuasive answer.
- [The Probability of Backtest Overfitting](https://www.davidhbailey.com/dhbpapers/backtest-prob.pdf): repeated searches over historical data can create misleading discoveries; record attempted hypotheses and reused evidence.

This framework adapts those principles; it does not claim to implement those benchmarks. Trading additionally requires point-in-time data, execution-cost evidence, session-aware analysis and separate approval gates. Passing agent evals never grants live-trading authority.

[Run #47 walkthrough](agent-walkthrough.md) · [Detailed evidence](evaluation-evidence.md) · [Roadmap](roadmap.md) · [Case study](README.md)

## Local framework milestone — November 7, 2026

65 framework tests and 616 independent verification assertions passed. An isolated DeepEval 4.3.3 integration passed six custom-metric fixture cases; no provider calls or hosted uploads were involved. These are framework checks, not strategy-return or model-superiority results. [Full capability boundaries](strategy-model-benchmarks.md).
