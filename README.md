# Flow

**Design the workflow. Run the work. Keep what helps.**

Flow is an AI skill that first works out how to approach a task, then follows that process through execution, verification, and useful learning.

A campaign might need audience research, inspiration, copywriting, and visual direction. A video might need a storyboard, generated takes, selection, editing, and playback checks. A business case might need evidence, alternatives, criteria, and costings. Flow chooses the stages the task needs.

## Three acts

| Act | What happens |
| --- | --- |
| **Design the flow** | Frame the goal, find relevant existing skills, research expert methods, check available tools, and propose a task-specific sequence. |
| **Run the flow** | Research the task, share a concrete plan, produce the deliverables, inspect the actual results, and repair failures. |
| **Keep the flow** | Identify useful learning, improve a fitting skill or save a reusable task flow, and verify that it was actually saved. |

Each meaningful step has a purpose, an output, and a **done when** condition. The flow describes the method; the plan describes what to make for this particular brief.

## Try it

> Use Flow to turn this product brief into a launch campaign. Show me the flow first.

> Use Flow to analyze these records and recommend a release decision. Just run it. Don't save any learnings.

> Use Flow to create a 30-second video ad. Check production capabilities first, then plan the shots, produce the video, and verify playback.

> Use Flow to build this business case. Let me review the flow and then the researched plan.

## Control the pace

| Request | Intended behavior |
| --- | --- |
| `Use Flow…` | Share the flow and plan, then continue authorized work. |
| `Show me the flow first` | Stop after the proposed workflow, before production. |
| `Review both` | Pause after the flow and again after the researched plan. |
| `Just run it` | Make routine choices and continue, retaining necessary decisions and permission boundaries. |
| `Don't save` | Make no persistent learning writes. |

These instructions do not override the host's permissions or the user's current scope.

## Install

The skill is the complete [`skills/flow`](skills/flow) folder. Keep its reference files alongside `SKILL.md`.

- **Codex:** ask the skill installer to install `skills/flow` from this repository. See OpenAI's [current skill documentation](https://learn.chatgpt.com/docs/build-skills) for local installation and plugin distribution.
- **Claude:** compress the `flow` folder into a ZIP, then upload it using the custom skill controls described in Anthropic's [current instructions](https://support.claude.com/en/articles/12512180-use-skills-in-claude). Compress the skill folder, not the entire repository.
- **Other hosts:** use the host's supported skill-loading mechanism. The core instructions use ordinary Markdown and discover available capabilities at runtime.

After installation, ask **“Use Flow to…”**. Hosts that support explicit skill invocation may also offer `$flow` or `/flow`.

Flow does not install integrations or grant access. Generation, browsing, artifact creation, memory, and durable skill writes depend on the host's available tools. When a required capability is missing, the instructions call for useful preparation and an explicit blocked state.

## What gets retained

Flow distinguishes reusable methods from personal context:

- A useful sequence or check improves a matching flow, or becomes a new `flow-<task-type>` skill when justified.
- A specialist correction belongs in that specialist skill.
- An explicit durable preference or verified project fact belongs in an authorized context store.
- A simulation, untested idea, or temporary state stays labeled as such.

Saved flows include scope, inputs, steps, checks, dependencies, and validation status. They perform their jobs directly rather than recursively invoking Flow. Nothing is claimed as remembered or saved without a successful write.

## Contents

- [`skills/flow/SKILL.md`](skills/flow/SKILL.md): the operating instructions.
- [`design-flow.md`](skills/flow/references/design-flow.md): optional stages and verification by medium.
- [`retain-learning.md`](skills/flow/references/retain-learning.md): evidence, scope, and persistence rules.
- [`saved-flow-template.md`](skills/flow/references/saved-flow-template.md): a template for reusable task flows.
- [`evals/`](evals): fictional trial prompts and observed results.

## Validation

The combined version passed structural validation and three isolated task trials on 20 October 2026: a campaign planning gate, a conflicting-record analysis, and a missing video-generation capability. See [the trial record](evals/results.md) for scope and limits.

These trials check specific behaviors. They are not a benchmark of output quality, proof of improvement over either source version, or evidence of identical behavior across models. Claude installation and cross-host execution have not been tested for this combined version.

## Background

This version combines two iterations of the same Flow idea developed with Claude and Codex. It retains the three-act structure and task-specific modules, while adding explicit capability checks, output verification, configurable review gates, and evidence-based persistence. Personal names, project-specific preferences, and assumed platform-only tool names have been removed.
