# Detailed evaluation evidence — through Run #46

**Verified November 6, 2026 · Initial integration validation · Trading strategy withheld**

## Latest milestone: historical-backtest integration

**Run #46 completed in Replit with the real model and existing ReplayEngine.** It read memory, requested a base-cost replay, requested a higher-slippage replay, and concluded with abstention. Both modes processed 390 bars from one frozen historical session. Neither admitted trades: the declared synthetic pricing assumptions produced no contracts meeting eligibility. This is evidence of integration and restrained interpretation, not of winning or losing trades.

| Check | Verified result | Interpretation |
|---|---|---|
| Focused final suite | **60/60 pass in Replit:** 32 agent regressions + 28 historical integration checks | Includes controlled accounting/full and partial exits, timing, input integrity, unsupported modes, access and request isolation; not 60 model-quality trials |
| Actual model/tool integration | Run #46, four model calls, 6,902 tokens; recorded model-cost estimate $0.0028892 | Real engine invocation, not a mock; model cost excludes hosting/data/human effort |
| Historical replay | Base and stressed costs: 390 bars each, zero trades | No performance inference; zero-trade accounting alone does not validate nonzero fills |
| Executable-quote mode | Explicitly rejected in a separate check | Missing verified quote event times, entry-to-exit quote paths and execution-cost calibration |
| Protected state | Before/after settings, order counts and protected-source hashes unchanged | No orders or strategy activation |
| Failure retained | Run #45 stopped without a usable replay result | The exact termination cause was not established; adapter changes preceded the successful run |
| Independent evidence review | Saved trace, replay outputs, usage totals and ten deployed-source hashes checked | Reproduction of stored evidence, not a new provider run |

The supported scope is one host-selected session, frozen historical SPY bars, synthetic option pricing and explicit base/stress assumptions. It reuses the legacy engine with restricted inputs; equivalence to the current paper strategy is not established. Cost-accounting behavior is tested, but costs are not empirically calibrated. No confidence score, fresh holdout result or live readiness is claimed.

## Earlier agent milestone

### What was evaluated

One bounded, tool-using research agent was added to the existing worker. It investigates frozen development evidence, reads experiment memory and produces an advisory conclusion. Metrics and disposition rules are computed by the host. The fixed workflow remains the baseline.

## Scored evidence sheet

| Check | Evidence | Result and scope |
|---|---|---|
| Agent controls and integration adapter | 32 tests with simulated model responses, run locally and in Replit | **32/32 pass**; not a model-quality success rate |
| Existing paper safeguards | Regression test log | **52/52 pass**; mocked/offline checks |
| Existing workflow regression | Post-change and pre-change reproduction | **One known failure remains**, reproduced before the agent change; the full repository suite is not claimed green |
| Evidence fidelity | Recompute reported cohort arithmetic from frozen source rows | **Pass** for saved analyses in all three integration runs |
| State and authority | Compare protected state before/after each run; activation eligibility | **Pass** in all three recorded runs; no strategy activation |
| Provenance and usage | Verify source hashes, same-input baseline hash and usage totals | **Pass** in saved-evidence reproduction |
| Real model integration | Three actual OpenAI runs across versions | Final version completed; earlier failures retained below. This is iteration evidence, not a three-trial reliability benchmark. |
| User impact | Review effort, investigation time, usefulness | **Not measured yet** |

## Failures that changed the design

| Observed behavior | Response | Verification |
|---|---|---|
| An explanation described a narrower scope than the analysis actually used | Validate explanation scope against tool arguments | Added regression coverage; final run completed under the revised checks |
| Rejected or unavailable evidence prompted further investigation until the call budget ran out | Reserve the last call for a conclusion or explicit abstention | Budget behavior tested; next real run completed |
| Previously used historical evidence could be mistaken for a fresh holdout | Preserve evidence lineage and mark it exploratory | Final run remains awaiting independent evaluation; no promotion eligibility |

Of the initial three runs, the first completed but had an explanation defect. The second stopped at its budget and abstained. The third completed with a **reject** result under host evidence rules. Failure runs are retained privately, not removed from the record.

## Baseline comparison and limits

The agent and fixed workflow used the **same frozen source snapshot**. The model received only the development partition. The fixed workflow withheld a proposal because unused evaluation evidence was unavailable; the agent explored development evidence and reached a rejection. Neither produced an eligible strategy change.

The two paths perform different jobs: exploration versus eligibility screening. This is an integration/control comparison, not a matched-task test of usefulness or proof that the agent outperforms the fixed workflow. The earlier Run #44 used six model calls and 7,031 tokens; the recorded model-usage cost estimate was approximately **$0.003**, excluding hosting, data and human effort. This is a single observed run, not a general cost or latency benchmark.

No independent holdout, realistic options profitability, live readiness, general hallucination rate or time saving is established by these runs. Archived strategy screens are a separate evaluation and are not counted as agent validation.

## Remaining portfolio evidence

- A sanitized working demonstration and short video walkthrough.
- A matched-task comparison with the same data, approved tools and resource constraints, including tasks where a capable fixed workflow should be sufficient.
- Timed personal review tasks and structured feedback from the owner. External trading-product adoption is not required at this research stage.

Private evidence includes versioned source snapshots, recorded model/tool traces, test logs, a frozen-input baseline comparison and a reproduction script. Public material omits raw trades, tool arguments identifying strategy hypotheses, sensitive parameters and account information.

## Evaluation datasets and remaining coverage

| Evidence set | Scope | Limitation |
|---|---|---|
| Frozen signal-development snapshot | Recorded signal features and directional SPY outcomes used in earlier agent checks | Exploratory evidence; not executable options P&L or a fresh independent holdout |
| Frozen historical replay packet | One replay session plus warmup bars; input integrity checked by hash | Synthetic option pricing and uncalibrated costs; not one- or two-year strategy validation |
| Controlled test fixtures | Simulated responses and accounting/control scenarios, including nonzero exits | Test fixtures validate specific behavior; they do not measure real-model reliability or market returns |

Dataset documentation identifies scope and provenance; raw private datasets are not published. A public sanitized fixture set remains planned.

## Separate evaluation tracks

**Agent quality:** tool selection, faithful use of evidence, justified conclusions/abstentions, permission compliance, reliability, latency and cost. Current checks establish limited integration/control behavior; repeated matched-task quality scores and a general success rate remain unmeasured.

**Strategy quality:** independent observations, performance after justified costs, uncertainty, drawdown, regime coverage and operational safety. Current agent runs establish no live-eligible strategy. Paper testing cannot establish actual live fills.

**User usefulness:** review effort, corrections and time to an evidence-backed decision, measured against a capable fixed workflow. These are planned measurements, not achieved outcomes.

[Real Run #46 walkthrough](run46-walkthrough.md) · [Planned next and AI SDLC](roadmap.md) · [Case study](README.md)

[Current evaluation framework](evaluation.md) · [Run #47 walkthrough](agent-walkthrough.md)
