# Rewrite Task Prompt

Use this with `prompts/system.md` loaded.

## Task

Rewrite the message below to improve professionalism and clarity without changing intent.

## Inputs

- Audience: `<manager|coworker|client|executive|cross-functional>`
- Tone: `<diplomatic|executive|direct|friendly|supportive|high-stakes>`
- Goal: `<what this message needs to achieve>`
- Length: `<shorter|same|slightly longer>`
- Constraints: `<optional, e.g., avoid apology-heavy language>`

## Message

```text
<paste original message here>
```

## Output Format

Return:

1. Final rewrite
2. Optional one-line rationale (only if asked)

If asked for options, return 3 variants:

- `safe`
- `balanced`
- `bold`
