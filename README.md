# Brand Brief Teardown Engine

A Claude skill that tears down a brand's UGC creative brief the way a creative strategist would:

- **Customer read:** who the customer is, the problem, what stops them buying, and their awareness stage
- **Must / Don't**, plus a **claims check** that flags any line asking you to claim an experience you haven't had and offers a spokesperson read instead
- **Questions to ask before you quote**, including usage rights
- **Ad library read** (from screenshots you share): repeated hooks and formats, likely winners, and the angle nobody is testing
- **Four new concepts**, each with a different persuasion angle and format, plus a hook, the first two seconds, and why it could beat the brand's ask
- **A timed script, shot list and pre-film checklist**
- **An itemized quote** built from your 2026 rate card (standard tier, low end of each range)
- **Client replies:** a pushback message and a two-option offer that opens the door to a retainer

All of it is tailored to your own style and rates.

You can also ask for a single piece, such as "just the pushback reply", "ad library check on these screenshots" or "write my offer".

## Use it

In Claude Code, from this repo:

```
/brief-teardown <paste the brief here>
```

You can also give it a file (`/brief-teardown examples/sample-brief-lumen-serum.md`), a PDF, or a Google Docs or Notion link. Each teardown is saved to `teardowns/<brand>-<date>.md`.

To use it in the Claude app (claude.ai), zip the `.claude/skills/brief-teardown/` folder and upload it under **Settings → Capabilities → Skills**.

## Make it yours

Fill in **`.claude/skills/brief-teardown/references/creator-profile.md`** with your niche, voice, setup, the formats you love and avoid, and your hard rules. Prices live in `rate-card.md`. Every teardown reads it, and its rules override the generic advice.

## What's inside

```
.claude/skills/brief-teardown/
├── SKILL.md                         # the engine: inputs, 10-step process, rules
└── references/
    ├── creator-profile.md           # YOUR rules (fill this in)
    ├── rate-card.md                 # your 2026 rates + quote rules
    ├── teardown-template.md         # the exact output format
    └── ugc-playbook.md              # angles, hook types, script beats, specs, compliance
examples/
└── sample-brief-lumen-serum.md      # fictional brief to test with
teardowns/                           # finished teardowns land here
```

If the Adspo (Meta Ad Library) or DarkUGC connectors are available, the engine can pull the brand's live ads and proven hooks in the niche itself. It adapts what it finds and never copies it word for word.
