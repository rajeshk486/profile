# Engineering Chapter Lead — Full Interview Question Bank & STAR Frameworks

Built against your JD: 4 squads, 18–25 FTEs, DORA/DevEx/Hiring/Engagement KPIs, matrix model separating engineering leadership from product ownership.

---

## 1. People & Talent Management

**Core Questions**
- How do you structure a hiring bar so 4 squads hire consistently without you personally sitting in every loop?
- Tell me about a low performer you managed out. What was your process?
- How do you handle a high performer threatening to leave over comp or growth?
- Describe your performance calibration process across squads with different Domain Leads/PMs.
- How do you build a promotion case for a senior engineer when the evidence is scattered across product teams you don't own?

**Scenario-Based**
- Two squad leads disagree on whether an engineer is "Senior" or "Staff" ready. You have final say. How do you resolve it without alienating either lead?
- You inherit a 22-person org with 3 open reqs that have been unfilled for 6 months. Hiring Fulfillment is a tracked KPI. What's your first 30 days?

**STAR Framework Hint**
- **Situation/Task**: Anchor on your 9-person team (2 SDE2s, 7 SDE1s) on the API migration program — real headcount, real seniority spread.
- **Action**: Talk concretely about how you calibrated expectations across SDE1→SDE2, how you gave feedback during a stalled 18-month program.
- **Result**: Quantify — retention, promotion, delivery recovery after the escalation you ran.

---

## 2. Delivery & Engineering Metrics (DORA)

**Core Questions**
- Walk me through establishing a DORA baseline when no telemetry exists.
- Which DORA metric do you weight most, and why, for a team doing legacy-to-modern migration work?
- How do you prevent Change Failure Rate from being gamed once teams know it's tracked?
- Cycle time is up 30% this quarter. How do you diagnose whether it's a people, process, or architecture problem?
- How do you report DORA metrics upward without turning them into a stick that damages psychological safety?

**Scenario-Based**
- Deployment frequency looks great, but MTTR is silently climbing. Leadership only asks about deploy frequency. How do you surface the real risk?
- Two squads have wildly different cycle times — one ships daily, one ships biweekly — but both claim their work is "harder." How do you evaluate that claim?

**STAR Framework Hint**
- **Situation**: Your API migration program was stalled 18 months with **zero production migrations** — that's a real "no baseline, no trust" starting point.
- **Task**: Establishing what "done" and "shipped" even meant before you could measure anything.
- **Action**: The escalation deck / accountability meeting you ran — frame this as forcing a metrics-and-accountability reset, not just a political move.
- **Result**: Whatever changed post-escalation — migrations unblocked, ownership clarified.

---

## 3. Technical & Architectural Oversight

**Core Questions**
- How do you stay technically credible when you're no longer writing production code daily?
- Describe how you evaluate an architecture decision (e.g., build vs. buy, sync vs. async) without becoming the bottleneck.
- How are you thinking about AI-supported development — where does it help, and where do you set guardrails?
- How do you know when a "golden path" (paved road for idea→deploy) is helping vs. becoming a straitjacket for senior engineers?
- Give an example of a technical standard you pushed org-wide and how you got buy-in from engineers who disagreed.

**Scenario-Based**
- A senior engineer wants to introduce a new pattern (e.g., a new gateway, a new agent framework) outside your golden path. How do you evaluate it without either rubber-stamping or blocking innovation?
- Design a golden path for idea→production for a 4-squad org where one squad ships daily and another ships monthly regulated changes. Where do you allow divergence?

**STAR Framework Hint**
- **Situation/Task**: Your token-management/GSU stack (LLM routing, priority queues, Apigee shared flow, fail-open compression sidecar) is a strong "I set an architectural standard under real constraints" story — GCP/GKE, AlloyDB policy store, explicit build-vs-buy calls (Redis vs Valkey pending legal).
- **Action**: Emphasize *decision-making under ambiguity* — you evaluated LiteLLM/RouteLLM/Kong before committing, made a fail-open safety call.
- **Result**: Frame the outcome as capacity protection / cost control, even if still in progress — "in-flight, here's the guardrail already delivering value."
- Second option: the self-healing pipeline (RCA → confidence-gated auto-MR) — great example of setting a *technical standard for safe automation* (70/100 threshold before auto-commit) — ties directly to "AI-supported development" in the JD.

---

## 4. Stakeholder & Matrix Management

**Core Questions**
- This role explicitly separates engineering leadership from product ownership. How do you handle a PM who wants to dictate technical sequencing?
- Describe a time a Domain Lead or Architect overruled an engineering decision you thought was right. What did you do?
- How do you push back on a delivery date you know is unrealistic, without becoming "the blocker"?
- How do you align squads' technical roadmap with product roadmap when the two are naturally in tension?

**Scenario-Based**
- A PM commits a delivery date externally before checking with you. Engineering isn't ready. What's your move in the next 24 hours?
- Your squads depend on another Chapter Lead's team for a shared service, and that dependency is now blocking your sprint. How do you resolve it without escalating to your VP every time?

**STAR Framework Hint**
- Use the API migration escalation again but from the *stakeholder friction* angle: "product ownership failures" were explicitly part of what caused the 18-month stall — this is your strongest matrix-management story. Be ready to narrate the actual conversation, not just the outcome.

---

## 5. Team Health, DevEx & Culture

**Core Questions**
- Walk me through your systematic process for discovering developer friction — qualitative and quantitative.
- How do you distinguish "engineers are unhappy" from "engineers are unproductive"? They're not always the same thing.
- Describe a time you invested in tooling/DevEx at the cost of a delivery deadline. How did you justify it?
- How do you keep engagement high on a squad doing "unglamorous" work (e.g., legacy migration, maintenance)?

**Scenario-Based**
- Engagement survey shows one squad scoring notably lower than the other three. You have no obvious incident or attrition to point to. How do you investigate?
- Pipeline telemetry says builds are fast, but engineers report "everything feels slow." How do you reconcile the two signals?

**STAR Framework Hint**
- **Situation**: A 9-person team doing multi-year migration work is a textbook "morale risk on unglamorous work" scenario — use it directly.
- **Action**: If you ran retros, 1:1s, or informal pulse-checks during the stalled period, that's your qualitative-signal story. Pair it with whatever pipeline/GitLab telemetry you had (MR cycle time, review latency) as the quantitative side.
- **Result**: Tie back to what stabilized once the program was unblocked.

---

## 6. Change Management & Strategic Thinking

**Core Questions**
- Tell me about a time you drove a technical initiative top-down against resistance from senior ICs.
- How do you sequence a multi-quarter initiative (e.g., a platform migration) so leadership sees progress every quarter, not just at the end?
- What's a technical decision you made that you later reversed? What changed your mind?
- How do you introduce AI-supported development practices to a team without it feeling imposed?

**Scenario-Based**
- You're six months into a golden-path rollout and adoption has stalled at 40%. Leadership is asking why. What do you do?
- You need to sunset a legacy system three squads still depend on. Two of the three are resistant. How do you sequence the migration?

**STAR Framework Hint**
- The 140-API C#/Oracle → Java/Spring Boot on GCP migration *is* your multi-quarter, high-resistance change story. Structure it explicitly: **Situation** (18 months stalled, zero migrations) → **Task** (unblock and re-baseline) → **Action** (escalation deck, accountability meeting, re-sequencing) → **Result** (whatever concrete recovery followed). This is your single best story — reuse it across categories 2, 4, and 6 with a different lens each time.

---

## 7. Leadership Philosophy & Self-Awareness

**Core Questions**
- What's a mistake you made as a manager that you'd do differently today?
- How do you define success for yourself in this role at the 6-month mark? At 18 months?
- How do you decide when to make a call yourself vs. push the decision down to a squad?
- What's your approach to feedback — both giving and receiving it?

**Scenario-Based**
- You disagree with your VP's directive on a technical or people decision. How do you handle it in the room vs. after?

**STAR Framework Hint**
- Keep this one honest and specific — a real miscalibration (e.g., escalating too late on the migration stall, or a people call you'd sequence differently now) lands better than a polished non-answer. Interviewers at VP level can smell a fake "weakness."

---

## How to Use This

1. Pick **one flagship story** (your API migration program) and rehearse narrating it from 4 different angles — metrics, stakeholder conflict, change management, team health. Same facts, different emphasis.
2. Keep a **second-tier story bank**: self-healing pipeline (technical standards/AI-dev), token-management stack (architecture under constraint), multi-agent scrum system (process innovation).
3. For every answer, force yourself to end on a **Result** with a number or concrete outcome — vague endings are the #1 gap in EM-level interviews.
