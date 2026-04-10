# llm_speak Sub-Skills

These are task-focused prompt overlays. Use with:

1. `prompts/system.md`
2. One skill file from this folder
3. Your raw message

Available:

- `admit-fault.md`
- `pushback.md`
- `deadline-shift.md`
- `status-update.md`
- `client-safe.md`

Usage example:

```text
Load prompts/system.md + skills/admit-fault.md.
Tone: apology-safe
Audience: manager
Rewrite: "you're right i missed this and caused delay"
```
