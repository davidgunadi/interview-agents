---
name: review-fireflies
description: >
  Reviews a Fireflies recording for a candidate and fills in their questions.md.
  Use this skill whenever the user runs `/review-fireflies [role-name] [candidate-name] [recording-name]`,
  or asks to review a Fireflies transcript, fill in interview answers, or populate questions.md
  from a recording. The user must have the Fireflies connector authorized in Claude.
---

# Review Fireflies Transcript

## Overview

This skill pulls a Fireflies transcript by recording name (or date/title) and fills in
the candidate's `questions.md` with answers and assessments.

The user must have the Fireflies connector authorized. If it is not available, stop and
tell the user to connect it via their claude.ai connector settings before proceeding.

---

## Step 1: Identify the candidate

- Extract role name, candidate name, and recording name from the skill arguments
- If any are missing, ask the user to provide them before continuing
- Confirm the target file: `roles/[role-name]/[candidate-name]/questions.md`
- Stop if `questions.md` does not exist — tell the user to run `/generate-questions` first

---

## Step 2: Pull the Fireflies transcript

- Use the Fireflies connector to search for the recording matching the provided name/date/title
- If multiple matches are found, list them and ask the user to confirm which one
- Retrieve the full transcript

---

## Step 3: Fill in questions.md

Read `.claude/agents/fireflies-reviewer.md` — it contains your persona, scoring criteria,
and instructions for how to assess and fill in answers.

- Read `roles/[role-name]/[candidate-name]/questions.md`
- Follow `.claude/agents/fireflies-reviewer.md` to populate every blank field
- Save the updated file in place

---

## Finishing up

Confirm to the user that `questions.md` has been filled in, and suggest running
`/create-summary [role-name] [candidate-name]` as the next step.
