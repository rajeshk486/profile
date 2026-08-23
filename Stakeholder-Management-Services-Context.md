# Chapter Lead — Stakeholder Management Scenario Bank (Services / Client-Delivery Context)

Same pattern-based approach, reframed for a **services company**: stakeholders now include external clients, account/delivery managers, pre-sales, and compliance — not just internal PMs. Contracts, SLAs, and billability replace "product roadmap" as the pressure source.

---

## Pattern 1 — Client Over-Commits Without Engineering Sign-Off

**What it's testing:** Whether you protect delivery integrity when the commitment was made externally, by someone else, often before you were even in the room.

- An Account Manager promises a client a delivery date in a contract renewal call, without checking feasibility with you. What's your move?
- A client's steering committee is told a feature is "in progress" when your squad hasn't started it. How do you handle the gap?
- Pre-sales scoped a fixed-price SOW based on assumptions your team knows are wrong. What do you do once you inherit it?

**Answering pattern:** Separate "the commitment already made" from "what's still negotiable" (scope, phased delivery, resourcing). Show you fix the *upstream process* — e.g., mandatory engineering sizing sign-off before any external date is quoted — not just firefight this one instance.

---

## Pattern 2 — SLA / Contract Pressure vs. Engineering Quality

**What it's testing:** Whether you hold the line on quality when a missed SLA has real financial/contractual penalty attached.

- You're at risk of breaching an SLA (e.g., defect turnaround, uptime). Do you cut corners to hit it or take the penalty? Walk me through the decision.
- A client's contract has a fixed release cadence; your team's regression testing needs more time this cycle. How do you resolve it?
- How do you build slack into SLA commitments so one bad sprint doesn't cascade into breach?

**Answering pattern:** Frame it as risk math, not idealism — quantify the cost of a quality shortcut (production incident, penalty, trust) vs. the cost of the SLA miss, and show you make that tradeoff *visible* to the client/account team rather than deciding silently.

---

## Pattern 3 — Multi-Account / Multi-Client Resource Contention

**What it's testing:** Prioritization logic when squads are shared across paying clients with different commercial weight.

- Two clients on the same shared squad both escalate for priority in the same sprint. One is a bigger account. How do you decide?
- A high-margin client wants dedicated engineers pulled from a lower-margin account's squad. How do you handle the internal negotiation?
- How do you plan capacity across 4 squads when client demand is inherently unpredictable quarter to quarter?

**Answering pattern:** Name the actual allocation mechanism (contractual FTE commitments, account tiering, a capacity-planning cadence with Account/Delivery Managers) and show it's pre-agreed, not improvised under pressure — commercial stakeholders respect a rule set more than case-by-case pleading.

---

## Pattern 4 — Onshore–Offshore / Distributed Delivery Friction

**What it's testing:** Coordination across time zones and reporting lines that don't map cleanly to your org chart.

- Your offshore squad and an onshore client-facing team disagree on priorities, and you're not in the room when the client sets direction. How do you stay aligned?
- A client-side technical lead wants direct access to your engineers, bypassing your Delivery Manager. How do you handle it?
- How do you maintain engineering standards when a client's onshore team pushes for shortcuts your offshore squad has to implement?

**Answering pattern:** Establish a single accountable channel (you or a lead) for technical direction even when delivery/account management sits elsewhere, and be explicit about where engineering standards are non-negotiable regardless of who's asking.

---

## Pattern 5 — Pre-Sales / RFP Commitments Engineering Wasn't Consulted On

**What it's testing:** How you handle inheriting technical debt created before you had any input — a very common services-company failure mode.

- You discover the SOW promises a technical approach your squad thinks is wrong. How do you renegotiate without blowing up the client relationship?
- How would you build a process so Engineering has a voice in pre-sales estimation going forward?

**Answering pattern:** Don't relitigate the SOW publicly — go to the account owner with alternatives (same outcome, different technical path) rather than "this can't be done." Then propose the structural fix: engineering review gate before SOWs are signed.

---

## Pattern 6 — Account/Delivery Manager vs. Engineering Authority

**What it's testing:** Since Engineering is separated from delivery ownership, this tests decision-rights clarity — your JD's exact fault line, just with a commercial owner instead of a PM.

- A Delivery Manager wants to override your call on a technical risk to protect the client relationship. How do you handle it?
- Who has final say on a go/no-go release decision when the Delivery Manager and you disagree?

**Answering pattern:** Propose a clear RACI up front — Engineering owns technical risk sign-off, Delivery/Account owns commercial and relationship risk, both must agree to ship. If forced to choose, don't let commercial pressure override a hard technical red line (e.g., known data integrity risk) — but flag any override loudly to your own leadership.

---

## Pattern 7 — Compliance, Audit & Regulatory Stakeholders

**What it's testing:** Given your FinTech/mutual funds domain, this is a near-certain angle — regulatory stakeholders don't negotiate on timelines the way clients do.

- An audit finding requires a fix that conflicts with your sprint commitments to a paying client. How do you sequence it?
- How do you keep engineering velocity high while satisfying a compliance team that wants documentation/sign-off gates on every release?
- A regulator-driven deadline is non-negotiable and under-resourced. What do you do?

**Answering pattern:** Compliance/regulatory work is a *hard constraint*, not a priority to weigh — frame it that way explicitly, then show how you renegotiate everything else around it rather than trying to protect both simultaneously.

---

## Pattern 8 — Direct Client Escalation to Engineering

**What it's testing:** Composure and boundary-setting when a client goes over the Account Manager's head straight to you.

- A client executive emails you directly, angry about a delay, bypassing your Delivery Manager. How do you respond?
- A client wants to join your squad's daily stand-up to get visibility. How do you handle the request?

**Answering pattern:** Respond promptly and factually, but loop the account owner back in immediately rather than freelancing the relationship — show you protect the commercial relationship's chain of command even under direct pressure.

---

## Pattern 9 — Steering Committee / QBR Reporting

**What it's testing:** Same "translate upward" skill as an internal exec review, but now the audience is a paying client's leadership.

- How do you present a quarter where DORA metrics look bad for legitimate reasons (regulatory rework, migration) to a client steering committee?
- A client's QBR asks "why does it cost this much for what looks like a small feature?" How do you answer?

**Answering pattern:** Lead with business outcome and risk posture, not internal engineering metrics — clients care about value delivered and risk avoided, not cycle time. Translate DORA into "reliability and speed of getting your requests live," not raw numbers.

---

## Pattern 10 — Change Request (CR) / Scope Creep Negotiation

**What it's testing:** Whether you can hold a scope boundary in a commercial, contract-bound context without damaging trust.

- A client keeps adding "small" asks inside a fixed-scope SOW. How do you draw the line?
- How do you distinguish a legitimate CR from scope creep, and who makes that call — you or Delivery/Account?

**Answering pattern:** Show a lightweight, consistent CR-classification process (effort threshold, contract impact) agreed with Delivery/Account in advance, so the "no" (or "yes, but as a CR") is a process outcome, not a personal judgment call each time.

---

## Pattern 11 — Vendor / Third-Party Dependency Management

**What it's testing:** Managing stakeholders you have zero contractual leverage over.

- A third-party vendor's API delay is blocking your squad's commitment to a client. How do you manage both relationships simultaneously?
- How do you build contingency into client commitments when a chunk of the work depends on an external vendor's timeline?

**Answering pattern:** Buffer external dependencies explicitly in client-facing commitments rather than treating vendor risk as equivalent to internal risk; show you communicate vendor risk to the client proactively, before it becomes a miss.

---

## Pattern 12 — Trust Rebuilding After an SLA Breach or Missed Milestone

**What it's testing:** Recovery credibility with a paying client, which is commercially higher-stakes than an internal miss.

- After an SLA breach, the client wants weekly executive check-ins going forward. How do you rebuild confidence without over-indexing on reporting theater?
- Describe restoring a client relationship after a production incident tied to your team's release.

**Answering pattern:** Concrete recovery mechanics (smaller milestones, transparent risk logs, a visible corrective-action plan) — and an explicit exit criteria for when the extra oversight can taper off, so it reads as a plan, not permanent damage control.

---

## Key Reframe vs. the Product-Company Version

| Product-Company Lens | Services-Company Lens |
|---|---|
| PM owns roadmap | Account/Delivery Manager owns client relationship + commercial risk |
| Internal engagement/DevEx metrics | SLA, penalty clauses, contract terms |
| Domain Lead / Architect | Same, plus client-side technical counterparts |
| VP / leadership reporting | QBRs / steering committees with paying clients |
| Golden path adoption | Compliance/audit gates, often non-negotiable |

If you don't know which context the interviewer means, it's worth asking early — "is this a product org or a client-delivery model?" — since your framing (and your CAMS-relevant compliance stories) shifts meaningfully between the two.
