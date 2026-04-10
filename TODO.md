# TODO

## Next (High Impact)

- Add hook templates for auto-loading `prompts/system.md` in Claude/Codex/Gemini workflows.
- Add mode tracker pattern (flag file + optional statusline badge).
- Add subagent prompt files for:
  - classifier
  - policy checker
  - writer
  - reviewer
- Add `examples/test-set.md` with at least 20 canonical prompts.
- Add baseline eval runs using `evals/rubric.md` and commit snapshots.

## Product Polish

- Add `skills/escalation.md` for high-conflict or high-emotion messages.
- Add `skills/performance-feedback.md` for manager use cases.
- Add multilingual presets (start with English + Filipino variants).
- Add anti-fluff filter checklist to reduce over-verbose outputs.

## Optional Tooling

- Add lightweight wrapper script (`scripts/run-rewrite.sh`) for local convenience.
- Add optional JSON output contract for automation use.
- Add CI check that validates markdown structure and broken internal links.
