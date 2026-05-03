# khev-tools

Khevin's personal Claude Code marketplace — a growing toolbox of design and product plugins.

## Plugins

### `design-expert` (v1.2.0)

A paragraph-first, evidence-grounded skill for interface design. Build, review, plan, and write UI with the discipline of NNg heuristics, Universal Design, IBM Carbon, anti-AI-slop patterns, a 32-pattern layout catalog, register-aware style files (editorial / expressive), voice taxonomies (UX copy / long-form / marketing-by-ad-lord), end-of-work self-review, and a curated 17-designer pantheon.

Source: `./plugins/design-expert` &middot; Plugin homepage: <https://github.com/Khevin/design-expert>

## Install

```
/plugin marketplace add https://github.com/Khevin/khev-tools
/plugin install design-expert@khev-tools
```

Use the full HTTPS URL for `marketplace add` — the `owner/repo` shorthand resolves to SSH and fails for users without GitHub SSH keys configured.

If you'd rather click than type, run `/plugin` by itself for an interactive Discover & Install panel.

Once installed, design-expert provides these slash commands:

- `/design-expert:plan` — gate-driven discovery, writes `PRODUCT.md` + `DESIGN.md`
- `/design-expert:build` — builds new UI from those briefs against the canonical library
- `/design-expert:write` — UX copy with WHAT/WHY/HOW errors and acknowledge/explain/act empty states
- `/design-expert:review` — scores an existing surface against the 10-lens framework + UD7 + heuristic stack

## Layout

```
khev-tools/
├── .claude-plugin/
│   └── marketplace.json     # marketplace metadata + plugin list
├── plugins/
│   └── design-expert/       # the plugin itself (own repo at Khevin/design-expert)
│       ├── .claude-plugin/
│       │   └── plugin.json
│       ├── .claude/
│       │   ├── commands/    # slash commands → /design-expert:<name>
│       │   └── skills/
│       │       └── design-expert/
│       │           ├── SKILL.md
│       │           ├── foundations.md · craft.md · anti-slop.md · …
│       │           ├── grids.md · layouts.md · self-review.md
│       │           ├── design-gods/        # 17 designers
│       │           ├── references/         # 8 references + NNg index
│       │           ├── styles/             # editorial · expressive
│       │           ├── voices/             # ux-copy · long-form · marketing/
│       │           └── library/            # do/don't research per surface
│       ├── README.md
│       └── LICENSE
└── README.md
```

## License

MIT.
