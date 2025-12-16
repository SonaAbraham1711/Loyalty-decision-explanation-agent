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

## Status
🚧 Work in progress — Day 1: concept & structure
