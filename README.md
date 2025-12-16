# Loyalty Decision Explanation Agent (Demo)

## Overview
This project is a **demo AI agent** designed to explain airline loyalty
decisions (e.g. missing miles) in a clear, transparent, and human-readable way.

It focuses on **reducing customer support effort** and **building trust**
by explaining *why* a loyalty outcome occurred and *what the next best action is*.

> ⚠️ This is a **non-production demo** using simplified, fictional rules.
> It does NOT reflect real airline or Miles & More logic.

---

## Problem Statement
Airline loyalty programs receive a high volume of customer requests such as:
- “Why didn’t my miles post?”
- “Am I eligible for retro-claim?”
- “What information is missing?”

These cases are:
- rule-heavy
- time-consuming for agents
- frustrating for customers when explanations are unclear

---

## Why this is hard (example complexity)
Loyalty outcomes typically depend on multiple variables at once (carrier, booking class, fare family, tier bonuses, claim window, and missing data).
This demo simulates that complexity with simplified rules and **transparent explanations**.

---

## Solution
This AI agent:
- evaluates eligibility using **demo loyalty rules**
- explains decisions in **plain language**
- identifies **missing information**
- recommends **next best actions**
- drafts a **support-ready response**

The agent is designed with **Responsible AI guardrails**:
- no hallucinated facts
- no promises of miles or compensation
- clear assumptions and confidence levels
- escalation when human review is needed

---

## Sample Output (What the agent generates)

### Example: Eligible miles (demo)
DECISION:
- Overall: Eligible
- Confidence: Medium
- Estimated miles: 500–625 (demo estimate with FTL bonus)

SEGMENT BREAKDOWN:
- FRA → MXP | Carrier: LH | Cabin: Economy | Booking class: Y | Fare family: Classic
  - Eligibility: Eligible
  - Reason: Flown ticket + qualifying fare/booking class (per demo rules)
  - Estimated miles: ~500 base + 25% FTL bonus

MISSING INFORMATION:
- None

NEXT BEST ACTIONS:
- For the customer:
  - No action needed. If miles do not appear after the standard posting window, submit a retro-claim.
- For support agent:
  - If still missing, request ticket number + boarding pass for verification.

SUPPORT REPLY DRAFT:
Hello, thanks for reaching out. Based on the flight details you provided, this trip is eligible for mileage credit under our demo rules.  
If the miles don’t appear after the normal posting window, please share your ticket number and a copy of your boarding pass so we can verify and process the claim.

ASSUMPTIONS & RESPONSIBLE AI NOTES:
- Assumptions made: Route treated as short-haul for demo estimation.
- Human verification needed: Ticket/boarding pass validation before manual credit.

---

## Inputs (Demo)
- Flight segment details (JSON)
- Member context (tier, claim type, timing)
- Simplified loyalty rules (text)

---

## Outputs
- Eligibility decision (per segment)
- Explanation of decision
- Missing information (if any)
- Next best actions
- Customer support reply draft
- Assumptions & confidence notes

---

## Tech Stack
- Python
- Vertex AI (LLM inference)
- Gradio (UI)
- Cloud Run (deployment)
- GitHub (portfolio & version control)

---

## Future Enhancements (Optional)
- Add a small knowledge base (RAG) to retrieve policy/rules snippets.
- Extend to partner claims (hotel/car rentals) with separate eligibility logic.
- Add escalation workflows for high-tier members or ambiguous cases.

---

## Status
🚧 Work in progress — Day 1: concept & structure
