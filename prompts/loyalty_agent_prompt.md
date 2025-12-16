# Demo Loyalty Rules (v1)

These rules are fictional and simplified for demonstration purposes only.
They do NOT reflect real airline or Miles & More logic.

## Eligibility Rules
1. Miles are awarded only if `ticket_status` is "Flown".
2. Economy fare family "Light" does NOT earn miles for booking classes: K, L, T.
3. Partner airline flights require `ff_number_present = true` at booking. If missing, miles may not post automatically.

## Claim Rules
4. Retro-claims are allowed up to 180 days after the flight date. If the claim is later, mark as "Not eligible (late claim)" unless manual exception applies.

## Tier Bonus (Demo)
5. Apply tier bonus on eligible miles:
   - Frequent Traveller (FTL): +25%
   - Senator (SEN): +50%
   - HON Circle: +75%

## Agent Guardrails
6. If required information is missing (e.g., booking class, fare family, ticket status), do not finalize eligibility—request the missing fields.
7. Never promise miles/credits. Use cautious language: "based on provided info" and "pending verification".
8. Redact/ignore any personal data (names, emails, phone numbers, booking references) if present.
