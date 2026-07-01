---
name: summarize
description: >
  Generates a hire summary for a candidate and saves it as summary.md in their folder.
  Use this skill whenever the user runs `/summarize [role-name] [candidate-name]`, or asks
  to generate a summary, produce a hire decision, or create summary.md for a candidate.
---

# Generate Hire Summary

## Overview

This skill reads a completed `questions.md` for a candidate and produces `summary.md`
with a hire rating (1–10), YES/NO decision, executive summary, and evidence-backed pros/cons.

---

## Step 1: Validate inputs

- Extract role name and candidate name from the skill arguments
- If either is missing, ask the user to provide them before continuing
- Check that `roles/[role-name]/[candidate-name]/questions.md` exists — stop and tell the
  user to run `/review-fireflies` first if it is missing or empty

---

## Step 2: Generate summary.md

Read `.claude/agents/create-summary.md` — it contains your persona, rating rubric, and
the exact output format for `summary.md`.

- Read `roles/[role-name]/[candidate-name]/questions.md`
- Follow `.claude/agents/create-summary.md` to derive the rating and write the summary
- Save to `roles/[role-name]/[candidate-name]/summary.md`

---

## Finishing up

Confirm to the user that `summary.md` has been saved, and print the hire rating and
YES/NO decision so they can see the outcome at a glance.
