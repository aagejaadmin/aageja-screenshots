# Conduct UAT and Obtain Migration Sign-Off

You are the Customer Administrator for Meridian Financial, a mid-size financial services firm in the final days of its Cornerstone Single Architecture migration. Your UAT team has completed testing in the Pilot environment. All Critical and High issues are resolved. Every critical workflow has been validated.

There is one problem: the VP of Learning is refusing to sign off. She manages quarterly sales training and relies heavily on Leaderboard to drive engagement. Leaderboard will not be available after migration, and she wants to delay production migration until it is.

Your job is to resolve this objection — in writing — using the feature parity gap communication framework, then complete the UAT Test Results Summary and submit Meridian Financial's sign-off recommendation.

Open the **Meridian Financial UAT Scenario Brief**, the **UAT Test Results Summary template**, the **Feature Parity Gap Communication Framework reference card**, and the **Leaderboard Feature Parity Fact Sheet** before you begin.

===

# Review the UAT Environments

Before you work through the scenario, orient yourself to the two pre-production environments you have been working in.

>[!knowledge] Stage vs. Pilot — Two Different Environments
>
>**Stage environment:** One week before the Pilot migration, Cornerstone GCS copies the Production database to Stage. You have a 2–3 day window (typically Monday through Wednesday) to run smoke tests and validate your pre-migration work. Stage is where you confirm readiness *before* the Pilot migration executes.
>
>**Pilot environment:** On Friday of that same week, Cornerstone migrates the Pilot environment. After that, the UAT validation window opens. UAT runs in Pilot for up to 4 weeks, with a goal of completing in 2 weeks.
>
>Stage validation and UAT are sequential, not interchangeable. If you find a critical issue during Stage validation, you flag it to Cornerstone before the Pilot migration runs. Issues found during UAT are tracked, prioritized, and resolved within the UAT window.

* [ ] Review the Stage vs. Pilot distinction in your lab guide before continuing.

![Stage environment timeline showing Production-to-Stage copy one week before Pilot migration, 2–3 day Stage validation window Monday through Wednesday, and Pilot migration executing on Friday](https://raw.githubusercontent.com/aagejaadmin/aageja-screenshots/main/placeholder.png)

===

# Review the Stage Validation Procedure

Stage validation is a 2–3 day smoke-test window. Its purpose is narrow: confirm that the environment is stable and your pre-migration work is intact before the Pilot migration runs.

>[!knowledge] What Stage Validation Covers
>
>Run three smoke tests first:
>
>- Can you log in as both a learner and an admin?
>- Do you see your data?
>- Can you access the new Galaxy home page?
>
>Then run through the Test Plan you prepared in Phase 1. Document any issues you find and flag high-priority issues to Cornerstone immediately. Stage validation is not the time for comprehensive UAT — that happens in Pilot.

* [ ] Review the Stage validation procedure in your lab guide.

![Stage validation checklist showing three smoke test items and Test Plan execution step, with a document and flag high-priority issues step below](https://raw.githubusercontent.com/aagejaadmin/aageja-screenshots/main/placeholder.png)

===

# Review the UAT Testing Areas

UAT in the Pilot environment covers seven categories. You will not test all of them in this lab — Meridian Financial's team has already completed testing. But you need to know the categories to evaluate what "critical workflows validated" means when you apply the sign-off criteria.

>[!knowledge] The Seven UAT Testing Categories
>
>1. **Learner Workflows** — login, transcript visibility, content discovery, enrollment, skills, Course Player
>2. **Manager Workflows** — Manager Dashboard, team progress, course recommendations, team reports
>3. **Admin Workflows** — unified admin console, user and group management, content visibility, security roles, notifications
>4. **Data Integrity** — user records, assignments and transcripts, skills data, group memberships, UGC visibility
>5. **Configuration Validation** — security roles, groups, Home Page, Unified Navigation, Manager Dashboard, profile pages
>6. **Post-Migration Rebuild Validation** — notification templates, custom reports, third-party integrations, deeplinks
>7. **Known Gaps & Workarounds** — Live Events, Project SmartCards, private UGC, Analytics+ reports

* [ ] Review the seven UAT testing categories in your lab guide.

![Seven UAT testing category cards arranged in a grid, each labeled with its category name and a brief description of what it covers](https://raw.githubusercontent.com/aagejaadmin/aageja-screenshots/main/placeholder.png)

===

# Review the UAT Testing Workflow

UAT is structured week by week. Knowing the sequence helps you evaluate whether Meridian Financial's team has completed the right work before sign-off.

>[!knowledge] Week-by-Week UAT Workflow
>
>**Week 1:** Run learner and manager smoke tests. Validate data integrity. Confirm groups are working. Spot-check skills data. Document all issues and classify them as Critical, High, Medium, or Low.
>
>**Week 2:** Rebuild and test critical notifications. Rebuild and test critical reports. Test group-based content access. Validate security roles. Resolve all Critical and High issues.
>
>**Weeks 3–4 (if needed):** Resolve remaining Medium and Low issues. Rebuild non-critical notifications and reports. Reconfigure additional third-party integrations. Train the admin team on the new console.

* [ ] Review the week-by-week UAT workflow in your lab guide.

![Week-by-week UAT workflow showing Week 1 through Weeks 3-4 as a horizontal timeline with bullet points under each week](https://raw.githubusercontent.com/aagejaadmin/aageja-screenshots/main/placeholder.png)

===

# Review the Escalation Framework

During UAT, different issue types route to different teams on different timelines. You need to know this framework to evaluate issue severity and to understand why the Leaderboard gap does not trigger an escalation.

>[!knowledge] Escalation Framework During UAT
>
>| Issue Type | Response Time | Who Handles |
>|---|---|---|
>| Data loss or critical workflow broken | 2 hours | Cornerstone GCS → Engineer |
>| Security role or permissions issue | 4 hours | Cornerstone Services + Partner |
>| Notification or report rebuild question | 1 business day | Partner or Cornerstone Services |
>| Nice-to-have or enhancement request | After validation | Backlog for post-migration |

* [ ] Review the escalation framework in your lab guide.

![Escalation framework table with four rows showing issue type, response time, and who handles each, formatted as a reference table](https://raw.githubusercontent.com/aagejaadmin/aageja-screenshots/main/placeholder.png)

===

# Review the Sign-Off Criteria

Before you evaluate the VP of Learning's objection, you must know exactly what the sign-off criteria require. These criteria determine whether a given gap blocks production migration or not.

>[!knowledge] What Constitutes Acceptable Testing for Sign-Off
>
>Sign-off is appropriate when:
>
>- **Critical workflows have been validated** across all seven UAT testing categories
>- **All Critical issues have been resolved**
>
>Medium and Low issues do **not** block sign-off. They are documented in the UAT Test Results Summary and resolved after production migration.
>
>A feature gap — a capability that will not be present in the initial migration — is not a Critical issue unless it breaks a critical workflow. A feature gap with a roadmap target is documented in the Known Gaps section of the UAT Test Results Summary.

>[!alert] The sign-off criteria are the standard you apply in the next activity. Read them carefully before you proceed.

@lab.Activity(Question1)

![Sign-off criteria displayed as two bullet points — critical workflows validated and Critical issues resolved — with a note that Medium and Low issues do not block sign-off](https://raw.githubusercontent.com/aagejaadmin/aageja-screenshots/main/placeholder.png)

===

# Review the Leaderboard Feature Parity Facts

Before you draft your objection response, you need the facts. Open the **Leaderboard Feature Parity Fact Sheet** and review the following information. You will use all of it in your response.

>[!knowledge] Leaderboard — What You Need to Know
>
>- Leaderboard will **not** be included in the initial Single Architecture migration
>- A unified leaderboard is **tentatively targeted for March 2027** — this is a roadmap target, not a commitment
>- **Badges will be migrated** and will eventually be unified across LMS and LXP capabilities
>- A **new form of gamification** is being developed as a replacement for the current Leaderboard
>- The Leaderboard gap is **not a Critical issue** — it is a feature gap with a roadmap target

>[!alert] Approved language: **"tentatively targeted for March 2027"**
>
>Do not say "will be available by March 2027" or promise any specific delivery date. The roadmap target is not a commitment. Using firm date language is a compliance risk for your organization and misrepresents Cornerstone's roadmap.

>[!knowledge] What Not to Say
>
>The feature parity gap communication framework on your reference card identifies language that is not approved. The most consequential error in this scenario is promising a specific delivery date. "Tentatively targeted" is the approved phrasing. Any variation that implies a firm commitment is wrong.

* [ ] Review the Leaderboard Feature Parity Fact Sheet before drafting your response.

![Leaderboard fact sheet showing five bullet points: not in initial migration, tentatively targeted March 2027, badges will be migrated, new gamification in development, not a Critical issue](https://raw.githubusercontent.com/aagejaadmin/aageja-screenshots/main/placeholder.png)

===

# Draft the Objection Response

You are now ready to draft your written response to the VP of Learning. Open the **Feature Parity Gap Communication Framework reference card** from M03. Use it alongside the Leaderboard facts you just reviewed.

Your response must address four things:

1. What Leaderboard is and why it is not available in the initial migration
2. What the roadmap target is — using approved language
3. What partial gamification continuity exists in the interim
4. Why the Leaderboard gap does not block production migration sign-off

>[!note] This is the highest-value practice in the module. Take the time to draft a complete response. A real VP of Learning will push back if your answer is vague, if you promise a date you cannot commit to, or if you cannot explain what replaces Leaderboard in the interim.

>[!hint] Your response does not need to be long. It needs to be accurate, specific, and use the approved language from the reference card. A three-to-four paragraph response that covers all four points is sufficient.

Write your objection response in the field below.

@lab.EssayTextBox(ObjectionResponse)[20]

![Blank response field with a prompt reading "Draft your written objection response to the VP of Learning here"](https://raw.githubusercontent.com/aagejaadmin/aageja-screenshots/main/placeholder.png)

===

# Complete the UAT Test Results Summary — Known Gaps

Open the **partially completed UAT Test Results Summary template**. The workflow validation results are already filled in — all critical workflows passed. Your task is to document the Leaderboard gap in the Known Gaps section.

>[!knowledge] How to Document a Known Gap
>
>The Known Gaps section of the UAT Test Results Summary captures feature gaps and expected limitations — things that are absent from the initial migration by design, not because something went wrong. Each entry includes:
>
>- **Gap description** — what is missing
>- **Classification** — Expected Limitation (not a Critical issue)
>- **Priority** — Low, Medium, High, or Critical
>- **Roadmap target** — if one exists
>- **Action required before production migration** — Yes or No

* [ ] Open the UAT Test Results Summary template.

![UAT Test Results Summary template open to the Known Gaps section, showing column headers: Gap Description, Classification, Priority, Roadmap Target, Action Required Before Production Migration](https://raw.githubusercontent.com/aagejaadmin/aageja-screenshots/main/placeholder.png)

* [ ] In the **Gap Description** field, enter a description of the Leaderboard gap.

![Known Gaps section with cursor in the Gap Description field, ready for input](https://raw.githubusercontent.com/aagejaadmin/aageja-screenshots/main/placeholder.png)

* [ ] Set the **Classification** to **Expected Limitation**.

>[!alert] Do not classify the Leaderboard gap as a Critical issue. It is a feature gap with a roadmap target — an expected limitation of the initial migration, not a workflow failure.

![Classification dropdown open showing options: Expected Limitation, Critical Issue, High Issue, Medium Issue, Low Issue — with Expected Limitation highlighted](https://raw.githubusercontent.com/aagejaadmin/aageja-screenshots/main/placeholder.png)

* [ ] Set the **Priority** to **Low**.

![Priority field showing Low selected](https://raw.githubusercontent.com/aagejaadmin/aageja-screenshots/main/placeholder.png)

* [ ] Enter the roadmap target in the **Roadmap Target** field.

>[!hint] Use the approved language from the Leaderboard Fact Sheet. Do not enter a firm date.

![Roadmap Target field with cursor ready for input](https://raw.githubusercontent.com/aagejaadmin/aageja-screenshots/main/placeholder.png)

* [ ] Set **Action Required Before Production Migration** to **No**.

![Action Required Before Production Migration field showing No selected](https://raw.githubusercontent.com/aagejaadmin/aageja-screenshots/main/placeholder.png)

@lab.Activity(Question2)

===

# Select the Migration Recommendation

With the Known Gaps section complete, you must now select the overall recommendation in the UAT Test Results Summary and document the outstanding item.

>[!knowledge] The Two Recommendation Options
>
>The UAT Test Results Summary offers two recommendation values:
>
>- **APPROVED FOR PRODUCTION MIGRATION** — all Critical issues resolved, critical workflows validated; any remaining items are Medium/Low and do not block migration
>- **CONDITIONAL** — sign-off is granted with conditions that must be met before migration proceeds; used when a specific action is required before production migration can run

* [ ] Select **APPROVED FOR PRODUCTION MIGRATION** as the recommendation.

![Recommendation field showing two radio button options: APPROVED FOR PRODUCTION MIGRATION and CONDITIONAL — with APPROVED selected](https://raw.githubusercontent.com/aagejaadmin/aageja-screenshots/main/placeholder.png)

* [ ] In the **Outstanding Items** section, document the Leaderboard gap as an outstanding item: Low priority, roadmap target March 2027, no action required before production migration.

![Outstanding Items section of the UAT Test Results Summary with a row for the Leaderboard gap, showing Priority, Roadmap Target, and Action Required columns](https://raw.githubusercontent.com/aagejaadmin/aageja-screenshots/main/placeholder.png)

===

# Verify and Submit

Before you submit the UAT Test Results Summary, review it against the sign-off criteria. A submission with errors — a Critical classification on the Leaderboard gap, a firm date promise, or a CONDITIONAL recommendation — will delay Meridian Financial's production migration.

* [ ] Confirm the Leaderboard gap is classified as **Expected Limitation**, not as a Critical issue.

* [ ] Confirm the roadmap target field uses **"tentatively targeted"** language and does not promise a specific delivery date.

* [ ] Confirm the recommendation is **APPROVED FOR PRODUCTION MIGRATION**.

* [ ] Confirm the outstanding items section documents the Leaderboard gap with **Low priority** and **no action required before production migration**.

>[!alert] If any of these four checks fails, return to the relevant section and correct it before submitting.

@lab.Activity(Question3)

* [ ] Submit the completed UAT Test Results Summary.

![Completed UAT Test Results Summary showing all sections filled in: workflow validations passed, Leaderboard gap documented as Expected Limitation with Low priority and March 2027 roadmap target, recommendation set to APPROVED FOR PRODUCTION MIGRATION](https://raw.githubusercontent.com/aagejaadmin/aageja-screenshots/main/placeholder.png)

===

# Summative Assessment

Answer all four questions. Each question covers a different phase of the pre-migration validation and sign-off process.

@lab.Activity(SummativeQ1)

@lab.Activity(SummativeQ2)

@lab.Activity(SummativeQ3)

@lab.Activity(SummativeQ4)