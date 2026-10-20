# Trial record

Date: 20 October 2026.

Three isolated agent tasks used the combined skill with fictional, task-local inputs. The agents received the skill location and the task, without the evaluator's expected answer. The public prompts in `cases.json` remove local paths while preserving the task constraints. The environment also had specialist skills available, including a short-video-ad flow; this was not a standalone-skill or cross-host compatibility test.

| Case | Observed result | Assessment |
| --- | --- | --- |
| Campaign review gate | Proposed six coordinated stages covering message, visual direction, drafting, production, verification, and learning. Explicitly paused before copy or assets. | Passed the requested planning boundary. Asset quality was not tested. |
| Analysis, execution, no save | Reported 5 unique tickets, identified the duplicate, conflict and missing status, reconciled counts, and failed the release gate. Reported no learning writes or skill edits. | Correct result for the supplied records. No live release operation was attempted. |
| Cinematic video capability gap | Reported footage generation as unavailable, supplied a timed 30-second storyboard and production handoff, and distinguished planned acceptance checks from a completed video. Reported no generated assets or persistent changes. | Preserved the requested outcome and blocked state. No footage, audio, or export was produced or tested. |

Two trial launches initially failed because the selected model was at capacity. Both completed when retried with the same task. Those infrastructure failures are not counted as completed behavioral runs.

The skill's YAML/frontmatter structure also passed the host's skill validator. Relative reference links were checked in the distribution copy.

These are observed results from three controlled tasks, not a success-rate estimate. They do not validate every module, production-quality marketing, actual learning persistence, or execution in Claude. A future regression run should use a fresh context, supply only the selected task and necessary raw inputs, and evaluate the actual output against the checks without leaking those checks into the task prompt.
