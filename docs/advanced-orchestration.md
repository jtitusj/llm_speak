# Advanced Orchestration: Subagents and Hooks

This repo works out of the box as plain markdown prompts.  
For advanced users (Gemini CLI/Codex/Claude Code), subagents and hooks can add guardrails and speed.

## Why Use Subagents

Split one rewrite request into specialized passes:

1. intent classifier
2. risk/policy checker
3. rewrite generator
4. final style reviewer

This reduces bad rewrites (too soft, too aggressive, too verbose) and improves consistency.

## Recommended Subagent Roles

### `classifier`

- Detect intent: admit fault, push back, request extension, escalate risk, etc.
- Infer audience sensitivity: manager, peer, client, leadership

### `policy`

- Block deceptive or manipulative framing
- Flag legal/HR-sensitive language
- Enforce “no fabricated commitments”

### `writer`

- Generate `safe`, `balanced`, `bold` options
- Keep meaning intact

### `reviewer`

- Check tone fit against preset
- Remove fluff/buzzwords
- Ensure final message is actionable

## Hook Ideas

### pre-rewrite hook

Input checks before generation:

- message length sanity
- profanity/hostility scan
- sensitive-topic tagging

### post-rewrite hook

Quality checks after generation:

- no invented facts
- no policy violations
- no accidental tone drift
- max length threshold

## Example Pipeline

```text
raw_message
  -> classifier
  -> policy
  -> writer (3 variants)
  -> reviewer (select/merge)
  -> final_output
```

## Minimal Integration Pattern

Even without custom code, you can simulate orchestration by running sequential prompts:

1. run classification prompt
2. run policy prompt
3. run rewrite prompt
4. run final QA prompt

Store each step in versioned markdown files for repeatable team behavior.

## Practical Guidance

- Keep default flow simple for casual use.
- Gate advanced orchestration behind an “advanced mode” section.
- Prefer deterministic checklists over clever prompts.
- Add small regression examples to detect tone regressions over time.
