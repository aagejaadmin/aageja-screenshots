## Activities

**Alias:** Question1
**Format:** Multiple choice — single answer
**Stem:** Meridian Financial has completed UAT. All Critical and High issues are resolved. Every critical workflow has been validated across all seven UAT testing categories. The VP of Learning is refusing to sign off because Leaderboard will not be available after migration. Based on the sign-off criteria, which of the following is correct?
**Options:**
A. Sign-off can proceed — critical workflows are validated and Critical issues are resolved; the Leaderboard gap is a known limitation, not a Critical issue
B. The VP of Learning's refusal is valid — Leaderboard is a critical workflow tool and its absence blocks sign-off
C. Sign-off should be marked CONDITIONAL until Cornerstone confirms the March 2027 roadmap target in writing
D. The team should escalate to Cornerstone GCS and request a 2-hour response, because a missing feature constitutes a critical workflow failure
**Correct answer:** A
**Correct answer feedback:** The sign-off criteria require that critical workflows are validated and Critical issues are resolved. Both conditions are met. The Leaderboard gap is a feature gap with a roadmap target — an expected limitation of the initial migration, not a Critical issue. Medium and Low issues, including feature gaps, do not block sign-off.
**Incorrect answer feedback:** Review the sign-off criteria in your lab guide. Sign-off requires that critical workflows are validated and Critical issues are resolved — not that every feature is present. The Leaderboard gap is a known limitation with a roadmap target. It is documented in the Known Gaps section of the UAT Test Results Summary, not treated as a blocker.
**Scored:** No — formative checkpoint
**Score value:** 0
**Retries:** Unlimited
**Enabling objective:** EO4

---

**Alias:** Question2
**Format:** Multiple choice — single answer
**Stem:** You are completing the Known Gaps section of the UAT Test Results Summary for the Leaderboard gap. Which combination of field values is correct?
**Options:**
A. Classification: Critical Issue — Priority: High — Action Required Before Production Migration: Yes
B. Classification: Expected Limitation — Priority: Low — Action Required Before Production Migration: No
C. Classification: Expected Limitation — Priority: Medium — Action Required Before Production Migration: Yes
D. Classification: Critical Issue — Priority: Low — Action Required Before Production Migration: No
**Correct answer:** B
**Correct answer feedback:** The Leaderboard gap is an expected limitation of the initial migration — a feature that will not be present by design, not because something failed. It carries Low priority because it has a roadmap target and does not affect critical workflows. No action is required before production migration.
**Incorrect answer feedback:** The Leaderboard gap is not a Critical issue — it is a feature gap with a roadmap target. Classifying it as Critical would misrepresent the migration status and could delay production migration unnecessarily. Review the Known Gaps documentation guidance in your lab guide.
**Scored:** No — formative checkpoint
**Score value:** 0
**Retries:** Unlimited
**Enabling objective:** EO4

---

**Alias:** Question3
**Format:** Multiple choice — single answer
**Stem:** You are reviewing the completed UAT Test Results Summary before submitting. Which of the following entries in the Roadmap Target field is correct?
**Options:**
A. "Leaderboard is tentatively targeted for March 2027"
B. "Leaderboard delivery is scheduled for Q1 2027"
C. "Leaderboard will be available by March 2027"
D. "Leaderboard will be released in a future update — date TBD"
**Correct answer:** A
**Correct answer feedback:** "Tentatively targeted for March 2027" is the approved language from the feature parity gap communication framework. It accurately represents the roadmap target without making a firm commitment. Options A and B imply a delivery guarantee that Cornerstone has not made. Option D is vague and does not give the VP of Learning the specific roadmap information she needs.
**Incorrect answer feedback:** The approved language is "tentatively targeted for March 2027." Any phrasing that implies a firm delivery date — "will be available," "is scheduled for," "will be released" — misrepresents Cornerstone's roadmap and is not approved. Review the Leaderboard Feature Parity Fact Sheet and the feature parity gap communication framework reference card.
**Scored:** No — formative checkpoint
**Score value:** 0
**Retries:** Unlimited
**Enabling objective:** EO4

---

**Alias:** SummativeQ1
**Format:** Multiple choice — single answer
**Stem:** During checklist execution, a Customer Administrator discovers that Skill Sync is not enabled between CSX and LX. What is the correct next action?
**Options:**
A. Enable Skill Sync in the CSX admin console and re-run the checklist item
B. Mark the item as Requires Action and proceed with the remaining checklist items
C. Open a GCS support case immediately — Skill Sync is a blocker that Cornerstone Services must resolve before migration can proceed
D. Document the gap in the Content Audit Summary and schedule a partner review call
**Correct answer:** C
**Correct answer feedback:** Skill Sync is explicitly labeled a blocker in the migration playbook. If Skill Sync is not enabled, the correct action is to stop and open a GCS support case. Cornerstone Services must enable Skill Sync — it is not a customer-side fix. Resolution takes approximately 2–3 weeks, and migration cannot proceed until it is resolved.
**Incorrect answer feedback:** Skill Sync is not a customer-side configuration item — the Customer Administrator cannot enable it directly. It is a blocker that requires Cornerstone Services to resolve via a GCS support case. Marking it as Requires Action understates the severity and the correct escalation path.
**Scored:** Yes
**Score value:** 1
**Retries:** 0
**Enabling objective:** EO1

---

**Alias:** SummativeQ2
**Format:** Multiple choice — single answer
**Stem:** A Customer Administrator is converting 12 dynamic groups to static groups. One group — "Compliance Training — All Employees" — controls access to mandatory annual compliance courses. How should this group be handled relative to the others?
**Options:**
A. Convert it last, after all other groups are confirmed working, to avoid disrupting compliance access during the conversion window
B. Treat it at standard priority — all groups must be converted before migration regardless of their purpose
C. Escalate it to Cornerstone GCS for conversion — compliance groups cannot be converted by the customer
D. Prioritize it and test it thoroughly before converting the other groups
**Correct answer:** D
**Correct answer feedback:** The migration playbook's decision framework is explicit: groups used for critical access control — including compliance training — must be prioritized and tested thoroughly. Converting the compliance group first and verifying that content access is intact before moving to other groups reduces the risk of a compliance gap during the migration window.
**Incorrect answer feedback:** The migration playbook identifies compliance-critical groups as the highest priority in the conversion sequence. Converting them last, or treating them at standard priority, increases the risk that a compliance access failure goes undetected until after migration. Cornerstone GCS does not perform group conversions — this is a customer-side task.
**Scored:** Yes
**Score value:** 1
**Retries:** 0
**Enabling objective:** EO2

---

**Alias:** SummativeQ3
**Format:** Multiple choice — single answer
**Stem:** A Customer Administrator is rebuilding email notification templates before the Pilot migration. She has six templates to rebuild: a compliance training due date reminder, a new course enrollment confirmation, a weekly learning digest, a manager team progress report, a system maintenance alert, and a course completion notice. Which template should she rebuild first?
**Options:**
A. New course enrollment confirmation — learners need to know immediately when they are enrolled
B. Compliance training due date reminder — compliance notifications are Tier 1 Critical and must be rebuilt before migration
C. Manager team progress report — managers need visibility into team learning before UAT begins
D. Weekly learning digest — it reaches the most users and should be tested early
**Correct answer:** B
**Correct answer feedback:** The notification rebuild prioritization framework places compliance notifications in Tier 1 — Critical — which must be rebuilt before migration. The compliance training due date reminder is the only Tier 1 item in this list. Enrollment confirmations and completion notices are Tier 2 — Important — rebuilt during the UAT window. The weekly learning digest is Tier 3 — Nice-to-have — rebuilt post-migration.
**Incorrect answer feedback:** The prioritization framework is compliance-first. Enrollment confirmations, manager reports, and engagement emails are important, but they are Tier 2 or Tier 3. Rebuilding them before compliance notifications leaves the organization exposed during the migration window if a compliance deadline fires before the critical template is in place.
**Scored:** Yes
**Score value:** 1
**Retries:** 0
**Enabling objective:** EO3

---

**Alias:** SummativeQ4
**Format:** Multiple choice — single answer
**Stem:** A Customer Administrator is completing the UAT Test Results Summary for a customer whose VP of Learning has refused to sign off because Leaderboard is unavailable. All Critical and High issues are resolved. All critical workflows are validated. How should the Leaderboard gap be classified in the Known Gaps section?
**Options:**
A. Critical Issue — the VP of Learning's refusal demonstrates that Leaderboard is a critical workflow dependency
B. High Issue — Leaderboard affects a significant portion of the learner population and should be escalated before sign-off
C. Expected Limitation — Leaderboard is a known feature gap in the initial migration, not a critical workflow failure
D. Medium Issue — the gap has a roadmap target and will be resolved within six months
**Correct answer:** C
**Correct answer feedback:** Leaderboard is a confirmed feature gap in the initial Single Architecture migration — it will not be present by design. A feature gap with a roadmap target is an expected limitation, not a Critical, High, or Medium issue. The sign-off criteria require that critical workflows are validated and Critical issues are resolved — both conditions are met. The VP of Learning's refusal does not change the classification; stakeholder objections are addressed through the feature parity gap communication framework, not by reclassifying the gap.
**Incorrect answer feedback:** The classification of a gap in the UAT Test Results Summary is based on its impact on critical workflows and data integrity — not on stakeholder sentiment. Leaderboard is a feature gap with a roadmap target. It does not break a critical workflow. Classifying it as Critical, High, or Medium would misrepresent the migration status and could delay production migration without justification.
**Scored:** Yes
**Score value:** 1
**Retries:** 0
**Enabling objective:** EO4

---

## Input Fields

**Token:** @lab.EssayTextBox(ObjectionResponse)[20]
**What the learner enters:** A written response to the VP of Learning addressing the Leaderboard feature gap. The response should explain what Leaderboard is and why it is not available in the initial migration, state the roadmap target using "tentatively targeted for March 2027" language, identify badges as a source of partial gamification continuity, and explain why the Leaderboard gap does not block production migration sign-off.
**Reviewer criteria:**
- Uses "tentatively targeted for March 2027" or equivalent approved language — does NOT use "will be available by," "is scheduled for," or any firm date commitment
- Identifies the Leaderboard gap as a feature gap / expected limitation, not a Critical issue
- Mentions that badges will be migrated as partial gamification continuity
- States that critical workflows are validated and Critical issues are resolved, and that sign-off can proceed
- Does not recommend delaying production migration

---

## Variables

None — this lab has no environment step.

---

## Screenshots to Supply

**Page: Review the UAT Environments**
Step: Review the Stage vs. Pilot distinction
Shot: Stage environment timeline showing Production-to-Stage copy one week before Pilot migration, 2–3 day Stage validation window Monday through Wednesday, and Pilot migration executing on Friday. Should be a simple horizontal timeline or two-column comparison card.

**Page: Review the Stage Validation Procedure**
Step: Review the Stage validation procedure in your lab guide
Shot: Stage validation checklist showing three smoke test items (can you log in, do you see your data, can you access Galaxy home page) and the Test Plan execution step, with a document-and-flag step below.

**Page: Review the UAT Testing Areas**
Step: Review the seven UAT testing categories in your lab guide
Shot: Seven UAT testing category cards arranged in a grid or list, each labeled with its category name and a brief description of what it covers.

**Page: Review the UAT Testing Workflow**
Step: Review the week-by-week UAT workflow in your lab guide
Shot: Week-by-week UAT workflow showing Week 1, Week 2, and Weeks 3–4 as a horizontal timeline or stacked sections with bullet points under each week.

**Page: Review the Escalation Framework**
Step: Review the escalation framework in your lab guide
Shot: Escalation framework table with four rows showing issue type, response time, and who handles each.

**Page: Review the Sign-Off Criteria**
Step: Review the sign-off criteria (before the formative activity)
Shot: Sign-off criteria displayed as two bullet points — critical workflows validated and Critical issues resolved — with a note that Medium and Low issues do not block sign-off.

**Page: Review the Leaderboard Feature Parity Facts**
Step: Review the Leaderboard Feature Parity Fact Sheet
Shot: Leaderboard fact sheet showing five bullet points: not in initial migration, tentatively targeted March 2027, badges will be migrated, new gamification in development, not a Critical issue.

**Page: Draft the Objection Response**
Step: Open the Feature Parity Gap Communication Framework reference card (before the essay box)
Shot: Blank response field or essay box with a prompt reading "Draft your written objection response to the VP of Learning here."

**Page: Complete the UAT Test Results Summary — Known Gaps**
Step: Open the UAT Test Results Summary template
Shot: UAT Test Results Summary template open to the Known Gaps section, showing column headers: Gap Description, Classification, Priority, Roadmap Target, Action Required Before Production Migration.

**Page: Complete the UAT Test Results Summary — Known Gaps**
Step: Enter a description of the Leaderboard gap in the Gap Description field
Shot: Known Gaps section with cursor in the Gap Description field, ready for input.

**Page: Complete the UAT Test Results Summary — Known Gaps**
Step: Set the Classification to Expected Limitation
Shot: Classification dropdown open showing options: Expected Limitation, Critical Issue, High Issue, Medium Issue, Low Issue — with Expected Limitation highlighted.

**Page: Complete the UAT Test Results Summary — Known Gaps**
Step: Set the Priority to Low
Shot: Priority field showing Low selected.

**Page: Complete the UAT Test Results Summary — Known Gaps**
Step: Enter the roadmap target in the Roadmap Target field
Shot: Roadmap Target field with cursor ready for input.

**Page: Complete the UAT Test Results Summary — Known Gaps**
Step: Set Action Required Before Production Migration to No
Shot: Action Required Before Production Migration field showing No selected.

**Page: Select the Migration Recommendation**
Step: Select APPROVED FOR PRODUCTION MIGRATION as the recommendation
Shot: Recommendation field showing two radio button options — APPROVED FOR PRODUCTION MIGRATION and CONDITIONAL — with APPROVED selected.

**Page: Select the Migration Recommendation**
Step: Document the Leaderboard gap in the Outstanding Items section
Shot: Outstanding Items section of the UAT Test Results Summary with a row for the Leaderboard gap, showing Priority, Roadmap Target, and Action Required columns.

**Page: Verify and Submit**
Step: Submit the completed UAT Test Results Summary
Shot: Completed UAT Test Results Summary showing all sections filled in — workflow validations passed, Leaderboard gap documented as Expected Limitation with Low priority and March 2027 roadmap target, recommendation set to APPROVED FOR PRODUCTION MIGRATION.

---

## Content Gaps

**G6 (inherited from Module PKB):** The "business owner" as a required sign-off party is named in the curriculum plan but not in Source 5's sign-off procedure, which names CSM and IT Lead. The lab positions the VP of Learning as a customer-side stakeholder whose objection must be resolved before the formal GCS submission — consistent with the "Customer sign-off" line in the UAT Test Results Summary template. SME confirmation recommended but does not block lab delivery.

**Feature parity gap communication framework:** The framework referenced throughout the objection scenario is sourced from M03 and is not reproduced in the M05 PKB. The lab references it as a job aid (the reference card in Media Requirements). The M03 module designer must supply this document before the lab can be delivered to learners. The lab's instructions and activities are designed around the framework's existence and the approved language it contains ("tentatively targeted").

**Supplemental sources used:** Source 1 (Single Architecture Migration Playbook, July 2026), Source 3 (Galaxy Migration AM/CSM Customer Readiness Checklist), Source 4 (Internal FAQ Version 5, July 2, 2026), Source 5 (Single Architecture Migration Playbook for Partners) — all as cited in the Module PKB.

---

## Recommended Editor Settings

**Scored activities (summative):** SummativeQ1, SummativeQ2, SummativeQ3, SummativeQ4 — 4 items, 1 point each, 4 points total
**Pass threshold:** 3 of 4 (75%) — no threshold stated in the lesson content; 75% set as standard for a four-item summative covering four distinct enabling objectives
**Retries on summative items:** 0 — one attempt per item
**Formative activities (unscored):** Question1, Question2, Question3 — unlimited retries, no score value
**Time limit:** None specified in the lesson content
**Essay box (ObjectionResponse):** Free text, not auto-scored; reviewer evaluates against the criteria in the Input Fields section above