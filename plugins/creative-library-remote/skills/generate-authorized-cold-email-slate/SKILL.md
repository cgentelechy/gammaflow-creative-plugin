---
name: generate-authorized-cold-email-slate
description: Generate exactly three database-grounded cold-email sequences with three emails each from a webpage, product brief, screenshot, or campaign idea using one authorized, de-identified GammaFlow email reference packet. Use when the user asks for three cold-email sequences, a 3x3 email slate, or remote creative-library email generation.
---

# Generate an Authorized Cold Email Slate

Create exactly three strategy lanes. Each lane contains a first-touch email, a real follow-up, and a final email.

## Workflow

1. Inspect the supplied material and create a compact campaign brief containing sender, sender company, audience, relevance premise, problem, desired outcome, offer, verified proof, personalization variables, and one conversion action. Ask one question if the conversion action cannot be inferred safely.
2. Call `consume_email_reference_packet` exactly once with the campaign brief. Never attempt another private retrieval in the same authorization.
3. Treat the returned packet as one de-identified sequence blueprint. It may synthesize several role-correct records internally. Never ask for, infer, expose, or mention source names, source text, database IDs, ranking data, or retrieval details.
4. Generate exactly three sequences:
   - direct problem-to-outcome;
   - useful insight or value-first;
   - controlled creative pattern.
5. Keep the audience, offer, proof, and conversion action consistent across all three. Email 2 must advance the thread. Email 3 must close or redirect the conversation without pretending to be a new first touch.
6. Return a comparison table, then all nine emails in send order with subject, body, CTA, required personalization, and recommended timing.

## Guardrails

- Use one conversion action per sequence.
- Never invent personalization, proof, customers, results, urgency, or triggering events. Use variables such as `{{company_trigger}}` when facts are missing.
- Do not copy recognizable source phrasing.
- Use the packet once; subsequent edits must rely on the generated work and conversation context already present in this task.
- Do not expose inspiration, citations, source IDs, or lineage details.
- Follow-ups must progress the thread rather than restating email 1.
