# Trading & Investment Tools

**Independent product development · Consumer fintech · Investment research · Options analytics**

As a self-directed investor, I encounter different questions at different stages of a decision: What deserves investigation? Which options contract fits the idea? Has anything changed that challenges why I own a stock?

I build and actively use tools around these questions in my own investing. They bring screening, market context, and investment reasoning into workflows I can inspect, evaluate, and improve through use.

My work combines product requirements, workflow design, and hands-on development. Using the tools myself creates an ongoing feedback loop: identify a need, build a capability, evaluate it in my investing workflow, and refine the experience.

**Current stage:** Built and actively used for personal investing, with ongoing validation and iteration. Each section distinguishes existing capabilities from planned improvements. Broader user adoption, commercial demand, and measured investment-performance improvements remain unvalidated.

## The collection

| Tool | Investor question | Core product decision |
|---|---|---|
| **Portfolio Intelligence** | Does my original investment thesis still hold? | Bring investment reasoning and changing market context together. |
| **Wheels Screener** | Which candidates deserve deeper options-income research? | Show the reasoning behind rankings and support follow-up analysis. |
| **LEAPS Scanner** | Where should I spend time researching long-dated options? | Filter inexpensive inputs before running deeper analysis. |
| **Swing Trading Tools** | Does this stock setup translate into a suitable options trade? | Separate opportunity discovery from contract selection. |
| **Multi-Timeframe & Options Analytics** | How should I interpret conflicting market signals? | Preserve component-level evidence alongside the overall interpretation. |

## Portfolio Intelligence

**The problem**

Investment theses and action notes live in a workbook, while market conditions change independently. Reviewing them separately makes it harder to connect a price move, approaching catalyst, or deteriorating indicator to the original reason for owning a stock.

**The product decision**

Use the existing workbook as the starting point, then place the thesis, scenario targets, invalidation conditions, and market context in one review experience. The initial scope supports portfolio review while keeping thesis editing in the established spreadsheet workflow.

**Built**

- Holdings dashboard with portfolio-category and ticker filters.
- Imported investment theses, scenario targets, catalysts, and decision journals.
- Daily market snapshots, attention flags, and ticker history.
- Manual import and refresh, with a configured scheduled-refresh path.

**Planned**

- Historical snapshots preserving the thesis and market context together.
- Clearer per-holding freshness and partial-refresh reporting.
- Improvements to import consistency and data-quality labeling.

**The tradeoff**

Reusing the workbook limits initial product scope, but updates still require re-importing. Preserving historical context is also essential: reviewing an old market snapshot beside today’s revised thesis can distort what the investor actually knew.

## Wheels Screener

**The problem**

An attractive options premium is only one part of evaluating a cash-secured put or covered-call opportunity. Investors also need to understand the underlying stock, market context, timing, and capital commitment.

**The product decision**

Provide a ranked shortlist with a detailed breakdown behind each candidate. Separate background scanning from browsing so stored results are available for inspection, with further analysis and refresh when needed.

**Built**

- Cached candidate screening and individual ticker analysis.
- Component scores, summaries, and supporting details.
- Put-options-chain lookup.
- Position tracking and wheel-lifecycle next-step logic.
- Scan status, refresh, pause, and resume controls.

**Next validation questions**

As I continue using and refining the tool, the questions to formalize are whether the explanations make rankings understandable, whether data freshness is clear, and whether users distinguish screening scores from probabilities of profit. Testing these with other investors would extend the evidence beyond my own use.

**The tradeoff**

Caching makes results readily available but introduces freshness concerns. Rankings simplify comparison, while their component explanations help users examine what the overall score conceals.

## LEAPS Scanner

**The problem**

Detailed long-dated-options analysis across a broad watchlist consumes time and market-data requests, including for stocks that fail basic suitability criteria.

**The product decision**

Use two stages: inexpensive checks based on quotes and company information, followed by deeper options analysis. Preserve exclusion reasons so filtering remains inspectable.

**Built**

- Prefiltering with recorded rejection reasons.
- Watchlist scans and individual ticker analysis.
- Table views with expandable details.
- Entry-plan and detailed-analysis endpoints.

**Planned or incomplete**

- Catalyst-aware prefiltering remains incomplete.
- Formal comparisons of API consumption and scan duration against the opportunities excluded by early filters.

**The tradeoff**

Early filtering can reduce unnecessary work, but stricter criteria may miss useful candidates. Ongoing validation needs to consider both efficiency and coverage.

## Swing Trading Tools

**The problem**

A directional view on a stock does not, by itself, establish that a particular options contract is suitable. Investors need to connect the setup’s timing and risk to the instrument they are considering.

**The product decision**

Support a progression from watchlist screening to ticker investigation and then contract review. Keep technical context and options suitability distinguishable within that workflow.

**Built**

- Watchlist and batch scanning.
- Ticker analysis with timeframe signals and market-structure views.
- Liquidity-level and pattern analysis.
- Options-contract analysis and position-tracking functionality.

**Next validation questions**

Further evaluation will examine whether the workflow makes disagreements between the stock setup and options suitability clear, which information supports a coherent thesis, and where repeated investigation or switching between tools remains necessary.

**The tradeoff**

More detail can improve understanding or increase cognitive load. The product challenge is surfacing the right information at each decision point.

## Multi-Timeframe & Options Analytics

**The problem**

Momentum, volatility, options positioning, and catalysts can point in different directions. Separate views make those disagreements difficult to compare.

**The product decision**

Combine the analytical layers while retaining their individual contributions. Make the basis of the overall interpretation available for inspection.

**Built**

- Single-ticker and batch-analysis endpoints.
- An analysis framework combining options, momentum, flow, volatility, and catalyst inputs.
- Component breakdowns, timeframe relationships, and narrative explanations.
- A separate gamma-exposure analysis view.

**Next validation questions**

Continued evaluation will focus on whether conflicting evidence is visible, how missing inputs affect interpretation, and whether score labels communicate their limitations accurately.

**The tradeoff**

Aggregation helps users scan complex information, but can create false precision. A computed score is not an established probability of a successful trade.

## How I’m validating and what comes next

**My own investing workflow is the first validation environment.** I actively use these tools, evaluate their usefulness, and iterate as my needs and understanding develop. That ongoing use informs product development; it does not substitute for broader user research or controlled measurement.

The next step is to make the evaluation more structured and test whether the workflows help other self-directed investors.

| Task | Evidence to collect |
|---|---|
| Review whether a holding needs attention | Completion time, missed information, and interpretation errors |
| Compare two options candidates | Ability to explain the ranking and identify relevant risks |
| Interpret conflicting market indicators | Recognition of uncertainty and missing evidence |

These structured measurements are proposed next steps, not reported results. Public demonstrations would use clearly labeled, independently generated synthetic data.

Commercial validation would examine what investors already use, which recurring problem would motivate switching, and whether willingness to pay could support data and operating costs. External adoption and sustainable economics remain hypotheses to test.

## What this work demonstrates

Building for my own investing gives me direct exposure to the decisions these products support. It also makes me responsible for evaluating the outputs, questioning their usefulness, and deciding what to improve.

The work connects product experience with technical and commercial choices: how much information to show, when deeper analysis is worth its cost, how to explain rankings, and where the investor needs control.

My focus is to keep improving the tools through personal use, make the learnings explicit, and establish which capabilities are valuable enough to serve a broader audience.

[Back to portfolio](../../README.md)
