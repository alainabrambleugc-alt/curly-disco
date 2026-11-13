# Brand Brief Teardown Engine

A Claude skill that tears down a brand's UGC creative brief the way a creative strategist, performance marketer and director would. Everything is framed around two things: what the buyer gets emotionally, and what the brand gets from its ad spend.

What each teardown gives you:

- **Persona ID:** who exactly you're speaking to, their age and life stage, their pain point in their own words, what's stopping them buying, and their awareness stage. A **benefit ladder** climbs from the feature to the life outcome they actually care about.
- **Must / Don't**, plus a **claims check** with two paths: an "Actor portrayal" disclosure approved by the brand, or a spokesperson read.
- **Questions to ask before you quote**, including usage rights.
- **Research:** the brand's and competitors' Meta ads (via Adspo or Motion), viral TikTok and Instagram videos in the niche (via Blueprint), UGC that sells (via DarkUGC), and any screenshots you share.
- **Four concepts**, each with a different persuasion angle, format and psychology trigger. Each has visual, spoken and on-screen hooks, motion in the first 2 seconds, a re-hook, retention grabs, a CTA, and a wide, standard and macro shot list.
- **A timed script** with movement every 5–7 seconds, plus notes on how the product moves and where to frame it so it stays clear of the text overlay and captions.
- **3 extra hooks and 2 extra CTAs** with every brief.
- **A shoot plan and a pre-film checklist.**
- **An itemized quote** from your 2026 rate card (standard tier, low end of each range).
- **Client replies:** a pushback message grounded in strategy, and an offer with packages plus an add-on menu (funnel and awareness versions, different lengths, bigger test batches, a strategy review, a retainer).

Before each teardown it asks you three quick questions: where the brief came from, whether you're running any specials, and whether you already own the product.

You can also ask for a single piece ("just the pushback", "3 more hooks", "quote this brief") or for brand outreach ("write a pitch to [brand]", "follow up with [brand]", "check in after delivery").

## Use it

In Claude Code, from this repo:

```
/brief-teardown <paste the brief here>
```

You can also give it a file (`/brief-teardown examples/sample-brief-lumen-serum.md`), a PDF, or a Google Docs or Notion link. Each teardown is saved to `teardowns/<brand>-<date>.md`.

To use it in the Claude app (claude.ai), zip the `.claude/skills/brief-teardown/` folder and upload it under **Settings → Capabilities → Skills**. Connect Adspo, Blueprint and DarkUGC there to turn on the research step.

## Make it yours

Fill in **`.claude/skills/brief-teardown/references/creator-profile.md`** with your niche, voice, setup, the formats you love and avoid, and your hard rules. Every teardown reads it, and its rules override the generic advice. Prices live in `rate-card.md`.

## What's inside

```
CLAUDE.md                            # value-first writing rules for everything in this repo
.claude/skills/brief-teardown/
├── SKILL.md                         # the engine: creator check, 13-step process, research, rules
└── references/
    ├── creator-profile.md           # YOUR style and rules (fill this in)
    ├── rate-card.md                 # your 2026 rates + quote rules
    ├── teardown-template.md         # the exact output format
    └── ugc-playbook.md              # persona, psychology, retention, directing, framing, funnel, upsells, outreach
examples/
└── sample-brief-lumen-serum.md      # fictional brief to test with
teardowns/                           # finished teardowns land here
```

TikTok Creative Center has no connector. The engine uses web access where it's available, and otherwise asks you for screenshots.
