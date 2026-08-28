---
name: generate-authorized-ad-slate
description: Generate exactly 12 complete paid-ad concepts from a webpage, landing page, product brief, screenshot, or campaign idea using one authorized, de-identified GammaFlow creative reference packet. Use when the user asks for 12 ads, a broad ad ideation slate, image directions, or LinkedIn ad previews through the remote creative library.
---

# Generate an Authorized Ad Slate

Create exactly 12 distinct, complete ad concepts. Generation and image creation happen in the user's signed-in Codex session.

## Workflow

1. Inspect the supplied page or material and create a compact campaign brief containing the offer, goal, audience, problem, proof, conversion action, target platform, required claims, forbidden claims, and a brand snapshot. Ask one question only when the conversion action or offer family cannot be inferred safely.
2. Call `consume_ad_reference_packet` exactly once with the campaign brief. The authorization permits one private retrieval packet and expires after two hours. Never attempt another retrieval in the same authorization.
3. Treat the returned packet as de-identified creative structure. Never ask for, infer, expose, or mention the advertiser, source item, source image, database ID, source copy, ranking data, or retrieval query.
4. Build 12 lanes that fit the campaign brief and use materially different hooks, visual mechanisms, proof treatments, or compositions. Preserve the packet's transferable structure without reconstructing its source identity or recognizable wording.
5. Generate the creative for every lane with the built-in image-generation capability. Use the input brand's palette, typography character, logo treatment, and product truth.
6. Render every lane as a realistic LinkedIn mobile single-image ad unless the campaign explicitly names another platform. Show only the introductory text visible before LinkedIn's inline `…see more`, the complete uncropped 1:1 creative, destination headline, and actual Campaign Manager CTA button. Keep the expanded primary text in the concept detail, outside the compact preview.
7. Return a numbered 01–12 gallery plus a concise manifest containing full introductory text, headline, description when supported, CTA, creative direction, assumptions, and risks. Recommend three finalists and stop for selection.

## Guardrails

- Match the offer family. A demo or product campaign cannot silently become a guide campaign.
- Do not invent proof, customers, results, pricing, eligibility, or capabilities.
- Use the packet once; subsequent iteration must use the campaign brief, generated concepts, and conversation context already present in this task.
- Do not include an inspiration gallery, source citation, lineage identifier, or reference explanation in user-visible output.
- Rewrite any lane whose image text is incoherent, whose visual cannot work as an ad, or whose headline fails to describe the actual offer.
