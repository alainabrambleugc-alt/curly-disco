# Brand Brief Teardown Engine

A Claude skill that tears down a brand's UGC creative brief in Alaina's own system (Mama WildRoot Creative): her storytelling guide, creator profile and Nov 2026 research notes, plus brand strategy, directing and pricing. Everything is framed around two things: what the buyer feels, and what the brand gets from its ad spend.

What each teardown gives you:

- **Brief flags** against your hard nos and real-life constraints (rain windows, wifi, turnaround).
- **Persona:** your four persona questions, the brain stack (40s always on) and driving need, awareness stage, and a **benefit ladder** from feature to feeling.
- **Must / Don't**, plus a **claims check** with two paths: the brand's own claims delivered with an on-screen "Actor portrayal" disclosure they approve in writing, or a spokesperson read / true rewrite / [NEED] gap.
- **Questions to ask before you quote**, including usage rights.
- **Research:** the brand's and competitors' Meta ads (via Adspo or Motion), viral TikTok and Instagram videos in the niche (via Blueprint), UGC that sells (via DarkUGC), and any screenshots you share.
- **Four concepts**, each with a different door (Feeling, Fix, Joke, Close), angle and format. Each has a triple hook from your seven hooks, a frame-1 plan, shoulder tap, re-hook, objection kill, CTA, a wide / standard / macro shot list, and a two-ledger read.
- **A teleprompter-ready script** on your spine, cut on new information, with product-motion and safe-zone notes, then your storytelling, Fogg and views passes.
- **3 extra hooks and 2 CTA alternatives** with every brief.
- **A storyboard for brand approval, a shoot plan** built from your real spaces, props and gear, **and a pre-film checklist.**
- **An itemized quote** from your 2026 rate card. It picks the tier (Standard film-only when the brand supplies the lines, Content + Strategy when you write and research) and applies bundle discounts: 10% off 3–4 of an item, 15% off 5, 20% off 6 or more.
- **Client replies:** a pushback message grounded in strategy, and an offer with packages plus an add-on menu (funnel and awareness versions, different lengths, bigger test batches, a strategy review, a retainer).

Before each teardown it asks you four quick questions: where the brief came from, which account it's for, whether you're running any specials, and whether you already own the product.

You can also ask for a single piece ("just the pushback", "3 more hooks", "quote this brief") or for brand outreach ("write a pitch to [brand]", "follow up with [brand]", "check in after delivery").

## Use it

In Claude Code, from this repo:

```
/brief-teardown <paste the brief here>
```

You can also give it a file (`/brief-teardown examples/sample-brief-lumen-serum.md`), a PDF, or a Google Docs or Notion link. Each teardown is saved to `teardowns/<brand>-<date>.md`.

To use it in the Claude app (claude.ai), zip the `.claude/skills/brief-teardown/` folder and upload it under **Settings → Capabilities → Skills**. Connect Adspo, Blueprint and DarkUGC there to turn on the research step.

## Make it yours

Your system lives in `.claude/skills/brief-teardown/references/`. The order of authority is: `storytelling-guide.md` (wins over everything), then `creator-profile.md`, then `research-notes.md`, then the playbook. When you update your guide or profile, replace those files and every teardown follows. Prices live in `rate-card.md`.

## What's inside

```
CLAUDE.md                            # writing rules for everything in this repo
.claude/skills/brief-teardown/
├── SKILL.md                         # the engine: creator check, 15-step process, research, rules
└── references/
    ├── storytelling-guide.md        # YOUR system: spine, hooks, brains x doors, rules (wins)
    ├── creator-profile.md           # who you are, hard nos, spaces, props, gear
    ├── research-notes.md            # Nov 2026 research: what sells, what's debunked
    ├── rate-card.md                 # your 2026 rates + quote rules
    ├── ugc-playbook.md              # brand strategy, funnel, angles, shots, framing, upsells, outreach
    └── teardown-template.md         # the exact output format
examples/
└── sample-brief-lumen-serum.md      # fictional brief to test with
teardowns/                           # finished teardowns land here
```

TikTok Creative Center has no connector. The engine uses web access where it's available, and otherwise asks you for screenshots.
