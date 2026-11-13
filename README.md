# Brand Brief Teardown Engine

A Claude skill that turns a brand's UGC creative brief into a content plan you can film from: the core message, the must-says and don'ts quoted from the brief, questions to send the brand, ranked creative angles, 10 hooks, a timed script, a shot list and a pre-film checklist. All of it is tailored to your own on-camera style.

## Use it

In Claude Code, from this repo:

```
/brief-teardown <paste the brief here>
```

You can also give it a file (`/brief-teardown examples/sample-brief-lumen-serum.md`), a PDF, or a Google Docs or Notion link. Each teardown is saved to `teardowns/<brand>-<date>.md`.

To use it in the Claude app (claude.ai), zip the `.claude/skills/brief-teardown/` folder and upload it under **Settings → Capabilities → Skills**.

## Make it yours

Fill in **`.claude/skills/brief-teardown/references/creator-profile.md`** with your niche, voice, setup, the formats you love and avoid, and your hard rules. Every teardown reads it, and its rules override the generic advice.

## What's inside

```
.claude/skills/brief-teardown/
├── SKILL.md                         # the engine: inputs, 10-step process, rules
└── references/
    ├── creator-profile.md           # YOUR rules (fill this in)
    ├── teardown-template.md         # the exact output format
    └── ugc-playbook.md              # angles, hook types, script beats, specs, compliance
examples/
└── sample-brief-lumen-serum.md      # fictional brief to test with
teardowns/                           # finished teardowns land here
```

If the DarkUGC connector is available, the engine can also pull proven hooks and the brand's current UGC patterns to inform the angles. It adapts what it finds and never copies it word for word.
