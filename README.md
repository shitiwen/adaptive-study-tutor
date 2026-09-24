# Adaptive Study Tutor

An adaptive university-tutoring skill that combines lesson preparation, diagnosis-first teaching, and strict mastery verification into one natural-language workflow.

## What it does

The skill routes each request to the most useful internal mode:

- **PREP** — turns course pages, teacher slides, or a syllabus into a teaching map, examples, checks, and (when useful) a verified slide deck.
- **TEACH** — starts from the learner's current understanding, finds the first missing step, and teaches interactively instead of dumping a solution.
- **MASTERY** — uses first-principles reasoning, Feynman explain-back, Socratic probes, deliberate practice, and novel-transfer checks before calling a concept confirmed.

It does not require the learner to select a mode. Requests such as “提前备课”, “开始上课”, and “严格检查我是否真正掌握” are routed automatically. Teaching is divided by coherent knowledge units and natural stopping points, not an artificial fixed number of minutes.

## Continuity between chats

The skill treats a long-term subject branch as the course ledger and a temporary lesson chat as the classroom workspace. At the end of a chapter, major unit, or temporary lesson chat it can produce a detailed state card containing:

- course and textbook position;
- confirmed, unchecked, weak, and blocked knowledge;
- exact mistakes and the evidence behind the diagnosis;
- examples already used, so the next lesson does not repeat them mechanically;
- the next opening recall check, main content, buffer content, and material to defer.

See [`references/continuity.md`](references/continuity.md) for the full handoff schema.

## Install

Install the skill from this repository with the Skills CLI:

```bash
npx skills add shitiwen/adaptive-study-tutor --skill adaptive-study-tutor --global
```

For a Codex-specific install, use:

```bash
npx skills add shitiwen/adaptive-study-tutor --skill adaptive-study-tutor --global --agent codex
```

Or download the source directly:

```bash
git clone https://github.com/shitiwen/adaptive-study-tutor.git
```

Then place the skill directory where your AI tool loads skills, keeping `SKILL.md`, `agents/`, `references/`, and `assets/` together.

## Typical prompts

```text
明天讲高数第 X 节，请根据教材和老师的范围提前备课，做一份教学地图和必要的 PPT。

开始上课。先用一道回忆题检查上节课的前置知识。

我觉得自己会了，请从第一性原理严格检查，并给我一道没见过的迁移题。
```

## Design lineage

This is an independent Work-compatible adaptation inspired by the public teaching ideas of:

- [Personal Tutor](https://github.com/briannajzhang/personal-tutor)
- [Universal Diagnostic Tutor](https://github.com/SenmuuuuW/universal-diagnostic-tutor-skill)
- [SuperTutor](https://github.com/cskwork/supertutor-skill)

It does not copy their environment-specific local servers, fixed paths, or mandatory runtime gates. The merged behavior is documented in [`SKILL.md`](SKILL.md) and the route references.

## License

MIT. See [`LICENSE`](LICENSE).
