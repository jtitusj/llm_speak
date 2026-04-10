# llm_speak

Turn boring workplace replies into polished, intelligent language using the AI coding assistant you already have.

`llm_speak` is a markdown-first prompt kit for Gemini CLI, Codex, Claude Code, and similar tools.  
No extra auth flow. No package install. Just load this repo and use the prompts.

## Why This Direction

You already have model access in your daily toolchain.  
So this project avoids rebuilding auth, SDK wrappers, and CLI plumbing that those tools already solve.

This keeps `llm_speak`:

- lightweight
- easy to share publicly
- fast to adopt for technical users

## Fun + Professional

This is a fun side project that still delivers real work value.

- `fun mode`: clean up awkward text quickly
- `serious mode`: produce audience-aware, high-credibility messaging when stakes are real

## Quick Start

### 1) Clone the repo

```bash
git clone https://github.com/<your-username>/llm_speak.git
cd llm_speak
```

### 2) Load this folder in your AI coding tool

Open the repo as workspace/context in your preferred assistant.

### 3) Use the prompt templates

Start with:

- `prompts/system.md`
- `prompts/rewrite.md`
- `prompts/presets.md`
- `skills/README.md` (task-specific overlays)

Then paste your raw message and specify tone + audience.

## File Layout

```text
.
├── README.md
├── TODO.md
├── docs
│   └── advanced-orchestration.md
├── evals
│   └── rubric.md
├── examples
│   └── before-after.md
├── prompts
│   ├── presets.md
│   ├── rewrite.md
│   └── system.md
└── skills
    ├── README.md
    ├── admit-fault.md
    ├── client-safe.md
    ├── deadline-shift.md
    ├── pushback.md
    └── status-update.md
```

## Example Workflow

Input:

```text
yeah youre right i messed this up
```

Prompt instruction:

```text
Use the "diplomatic" preset. Audience: manager. Goal: admit fault professionally.
```

Output:

```text
You’re right, and I appreciate the clarification. I missed that detail on my first pass, and I’ll correct it now.
```

## Mode Triggers

You can invoke behavior with natural commands:

- `llm_speak mode`
- `rewrite this professionally`
- `make this sound smarter`

Stop and return to normal behavior with:

- `stop llm_speak`
- `normal mode`
- `raw output`

Default mode is `balanced` if none is specified.

## Sub-Skills

For focused use cases, layer one skill file with your system prompt:

- `skills/admit-fault.md`
- `skills/pushback.md`
- `skills/deadline-shift.md`
- `skills/status-update.md`
- `skills/client-safe.md`

This gives consistent structure for the most common workplace messages.

## Customization

Edit the markdown prompts directly:

- add/remove tone presets in `prompts/presets.md`
- tighten rewrite rules in `prompts/system.md`
- add your company voice notes in `prompts/rewrite.md`

Because everything is plain markdown, teams can version-control prompt behavior in Git.

## Advanced Usage (Optional)

If your users already run tool-native workflows (subagents/hooks), use:

- `docs/advanced-orchestration.md`

It shows how to layer:

- intent classification
- policy checks
- multi-variant generation
- final review hooks

on top of the same prompt files, without forcing complexity on casual users.

## Examples and Evaluation

- Before/after examples: `examples/before-after.md`
- Scoring rubric: `evals/rubric.md`

Use these to compare rewrites and avoid style drift as the prompt kit evolves.

## Suggested Use Cases

- Admit fault without sounding weak
- Push back without sounding defensive
- Ask for deadline shifts with clear accountability
- Rewrite terse messages into collaborative language
- Convert emotional drafts into calm, executive-ready replies

## Roadmap

See `TODO.md` for prioritized next steps.

## Contributing

PRs are welcome, especially:

- new presets that are actually useful at work
- better constraints to reduce fluff and buzzwords
- stronger before/after examples

## License

MIT
