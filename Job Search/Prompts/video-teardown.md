You are analyzing a video as raw material — not summarizing it.

Read it the way a principal-level product strategist, systems thinker, and founder would read
it: someone expected to hold a defensible position on how markets and organizations actually
behave, not just on what to ship next. Assume full PM vocabulary; explain nothing a
practitioner already knows.

Your job is NOT to summarize the video or tell me what I should believe. Your job is to extract
the raw intellectual material, tensions, evidence, assumptions, contradictions, implications,
and possibilities that let me form my own opinions.

The core objective:

> Turn someone else's thinking into material I can interrogate, test, connect, and reason
> about myself.

## How the sections relate

The analysis moves in one direction, and I sit at the end of the chain:

  SOURCE → CRITIQUE → MODEL → REALITY CHECK → EXPLORE → TEST → QUESTION

  §1 Source         What was actually said?
  §2 Critique       Is the reasoning sound?
  §3 Model          What is the underlying system?
  §4 Reality check  Does it survive contact with the real world?
  §5 Explore        What territory does this open?
  §6 Test           What could actually be investigated or built?
  §7 Question       What do I need to figure out?

Each lens has a distinct job. §2 tests the argument. §3 models the system. §5 explores what the
argument makes possible. Use a lens only when it adds something new — do not process the same
idea three times in three voices. If a claim was already dismantled in §2, it does not need
re-dismantling in §5; carry forward only what the new lens changes.

## Labels

For every claim attributable to the speaker, include a timestamp when available. Distinguish
clearly between:

* Speaker said
* Direct inference
* Your analytical extension
* Speculation / hypothesis

Do not blur these categories.

## Depth override

If I have written a depth below, use it and skip the counting in Step 0. Step 0 still runs;
its count becomes informational only.

DEPTH OVERRIDE: [SHALLOW / STANDARD / DEEP / none]

---

# STEP 0 — TRIAGE (output this first, before any analysis)

Emit this block and fill it in. Your later output must stay consistent with it.

  Timestamps present in source:        yes / no

  Non-obvious claims found:            [count]
    Count a claim only if it would surprise a PM with ~8 years of experience — someone who
    already knows discovery, prioritization, stage differences, and the standard frameworks.
    Do NOT count: restatements of common practice, war stories without a generalizable claim,
    tactical advice, or anything that would fit on a conference slide without objection.
    List each counted claim in one line. If you cannot write the line, it does not count.

  Claims resting on a single company
    or anecdote:                       [count]

  Contradiction present:               yes / no
    Only yes if you can name, in one line, the specific mainstream practice or the speaker's
    own earlier statement being contradicted. Rhetorical framing ("most people get this
    backwards") does not qualify on its own.

  Transferable mechanism:              yes / no — name it in one line

  Implied product or market gap:       yes / no — name it in one line

  DEPTH: [SHALLOW / STANDARD / DEEP]
  SECTIONS I WILL RUN: [list]
  SECTIONS I WILL SKIP: [section] — skipped because [what was absent from the source]

Routing rules — apply mechanically, do not override:

  Fewer than 3 non-obvious claims        → SHALLOW
  3–6 non-obvious claims                 → STANDARD
  7+, or a named contradiction           → DEEP

  SHALLOW  → run §1, §2, §7 only. Stop there. Do not run §3, §4, §5, §6.
             A shallow video is a normal outcome, not a failure. Say so plainly.
  STANDARD → run §1, §2, §4, §7. Run §3 only if the idea has actors and feedback loops beyond
             the speaker's own team. Run §5 and §6 only for claims marked as contradictions.
  DEEP     → run everything.

  Timestamps = no          → drop the timestamp requirement everywhere, state it once, and do
                             not approximate or invent positions.
  No transferable mechanism → the cross-industry part of §4 is omitted, not attempted.
  No implied gap            → the opportunities part of §6 is omitted, not attempted.

---

# 1. CORE IDEAS & ARGUMENT MAP

Identify the video's genuinely important ideas — not everything that was said.

For each important idea:

### Claim
What is the speaker actually saying?

### Timestamp
Where does the speaker say it?

### Observation
What does the speaker observe or describe?

### Interpretation
How does the speaker interpret that observation?

### Assumption
What has to be true for that interpretation to hold?

### Conclusion
What does the speaker conclude from it?

### Why It Is Interesting
What makes this worth thinking about?

Then identify the small number of ideas that contain disproportionate intellectual value. Do
not force a fixed number.

Also identify ideas that are merely conventional, tactical, anecdotal, obvious, or
context-specific — so I know what *not* to overthink.

---

# 2. INTERROGATE THE THINKING

**Job of this section: is the argument sound?** Nothing else.

Act as a skeptical but intellectually honest challenger.

For each important claim:

**Claim → Evidence → Assumption → Logic → Missing variable → Counterargument**

Look for: hidden assumptions, logical leaps, overgeneralization, survivorship bias, selection
bias, correlation vs. causation, incentives that could distort the conclusion, omitted
stakeholders, omitted costs, omitted constraints, and situations where the opposite could be true.

Ask:
> What would a strong operator challenge here?
> What would have to be true for the speaker to be wrong?
> What would have to be true for the speaker to be right?

### Falsification & Updating

For the load-bearing claims only — not every claim:

* What evidence would materially **strengthen** this claim?
* What evidence would materially **weaken** it?
* What single observation would force reconsidering the underlying assumption?

This is about updating, not just disproof: what should move my confidence, and in which direction.

Do NOT resolve every disagreement for me. Where there is genuine ambiguity, preserve it.

---

# 3. FIRST PRINCIPLES + SYSTEMS + SECOND-ORDER EFFECTS

**Run only if Step 0 listed this section. If it did not, output "§3 — skipped per Step 0" and
move on.**

**Job of this section: what happens if the argument is true?** Assume it holds; model the system.

Strip away context and determine what might be fundamental.

Separate: **fundamental principle** from **current convention**, **organizational habit**,
**historical artifact**, **technology constraint**, **incentive-driven behavior**.

Ask:
> If we designed this from scratch, what would still be true?

Then model the surrounding system: actors, incentives, dependencies, constraints, feedback
loops, bottlenecks, power dynamics, network effects, switching costs, information asymmetry.

For each important idea, trace:

**First-order effect → Second-order effect → Third-order effect**

Pay particular attention to: unintended consequences, behavioral adaptation, competitive
response, new bottlenecks created by the solution, situations where optimizing one part harms
the system, and situations where solving today's problem creates tomorrow's.

---

# 4. REAL-WORLD CONTRADICTIONS & CROSS-INDUSTRY LENSES

**Run only if Step 0 listed this section. If it did not, output "§4 — skipped per Step 0" and
move on.**

Test the ideas against how the product world actually functions.

### Companies
incentives, organizational politics, decision rights, risk, capital allocation, revenue,
margins, existing customers, legacy systems

### Product Organizations
discovery, prioritization, roadmap pressure, stakeholder management, experimentation, technical
constraints, launch, adoption, monetization

### Company Stage
**Startup → Growth / mid-size → Large company**

For each principle, state explicitly whether it becomes **MORE true or LESS true as the company
scales** — and name the principles that silently assume one stage while being presented as
universal. Also identify where a principle changes meaning, stops working, or requires a
different implementation.

Then examine whether the idea changes across:
**Zero-to-one → Product-market fit → Scaling → Mature product**

### Cross-industry parallels
Omit entirely if Step 0 found no transferable mechanism.

**Video concept → Industry/example → Common mechanism → What the comparison reveals**

Candidate industries: AI, software, fintech, payments, healthcare, e-commerce, marketplaces,
enterprise SaaS, infrastructure, manufacturing, logistics, automotive, media, gaming, energy,
retail, education.

Do not generate generic analogies to fill this section. Refuse forced comparisons and say so.

---

# 5. INTELLECTUAL EXPLORATION MAP

**Run only if Step 0 listed this section. If it did not, output "§5 — skipped per Step 0" and
move on.**

**Job of this section: what territory does the argument open up?** Not whether it's right —
that was §2.

For each high-value opportunity, trace:

**Speaker's idea**
↓
**Hidden assumption**
↓
**Tension / contradiction**
↓
**What logically follows**
↓
**What might also be true**
↓
**Unexplored question**
↓
**Testable hypothesis**
↓
**Potential experiment**
↓
**Potential product / business implication**

Prioritize: ideas that challenge conventional thinking, contradictions that reveal deeper system
dynamics, assumptions that are rarely questioned, implications the speaker didn't pursue, ideas
that change meaning at different company stages, ideas that become more interesting in another
industry, emerging constraints, newly possible products, markets where the existing workflow
looks structurally broken.

Label every step that goes beyond the source as **Inference / Extension / Speculation**. Do not
present your extensions as things the speaker said.

---

# 6. HYPOTHESES, EXPERIMENTS & OPPORTUNITY SPACES

**Run only if Step 0 listed this section. If it did not, output "§6 — skipped per Step 0" and
move on.**

## Hypotheses

**Hypothesis** | **Why it might be true** | **What would make it false** | **Evidence currently
available** | **Evidence missing** | **Cheapest way to test it** | **What result would change
the hypothesis**

Favor hypotheses that are genuinely uncertain and decision-relevant. Prefer tests that produce
signal in under two weeks using tools I already have.

## Product / Business Opportunities

Omit entirely if Step 0 found no implied gap.

Look for: problems that should exist as products but don't; workflows still handled through
spreadsheets, email, meetings, or manual coordination; missing infrastructure or software
layers; broken interfaces between teams or systems; opportunities created by AI or automation;
problems caused by increasing organizational complexity; opportunities created by changing
incentives, regulation, or technology costs.

For each serious opportunity:

**Problem** | **Who experiences it** | **Current workaround** | **Why existing solutions are
inadequate** | **Insight from the video that led here** | **Potential product** | **Why now** |
**Potential moat** | **Distribution** | **Business model** | **Biggest risk** | **What must be true**

Distinguish: **Already exists** / **Existing category with an interesting variation** /
**Potentially novel category**. Do not claim something is new without evidence.

## Decision Lens

For the most decision-relevant bet or opportunity surfaced by the video — **if one exists**:

**Worst plausible outcome** | **Likelihood** | **Preventable?** | **Recoverable?** |
**Reversible or irreversible?** | **Cost of doing nothing** | **What would have to be true for
the upside to be much larger than I currently believe**

Separate **real risk** from **psychological risk** from **organizational risk** from
**status-quo bias**.

If no meaningful bet emerges, say so and skip. Do not invent one.

---

# 7. QUESTIONS FOR ME — NOT ANSWERS FOR ME

**Always runs, at every depth.**

Do NOT tell me what my opinion should be.
Do NOT write "My Independent View."
Do NOT tell me what I now believe.

### Questions That Challenge My Assumptions
Questions that force me to reconsider how I normally approach products.

### Questions About the Speaker
Where the argument remains incomplete, questionable, or assumption-dependent.

### Questions About the Real World
Whether the ideas survive contact with actual companies, markets, customers, incentives, and
organizational constraints.

### Questions Worth Investigating
Where external evidence, customer research, experiments, or deeper study could materially change
the conclusion.

### Questions That Could Lead to a Product
Unresolved problems or tensions that could become opportunities.

### Questions I Should Carry Forward
The few worth remembering long after I stop thinking about the video itself.

---

# FINAL: INTELLECTUAL FRICTION SUMMARY

Include only rows the run actually covered. Leave the rest out rather than filling them.

| Dimension | Finding |
| --- | --- |
| Strongest claim | |
| Most interesting observation | |
| Biggest hidden assumption | |
| Most questionable inference | |
| Strongest counterargument | |
| Evidence that would most change my assessment | |
| Most important contradiction | |
| Most interesting second-order effect | |
| Best first-principles question | |
| Best systems-thinking question | |
| Most useful cross-industry parallel | |
| Most promising hypothesis | |
| Cheapest useful experiment | |
| Most interesting unexplored opportunity | |
| Most important unanswered question | |

Then:

## "If I were going to think deeply about only the ideas from this video, these are the tensions I would sit with."

Do not resolve the tensions. State them as open intellectual problems.

---

# CLOSING RECONCILIATION

End with:

  "Ran [sections] at [depth]. Skipped [sections] because [reason]."

If what you ran does not match Step 0, state the mismatch as the first line of this block.

---

# ENFORCEMENT

Never manufacture depth. A short, honest analysis of a thin video is a correct outcome.

If the speaker does not discuss something: **"Not meaningfully addressed in the source."**

If you make an analytical extension, label it.

If an idea is primarily your own synthesis rather than something implied by the video:
**Model-generated extension**

If a factual claim requires external validation, say so.

If timestamps are unavailable, state explicitly that timestamps could not be verified.

If you find yourself restating an insight an earlier section already covered, cut it and
reference the earlier section instead.

Quality is measured by **fidelity to the source + quality of reasoning + useful intellectual
tension** — not by the number of insights produced.

---

SOURCE: [paste link or transcript]
CONTEXT: [optional — your domain, what you're weighing right now]