# Run #47: testing an apparent market-condition effect

**Recorded paper outcomes · Validated November 7, 2026 · Strategy details private**

**Question:** Does a historical trading setup perform differently across two market conditions recorded at entry?

**Evidence:** 36 recorded paper trades across 12 sessions, including 10 gross winners and 26 losses. The cohort was selected by data completeness and size, not profitability. Public aliases protect the private setup and conditions.

## The walkthrough

| Evaluation dimension | What happened | Assessment |
|---|---|---|
| **Evidence** | Entry and exit fills were linked. Historical strategy versions and complete fee verification were missing. | Sufficient for limited historical exploration; insufficient to validate today's strategy. |
| **Analysis** | The initial comparison showed Condition A averaging 4.96 percentage points worse than Condition B. | Arithmetic verified; the groups required further comparison. |
| **Investigation** | The agent chose to compare trade directions. Among bullish trades, the difference reversed to about 1 point better in A. Bearish trades had no comparison group in B. | Useful follow-up: the original table mixed different kinds of trades. |
| **Decision and safety** | The agent requested better fill/fee evidence. Host controls prevented strategy activation. | Collect more evidence; the result did not justify a rule change. |
| **Usefulness and efficiency** | The follow-up exposed why the initial comparison could mislead. Four model calls cost approximately $0.0023 in estimated tokens. | Concrete research value; time savings and superiority over the fixed workflow remain unmeasured. |

These are retrospective assessments of one recorded run, not scores from a repeated-trial benchmark.

## The comparison in three rows

The metric is the average per-trade **gross return on entry premium**, not portfolio return or verified net profit.

| Comparison | Condition A | Condition B | Interpretation |
|---|---|---|---|
| All selected trades | 22 trades; mean −8.04% | 14 trades; mean −3.08% | A initially looks worse. |
| Bullish trades only | 12 trades; mean −2.08% | 14 trades; mean −3.08% | The ranking reverses when direction is matched. |
| Bearish trades | 10 trades, all losses | No observations | No matched comparison is possible. |

Different session dates and unknown historical strategy versions still limit the comparison. This does not establish why individual trades lost or prove that removing bearish trades would improve a strategy.

## What the agent chose—and what the system enforced

**Prescribed audit and initial comparison → agent-selected direction follow-up → agent-selected next evidence requirement → host-enforced no activation.**

A dedicated research adapter executed the run and saved its trace and deterministic results. It was launched through a verified script and displayed in the Experiments dashboard; this is not yet the generic research-button path or a recurring agent schedule.

**Takeaway:** The agent exposed a misleading aggregate comparison and helped identify the next evidence needed. It did not establish a better trading strategy.

## Verification and next step

Thirty focused tests passed, and 191 independent assertions checked the frozen run's calculations, trace and protected state. These are checks, not independent experiments. Trading controls and order counts remained unchanged.

Next: improve fill/fee and strategy-version lineage, then evaluate a predeclared comparison with overlapping trade directions on additional independent sessions. Automated isolated paper admission and human-approved live release remain planned.

[Evaluation framework](evaluation.md) · [Earlier Run #46](run46-walkthrough.md) · [Architecture](architecture.md) · [Roadmap](roadmap.md)
