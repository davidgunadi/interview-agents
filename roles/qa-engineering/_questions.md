# Interview Template: QA Engineer

---

## 1. Technical Interview

### 1.1 Technical Rubric

Score each dimension 1–5 after the interview. Pull evidence from answers.

| Dimension | Weight | Score (1–5) | Evidence / Notes |
|-----------|--------|-------------|------------------|
| Test Case Design & Analysis (functional, integration, regression) | High | | |
| Manual Testing Across Web/Mobile/API/Backend | High | | |
| Defect Management & Root Cause Analysis | High | | |
| Release Validation (smoke/sanity, acceptance criteria) | High | | |
| Cross-functional Collaboration (Dev/PM/Tech Lead) | Med | | |
| Automation Testing | Med | | |

**Scoring guide:** 1 = no signal / wrong answers, 2 = weak, 3 = adequate, 4 = strong, 5 = exceptional

**Weighted average:** ___

---

### 1.2 Core Technical Questions

Standard questions for this role, not tailored to any specific candidate.

### Q1: Walk me through how you'd turn a user story or requirement doc into a set of test scenarios and test cases. How do you decide what's functional vs. integration vs. regression coverage?

**What a good answer looks like:**
- Describes a structured process from requirement/acceptance criteria to test design
- Distinguishes functional, integration, and regression scope with concrete examples
- Mentions edge cases and negative testing, not just the happy path

**Red flags:**
- Only describes happy-path testing
- Can't explain the difference between test types
- No mention of tracing test cases back to acceptance criteria

---

### Q2: Describe your approach to testing an API or backend service manually. What do you check beyond "does it return 200"?

**What a good answer looks like:**
- Covers status codes, payload schema/contract validation, error handling, edge cases, auth
- Mentions tools used (Postman, curl, etc.) and how they structure test data
- Talks about testing failure modes, not just the success path

**Red flags:**
- Vague or surface-level ("I just check if it works")
- No mention of validating response structure or error cases
- Confuses API testing with UI testing

---

### Q3: Tell me about a defect you found that was hard to pin down. How did you isolate the root cause, and how did you document it so a developer could act on it without back-and-forth?

**What a good answer looks like:**
- Describes a systematic isolation process (narrowing environment, data, steps to reproduce)
- Clear, structured defect documentation (repro steps, expected vs. actual, severity, environment)
- Some root cause reasoning, not just symptom reporting

**Red flags:**
- Defect reports described as vague or missing repro steps
- No isolation process — just "I told the developer it was broken"
- Can't explain severity/priority reasoning

---

### Q4: Before a release, how do you decide what needs smoke testing vs. full regression? Tell me about a time a release was at risk and how you handled the validation.

**What a good answer looks like:**
- Clear criteria for scoping smoke/sanity vs. full regression (risk-based, change-based)
- Concrete example of a release under time pressure and how testing was prioritized
- Mentions post-release monitoring/validation, not just pre-release testing

**Red flags:**
- No clear method for scoping — tests everything or tests arbitrarily
- No example of pressure/tradeoff — purely theoretical answer
- No mention of what happens after release (monitoring, rollback awareness)

---

### Q5: How do you handle a disagreement with a developer or PM about whether something is actually a bug, or about its severity?

**What a good answer looks like:**
- Describes using evidence (requirements, acceptance criteria, user impact) to make the case
- Willing to escalate or align with PM/Tech Lead when needed, without being confrontational
- Shows judgment on when to hold the line vs. defer

**Red flags:**
- Always defers without pushing back, even when evidence supports them
- Frames disagreements as purely personal/political rather than evidence-based
- No concrete example, only hypothetical

---

### Q6: What automation testing experience do you have? Walk me through a case where you automated a test — what did you choose to automate, what tooling did you use, and why not automate everything?

**What a good answer looks like:**
- Concrete tooling/framework experience (even if limited) and reasoning for automation candidates (regression-heavy, stable flows)
- Understands ROI tradeoff — not everything should be automated
- Can speak to maintenance cost of automated suites

**Red flags:**
- No hands-on automation experience and no framework knowledge at all
- Cannot articulate why some tests are automated and others aren't
- Confuses "automation" with running a script once

---

## 2. Behavioral Interview

Not a technical assessment — this section probes a role-specific selection of traits drawn from `roles/_behavioral_question_bank.md` (e.g. ownership, diligence, adaptability, collaboration, coachability — the actual set varies by role). Evidence for any trait can surface in response to any question below (or even during the Technical Interview) — the rubric is scored from the totality of the transcript, not one-to-one against the question that "belongs" to it.

### 2.1 Behavioral Rubric

| Trait | Assessed Outcome | Evidence / Notes |
|-------|-------------------|-------------------|
| Ownership | [ ] Green  [ ] Amber  [ ] Red | |
| Integrity | [ ] Green  [ ] Amber  [ ] Red | |
| Learning From Mistakes | [ ] Green  [ ] Amber  [ ] Red | |
| Leading (IC variant) | [ ] Green  [ ] Amber  [ ] Red | |
| Conflict / Difficult Conversations | [ ] Green  [ ] Amber  [ ] Red | |
| Receiving Feedback | [ ] Green  [ ] Amber  [ ] Red | |

**Anchors — copied verbatim from `roles/_behavioral_question_bank.md` for each selected trait, do not redesign:**

**Ownership**
- Green — Uses "I" for failure points, "we" for wins. Proactively expanded scope without being asked. Follows through to resolution, not just identification.
- Amber — Claims some ownership but softens it — acknowledges a failure existed but frames their role ambiguously, or expanded scope once but describes it as an exceptional one-off rather than a pattern.
- Red — Failure is always someone else's fault or "the process." Identifies problems but has no story of actually fixing one outside their lane.

**Integrity**
- Green — Chose transparency even when it was costly (career, relationship, timeline). Specific, not hypothetical.
- Amber — Describes a real ethical or professional tension but the resolution is unclear or was deferred to someone else, or the "cost" of honesty turns out to have been minimal.
- Red — Answer is entirely hypothetical ("I would..." rather than "I did..."). Frames dishonesty-adjacent behavior as clever or resourceful.

**Learning From Mistakes**
- Green — Can state the mistake plainly without over-qualifying it. Describes a concrete behavioral or process change that stuck. Some self-awareness about *why* the mistake happened, not just what happened.
- Amber — Names a real mistake and a change made, but the change is described in general terms ("I'm more careful now") without a concrete mechanism, or self-awareness of the cause is thin.
- Red — "Mistake" is trivially small or not really their fault. No lasting change described — same mistake could recur. Over-rehearsed, generic answer (interview-prep smell).

**Leading**
- Green — Names specific actions taken to influence or lead, not just "I motivated the team." Acknowledges tradeoffs made. Owns the outcome, good or bad, with concrete detail on how they knew it worked.
- Amber — Describes a leadership/influence moment but stays vague on the specific mechanism — general "I aligned the team" language, unclear what action actually shifted the outcome, or credits authority/title rather than persuasion.
- Red — Vague "we" language with no personal action described. Leadership framed purely as authority ("I told them to..."). No mention of how they knew it worked.

**Conflict / Difficult Conversations**
- Green — Addresses the conflict directly rather than avoiding or escalating past it. Reflects on the relationship post-conflict, not just the immediate resolution.
- Amber — Describes a real tense disagreement but the resolution is vague, or reflection stops at "it worked out" without detail on how the relationship was maintained.
- Red — Conflict always resolved by them being "right" and the other person coming around. Avoidance dressed up as diplomacy ("I just let it go").

**Receiving Feedback**
- Green — Distinguishes between initial emotional reaction and eventual response — honest that it stung before it was useful. Can describe feedback they *didn't* fully agree with and how they handled that tension productively (not just capitulation).
- Amber — Describes real feedback and an eventual change, but skips the initial reaction/friction, or the disagreement was resolved by simply deferring rather than genuinely working through it.
- Red — Claims to have never received hard feedback, or that all feedback was immediately and gratefully accepted. No example of pushing back on feedback they thought was wrong.

---

### 2.2 Behavioral Questions (STAR)

All questions must be phrased to elicit a STAR response (Situation → Task → Action → Result).

### B1: Tell me about a project or release where you noticed a quality problem that wasn't technically your responsibility. What did you do?

**Primary trait probed:** Ownership

**What to listen for:**
- Proactively expanded scope beyond assigned test cases
- Followed through until the issue was actually resolved, not just flagged

---

### B2: Have you ever been asked to sign off on a release, or found yourself under pressure to sign off, when you weren't confident the quality bar was met? What did you do?

**Primary trait probed:** Integrity

**What to listen for:**
- Chose transparency about risk even when it created friction with deadlines/stakeholders
- Specific, real instance — not hypothetical

---

### B3: Walk me through a significant bug or gap you missed that made it to production. How did you find out, and what changed in how you test afterward?

**Primary trait probed:** Learning From Mistakes

**What to listen for:**
- States the miss plainly, without deflecting blame
- Concrete change to their test process/checklist that stuck afterward

---

### B4: Tell me about a time you had to convince a developer or PM to prioritize fixing something, without having authority to force the decision.

**Primary trait probed:** Leading (IC variant)

**What to listen for:**
- Specific persuasion tactics (evidence, user impact, risk framing), not just "I explained it"
- Owns the outcome, including if it didn't fully work

---

### B5: Tell me about a disagreement with a developer or PM about whether something was a bug, or how severe it was, that got tense. How did you handle it?

**Primary trait probed:** Conflict / Difficult Conversations

**What to listen for:**
- Addressed the disagreement directly with evidence rather than avoiding it or escalating unnecessarily
- Reflects on how the working relationship held up afterward

---

### B6: Tell me about the most critical piece of feedback you've received on your testing work. What was your first reaction, and what did you do with it?

**Primary trait probed:** Receiving Feedback

**What to listen for:**
- Honest about initial friction/defensiveness before it became useful
- Example of feedback they initially disagreed with and how they worked through that tension

---

## 3. Additional Information

> [This section is left blank in the template. During review, anything the candidate raises that doesn't fit a predefined question in Section 1 or 2 gets logged here, tagged [Technical] or [Behavioral].]

---

## 4. Candidate's Questions for Us

> [This section is left blank in the template. Filled during post-interview review with whatever the candidate actually asked.]

---

## 5. Post-Interview Summary

**Strongest signals:**
>

**Biggest concerns:**
>

**CV vs reality gap (if any):**
>

**Final notes for the hiring manager:**
>
