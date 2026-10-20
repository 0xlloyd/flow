# Saved flow template

Use this structure selectively. Remove empty sections. Replace placeholders with the generalized procedure that actually ran. Keep scope and triggers in the description so the host can discover the skill.

```markdown
---
name: flow-<task-type>
description: "<Recurring job and when to use this flow; useful boundaries and expected output.>"
---

# Flow: <task type>

## Inputs and scope

- Required: <inputs or constraints that materially affect correctness>.
- Optional: <preferences that can use stated defaults>.
- Does not cover: <relevant boundary, if needed>.

## Procedure

1. **<Step>** — Why: <purpose>. Input: <dependency>. Output: <concrete result>. Skill/tool: <discoverable capability, if needed>. Done when: <observable criterion>.
2. **<Step>** — <same fields, only where helpful>.

Mark [REVIEW] only for a requested user checkpoint; mark [DECISION] for a consequential unresolved choice. Preserve the user's current authorization and platform rules. State when branches or optional stages apply.

## Verification and recovery

- <Actual output checks appropriate to this task.>
- <Failure → targeted correction → recheck.>
- <Stop condition or explicit blocked-state handling.>

## Dependencies and alternatives

- <Required or optional skills/capabilities; current discovery instructions.>
- <Fallback and what changes if a capability is missing.>

## Validation status

- Status: <draft / simulated use / real-task use>.
- Evidence: <date and non-private description of the check or outcome>.
- Observed runs: <real count and simulated count, only when known>.
- Not yet verified: <material limits>.

## Lessons incorporated

- <Date>: <specific procedure change and supporting observation>.

## References

- <Attributable sources needed for reuse, with dates/freshness limits.>
```

The saved skill performs its task directly. Do not write “run through Flow's three acts” as a dependency. Keep the updated procedure authoritative; a lessons log alone is not an implementation of the correction.
