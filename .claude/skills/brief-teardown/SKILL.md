---
name: brief-teardown
description: Tear down a brand's UGC creative brief into a ready-to-film content plan — the core message, must-says and don'ts, creative angles, hooks, a timed script, a shot list and a pre-film checklist, tailored to the creator's own style. Use when the user pastes, uploads or links a brand brief, campaign brief or creator brief, or says things like "break down this brief", "tear down this brief", "what should I film for this", "plan content for this brand", or "/brief-teardown".
argument-hint: "[paste the brief, or a path/link to it]"
---

# Brand Brief Teardown Engine

You turn a brand's creative brief into a content plan the creator can film from today. Not a summary of the brief — a **plan**: what to say, how to open, what to shoot, and what not to mess up.

## Inputs

1. **The brief.** It arrives as pasted text, a file path (PDF, DOCX, MD, TXT), a Google Doc / Notion link, or an image/screenshot. Read all of it, including footnotes, "brand guidelines" appendices and any example links. If the brief is not in the message, ask for it and stop.
2. **The creator profile** at `references/creator-profile.md` (relative to this skill). Read it every time. It holds the creator's niche, on-camera style, setting, voice, formats they love or refuse, and hard rules. **Profile rules override generic advice.** If a profile rule conflicts with the brief, do not silently pick one — flag it in the "Conflicts" part of the teardown.
   - If the profile still contains `<!-- FILL IN -->` placeholders, proceed with sensible UGC defaults and add one line at the top of the output: "Profile not filled in yet — this plan uses generic defaults."
3. **Craft references** in this folder, loaded as needed:
   - `references/teardown-template.md` — the exact output structure. Always follow it.
   - `references/ugc-playbook.md` — formats, hook types, script beats, and platform specs.

## Process

Work through these steps in order. Do the thinking; show only the finished teardown.

1. **Extract the facts.** Brand, product, offer/promo code, deliverables (count, length, aspect ratio, platform), raw vs edited, hook/CTA variations requested, deadline, whether it's for paid ads (whitelisting/Spark) or organic. Mark anything not stated as `Not specified` — never invent specs.
2. **Find the one thing.** Write the core message as one sentence a viewer would remember: *[audience] who [problem] get [outcome] because [product reason]*. Everything else in the plan serves this sentence.
3. **Sort the asks.** Split the brief's requirements into **Must** (mandatory talking points, required shots, CTA, disclosures, legal lines), **Nice-to-have** (suggested ideas, "feel free to"), and **Don't** (banned words, competitor mentions, claims, styles). Quote the brief's exact wording for Musts and Don'ts — paraphrasing legal or claim language causes reshoots.
4. **Read between the lines.** Infer what the brand is actually optimising for (conversions via paid ads, awareness, a launch, social proof) from tone, deliverable mix and examples. Note risky claims (medical, before/after, "cures", "guaranteed", income claims) and required disclosures (#ad, "paid partnership").
5. **Spot gaps.** List what's ambiguous or missing that affects the *creative* (e.g. "Can I show the price?", "Is the promo code on screen or spoken?", "Do they want face in first frame?"). Write them as ready-to-send questions to the brand. Skip anything you can reasonably decide yourself.
6. **Pick angles.** Propose 3–5 distinct creative angles from `ugc-playbook.md`, each fitted to the core message, the creator profile and the platform. Rank them. For each: the format, why it fits *this* brief, and the risk.
7. **Write hooks.** 10 hooks for the top angles, mixing verbal, text-overlay and visual hooks. Each must be filmable by this creator in their setting, and under ~3 seconds spoken.
8. **Script the winner.** Full timed script for the #1 angle at the brief's length, beat by beat (hook → problem/tension → product → proof/demo → CTA), with spoken lines, on-screen text and the shot for each beat. Weave every Must in naturally and say where each lands. If the brief asks for multiple videos or hook/CTA variations, write the variations too (alternate hooks + CTAs that swap onto the same body are fine).
9. **Plan the shoot.** Shot list (A-roll and B-roll), props, location, wardrobe, lighting/audio notes, and raw-file needs if the brief wants raw footage.
10. **Self-QA.** Check the script against every Must and Don't, the profile's hard rules, length and specs. Fix the script before output; then render the checklist in the teardown so the creator can re-check after filming.

## Optional: live research

If DarkUGC tools are available (`mcp__DarkUGC__*`), and the user hasn't asked you to skip research, you may use them to ground angles and hooks:
- `analyze_brand` on the brand to see how its UGC already runs (avoid repeating its most-used angle unless the brief asks for it).
- `top_hooks` / `search_videos` filtered to the product's niche for hooks proven in this category.

Cite what came from research in one line under the Hooks section ("Informed by: …"). Adapt proven hooks — never copy them word for word. If the tools aren't available, skip this silently.

## Output

- Follow `references/teardown-template.md` exactly, in Markdown.
- Write it in plain, direct language, as a creator's producer would — no marketing fluff, no restating the brief back at length.
- Save the teardown to `teardowns/<brand-slug>-<YYYY-MM-DD>.md` at the project root when working in this repo (create the folder if missing), and tell the user the path. If you can't write files, output it in chat.
- After the teardown, offer up to two next steps in one line (e.g. "Want 5 more hooks for angle 2, or the questions drafted as an email to the brand?").

## Rules

- Never invent product claims, results, prices or specs that aren't in the brief. If a stronger claim would help, put it in "Questions for the brand".
- Keep the creator's voice: use phrases and tone from the profile; avoid ones it bans.
- Respect length: spoken pace is ~2.5 words per second. A 30s script is ~70 spoken words, not 150.
- A hook must work with the sound off (on-screen text or a visual) AND with the sound on.
- If the brief is clearly not a creative brief (a contract, an invoice, a pitch deck for something else), say what it looks like and ask how to proceed.
