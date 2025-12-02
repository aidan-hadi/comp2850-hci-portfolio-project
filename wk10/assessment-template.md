# COMP2850 HCI Assessment: Evaluation & Redesign Portfolio

**Student**: [201832158]
**Submission date**: [DD/MM/YYYY]
**Academic Year**: 2025-26

---

## Privacy & Ethics Statement

- [ ] I confirm all participant data is anonymous (session IDs use P1_xxxx format, not real names)
- [ ] I confirm all screenshots are cropped/blurred to remove PII (no names, emails, student IDs visible)
- [ ] I confirm all participants gave informed consent
- [ ] I confirm this work is my own (AI tools used for code assistance are cited below)
---
**AI tools used** (if any):   
No AI tools were used in any way   

## 1. Protocol & Tasks

### Link to Needs-Finding (LO2)

## **Story S1: Confirmation Feedback**  
**Situation**: When I submit a form (add task, edit task, delete task)  
**Motivation**: I want immediate, explicit confirmation that the action succeeded  
**Outcome**: So I can trust the interface without refreshing to verify  
**Underlying need**: Because uncertainty about save status causes anxiety and inefficient workarounds (page reload)  

**Evidence**: Participant A  
**Inclusion risk**: Low digital Literacy, untrusting of computer systems  
**Type**: Job story  
**How does Task 1-4 test this**: Task 1-4 test this at every step, by confirming these texts exist, and if not, they will be reported.  

## **Story S2: Edit Button**  
**Situation**: When I want to edit a task in case I write something wrong  
**Motivation**: I want to be able to change the task without needing to rewrite the task   
**Outcome**: So I can save time   
**Underlying need**: Because the user can become annoyed at the interface    

**Evidence**: Participant B   
**Inclusion risk**: None    
**Type**: Job story  
**How does Task 2 test this**: Task 2 test this feature, and links it to this job story  

## **Story S3: Working Task Filter Button**  
**Situation**: When I want to filter the tasks by a certain name, to check if i've done something    
**Motivation**: I cannot find the task in a long list! Did I delete it?? Where is it?  
**Outcome**: Task is filtered   
**Underlying need**: The user would have to scroll through every task, which is inheriently unsorted, to find the right information.   

**Evidence**: Participant C   
**Inclusion risk**: None    
**Type**: Job story   
**How does Task 1 test this**: Task 1 test this feature, and links it to this job story  


---

# Evaluation Tasks — Week 9

## Task T1: Filter Tasks

**Scenario**:
"You've been asked to find all tasks containing the word 'report'. Use the filter box to show only matching tasks, then count how many tasks remain."

**Setup**:
- Pre-populate task list with 10 tasks, 3 containing "report" in title
- Example: "Submit expense report", "Draft annual report", "Review quarterly report", plus 7 others

**Success criteria**:
- Participant uses filter box (types "report")
- Participant reports correct count (3 tasks)
- Completed within 2 minutes
- No validation errors

**Metrics**:
- Time from page load to stating count (ms)
- Completion (0 = fail, 1 = success)
- Validation errors (count)
- Confidence rating (1–5): "How confident are you that you found all matching tasks?"

**Accessibility checks**:
- Result count announced by screen reader?
- Keyboard-only completion possible?
- Works with JS disabled?

---

## Task T2: Edit Task Title

**Scenario**:
"The task 'Submit invoices' has a typo. Change it to 'Submit invoices by Friday' and save the change."

**Setup**:
- Task ID 5: "Submit invoices" (visible in list)
- Participant must click Edit, change text, save

**Success criteria**:
- Participant activates edit mode
- Participant updates title correctly
- Change persists after save
- Completed within 90 seconds
- No validation errors

**Metrics**:
- Time from click Edit to save confirmation (ms)
- Completion (0/1)
- Validation errors (e.g., blank title submitted by mistake)
- Confidence rating (1–5)

**Accessibility checks**:
- Status message "Updated [title]" announced?
- Focus remains on/near edited task?
- Works with keyboard only?
- Works with JS disabled?

---

## Task T3: Add New Task

**Scenario**:
"You need to remember to 'Call supplier about delivery'. Add this as a new task."

**Setup**:
- Empty or partially filled task list
- Form visible at top of page

**Success criteria**:
- Participant types exact title (or close match)
- Submits form
- New task appears in list
- Completed within 60 seconds

**Metrics**:
- Time from focus in input to confirmation (ms)
- Completion (0/1)
- Validation errors (if they submit blank by accident)
- Confidence rating (1–5)

**Accessibility checks**:
- Status message "Added [title]" announced?
- Form remains usable after error (if triggered)?
- Works with JS disabled (PRG)?

---

## Task T4: Delete Task

**Scenario**:
"The task 'Test entry' is no longer needed. Delete it from the list."

**Setup**:
- Task ID 8: "Test entry" (visible in list)

**Success criteria**:
- Participant clicks Delete button
- Confirms deletion (HTMX path) or submits form (no-JS)
- Task removed from list
- Completed within 45 seconds

**Metrics**:
- Time from click Delete to confirmation (ms)
- Completion (0/1)
- Confirmation dialog acknowledged (HTMX only)
- Confidence rating (1–5)

**Accessibility checks**:
- Delete button has accessible name ("Delete task: Test entry")?
- Status message "Deleted [title]" announced (HTMX)?
- Works with keyboard only?
- Works with JS disabled (no confirmation, but functions)?

---

## Task Order

**Recommended sequence**:
1. **Warm-up** (not timed): "Browse the task list and familiarize yourself with the interface."
2. T3 (Add) — Low cognitive load, builds confidence
3. T1 (Filter) — Medium complexity, tests search
4. T2 (Edit) — Tests inline interaction, validation
5. T4 (Delete) — Destructive action, tests confirmation
6. **Debrief** (qualitative): Open-ended questions

**Counterbalance** if testing multiple participants: alternate T1/T2 order to avoid learning effects.

---

## Notes for Facilitator

- **Do not help** unless participant is completely stuck (>3 min). Note as "facilitated" in observations.
- **Think-aloud optional**: Ask participants to narrate their thoughts if comfortable. Don't force.
- **Screen reader users**: Allow extra time for navigation. Log SR-specific observations separately.
- **Keyboard-only**: Offer keyboard-only variant to 1-2 participants for comparison.
- **No-JS**: Test at least 1 participant with JS disabled to verify parity.

---

## Success Definitions

**Completion codes**:
- `1` = Task fully completed, correct outcome
- `0.5` = Partial completion (e.g., found filter but wrong count)
- `0` = Failed or abandoned

**Time bounds**:
- T1: 120s
- T2: 90s
- T3: 60s
- T4: 45s

If participant exceeds time, prompt: "Would you like to continue, or shall we move to the next task?"


## Consent Process

**Before starting** (read aloud):

> "Thanks for agreeing to pilot our prototype. This is a quick usability test—about 15 minutes. I'll ask you to complete 4 tasks while I observe and take notes. I'm testing the interface, not you, so there are no wrong answers.
>
> **What we're collecting**:
> - Task completion times (from server logs)
> - Whether you complete each task successfully
> - Errors or validation issues
> - Your confidence ratings after each task
> - My notes on any hesitations or accessibility issues
>
> **What we're NOT collecting**:
> - Your name, email, or student ID
> - Screen recordings or audio
> - Your device details beyond 'keyboard-only' or 'screen reader'
>
> I'll assign you a random session code (like `sid=X7kL9p`) which will appear in the logs. You can request that I delete all data linked to your session code at any time, even after today.
>
> **You can stop at any time**, no questions asked, and it won't affect your grade.
>
> Do you have any questions before we start?"

**Verbal consent**: "Are you happy to proceed?"

Record in `wk09/lab-wk9/research/consent-log.md`:
Date: 2025-10-15 Participant code: P1 Session ID: X7kL9p Consent: Verbal consent given Notes: Requested keyboard-only variant

**Opt-out path**: If participant requests deletion:
1. Open `data/metrics.csv`
2. Delete all rows where `session_id=X7kL9p`
3. Note in `consent-log.md`: "Data deleted on request [date]"


---

## 2. Findings Table

**Instructions**: Fill in this table with 3-5 findings from your pilots. Link each finding to data sources.

| Finding | Data Source | Observation (Quote/Timestamp) | WCAG | Impact (1-5) | Inclusion (1-5) | Effort (1-5) | Priority |
|---------|-------------|------------------------------|------|--------------|-----------------|--------------|----------|
| SR errors not announced | metrics.csv L47-49 + P2 notes 14:23 | P2: "I didn't hear any error" | 3.3.1 Level A | 5 | 5 | 3 | 7 |
| [Your finding 2] | [Link to metrics.csv line OR pilot notes] | [Participant quote + timestamp] | [WCAG criterion] | [1-5] | [1-5] | [1-5] | [Score] |
| [Your finding 3] | | | | | | | |
| [Your finding 4] | | | | | | | |
| [Your finding 5] | | | | | | | |

**Priority formula**: (Impact + Inclusion) - Effort

**Top 3 priorities for redesign**:
1. [Finding #X - Priority score Y]
2. [Finding #X - Priority score Y]
3. [Finding #X - Priority score Y]

---

## 3. Pilot Metrics (metrics.csv)

**Instructions**: Paste your raw CSV data here OR attach metrics.csv file

```csv
ts_iso,session_id,request_id,task_code,step,outcome,ms,http_status,js_mode
2025-11-22T14:18:23.456Z,P1_a7f3,req_001,T1_add,success,,890,200,on
2025-12-02T14:05:39.921515200Z,P1_5zljfj,r_ff8b75da,T0_list,success,,34,200,off
2025-12-02T14:06:00.170233600Z,P1_5zljfj,r_cf7e60bf,T3_add,success,,90,200,on
2025-12-02T14:09:58.869399300Z,P1_5zljfj,r_62958dbe,T1_filter,success,,30,200,on
2025-12-02T14:09:59.856707500Z,P1_5zljfj,r_c87d5be9,T1_filter,success,,6,200,on
2025-12-02T14:10:00.342958600Z,P1_5zljfj,r_9678ddf5,T1_filter,success,,4,200,on
2025-12-02T14:10:01.879752800Z,P1_5zljfj,r_2eee8d9e,T1_filter,success,,9,200,on
2025-12-02T14:12:28.491939500Z,P1_5zljfj,r_a6f9a5db,T1_filter,success,,8,200,on
2025-12-02T14:14:08.969239300Z,P1_5zljfj,r_48898893,T4_delete,success,,10,200,on
2025-12-02T14:16:03.702626Z,P1_5zljfj,r_f38a635b,T3_add,success,,14,200,on
2025-12-02T14:21:31.935361900Z,P1_5zljfj,r_4b83abe1,T0_list,success,,151,200,off
2025-12-02T14:22:09.015149900Z,P2_JUisui,r_b7b9b2d5,T0_list,success,,22,200,off
2025-12-02T14:22:26.508560Z,P2_JUisui,r_56e339ad,T3_add,success,,14,200,on
2025-12-02T14:25:50.317912800Z,P2_JUisui,r_e1b29fd3,T1_filter,success,,9,200,on
2025-12-02T14:25:52.385796800Z,P2_JUisui,r_4374224e,T1_filter,success,,0,200,on
2025-12-02T14:25:53.586247400Z,P2_JUisui,r_4fba6b9b,T1_filter,success,,7,200,on
2025-12-02T14:25:56.491719100Z,P2_JUisui,r_58c81a6d,T1_filter,success,,6,200,on
2025-12-02T14:25:56.607099300Z,P2_JUisui,r_949ef33c,T1_filter,success,,6,200,on
2025-12-02T14:26:54.022355500Z,P2_JUisui,r_8531f50d,T1_filter,success,,7,200,on
2025-12-02T14:26:54.874997600Z,P2_JUisui,r_4000f59d,T1_filter,success,,16,200,on
2025-12-02T14:28:51.335513200Z,P2_JUisui,r_e843551a,T4_delete,success,,2,200,on
2025-12-02T14:28:56.299673300Z,P2_JUisui,r_b71735c2,T4_delete,success,,8,200,on
2025-12-02T14:36:36.075939800Z,P3_1FhG3d,r_52742e0d,T0_list,success,,46,200,off
2025-12-02T14:37:48.911654800Z,P3_1FhG3d,r_9178ca6e,T3_add,success,,23,200,off
2025-12-02T14:37:48.938694800Z,P3_1FhG3d,r_f6800ad4,T0_list,success,,19,200,off
2025-12-02T14:40:59.212334500Z,P3_1FhG3d,r_da3642c9,T1_filter,success,,10,200,on
2025-12-02T14:41:00.259630800Z,P3_1FhG3d,r_4aad4cc5,T1_filter,success,,7,200,on
2025-12-02T14:41:03.775989100Z,P3_1FhG3d,r_396cf391,T1_filter,success,,10,200,on
2025-12-02T14:44:33.812354400Z,P3_1FhG3d,r_9b24b622,T4_delete,success,,6,200,on
2025-12-02T14:51:32.654261100Z,P4_AEh6u7,r_0e57d05d,T1_filter,success,,23,200,off
2025-12-02T14:51:32.684580800Z,P4_AEh6u7,r_36ac3d74,T0_list,success,,24,200,off
2025-12-02T14:55:02.984197400Z,P4_AEh6u7,r_47253b5d,T3_add,success,,44,200,on
2025-12-02T14:58:57.622544Z,P4_AEh6u7,r_c8f2910e,T1_filter,success,,11,200,on
2025-12-02T14:59:01.472216600Z,P4_AEh6u7,r_980acac3,T1_filter,success,,6,200,on
2025-12-02T15:01:15.317114400Z,P4_AEh6u7,r_5f382d6a,T1_filter,success,,11,200,on
2025-12-02T15:01:39.907001200Z,P4_AEh6u7,r_0161e344,T4_delete,success,,6,200,on

```

**Participant summary**:
- **P1**: Standard Mouse + HTMX
- **P2**: Standard Keyboard + HTMX
- **P3** Standard Mouse + noJS
- **P4** Standard Mouse (But keyboard was allowed and used) + Screen reader + HTMX

**Total participants**: n = 4

---

## 4. Implementation Diffs

**Instructions**: Show before/after code for 1-3 fixes. Link each to findings table.

### Fix 1: [Fix Name]

**Addresses finding**: [Finding #X from table above]

**Before** ([file path:line number]):
```kotlin
// ❌ Problem code
[Paste your original code here]
```

**After** ([file path:line number]):
```kotlin
// ✅ Fixed code
[Paste your improved code here]
```

**What changed**: [1 sentence - what you added/removed/modified]

**Why**: [1 sentence - which WCAG criterion or usability issue this fixes]

**Impact**: [1-2 sentences - how this improves UX, who benefits]

---

### Fix 2: [Fix Name]

**Addresses finding**: [Finding #X]

**Before**:
```kotlin
[Original code]
```

**After**:
```kotlin
[Fixed code]
```

**What changed**:

**Why**:

**Impact**:

---

[Add Fix 3 if applicable]

---

## 5. Verification Results

### Part A: Regression Checklist (20 checks)

**Instructions**: Test all 20 criteria. Mark pass/fail/n/a + add notes.

| Check | Criterion | Level | Result | Notes |
|-------|-----------|-------|--------|-------|
| **Keyboard (5)** | | | | |
| K1 | 2.1.1 All actions keyboard accessible | A | [pass/fail] | [e.g., "Tested Tab/Enter on all buttons"] |
| K2 | 2.4.7 Focus visible | AA | [pass/fail] | [e.g., "2px blue outline on all interactive elements"] |
| K3 | No keyboard traps | A | [pass/fail] | [e.g., "Can Tab through filter, edit, delete without traps"] |
| K4 | Logical tab order | A | [pass/fail] | [e.g., "Top to bottom, left to right"] |
| K5 | Skip links present | AA | [pass/fail/n/a] | [e.g., "Skip to main content works"] |
| **Forms (3)** | | | | |
| F1 | 3.3.2 Labels present | A | [pass/fail] | [e.g., "All inputs have <label> or aria-label"] |
| F2 | 3.3.1 Errors identified | A | [pass/fail] | [e.g., "Errors have role=alert (FIXED in Fix #1)"] |
| F3 | 4.1.2 Name/role/value | A | [pass/fail] | [e.g., "All form controls have accessible names"] |
| **Dynamic (3)** | | | | |
| D1 | 4.1.3 Status messages | AA | [pass/fail] | [e.g., "Status div has role=status"] |
| D2 | Live regions work | AA | [pass/fail] | [e.g., "Tested with NVDA, announces 'Task added'"] |
| D3 | Focus management | A | [pass/fail] | [e.g., "Focus moves to error summary after submit"] |
| **No-JS (3)** | | | | |
| N1 | Full feature parity | — | [pass/fail] | [e.g., "All CRUD ops work without JS"] |
| N2 | POST-Redirect-GET | — | [pass/fail] | [e.g., "No double-submit on refresh"] |
| N3 | Errors visible | A | [pass/fail] | [e.g., "Error summary shown in no-JS mode"] |
| **Visual (3)** | | | | |
| V1 | 1.4.3 Contrast minimum | AA | [pass/fail] | [e.g., "All text 7.1:1 (AAA) via CCA"] |
| V2 | 1.4.4 Resize text | AA | [pass/fail] | [e.g., "200% zoom, no content loss"] |
| V3 | 1.4.11 Non-text contrast | AA | [pass/fail] | [e.g., "Focus indicator 4.5:1"] |
| **Semantic (3)** | | | | |
| S1 | 1.3.1 Headings hierarchy | A | [pass/fail] | [e.g., "h1 → h2 → h3, no skips"] |
| S2 | 2.4.1 Bypass blocks | A | [pass/fail] | [e.g., "<main> landmark, <nav> for filter"] |
| S3 | 1.1.1 Alt text | A | [pass/fail] | [e.g., "No images in interface OR all have alt"] |

**Summary**: [X/20 pass], [Y/20 fail]
**Critical failures** (if any): [List any Level A fails]

---

### Part B: Before/After Comparison

**Instructions**: Compare Week 9 baseline (pre-fix) to Week 10 (post-fix). Show improvement.

| Metric | Before (Week 9, n=X) | After (Week 10, n=Y) | Change | Target Met? |
|--------|----------------------|----------------------|--------|-------------|
| SR error detection | [e.g., 0/2 (0%)] | [e.g., 2/2 (100%)] | [e.g., +100%] | [✅/❌] |
| Validation error rate | [e.g., 33%] | [e.g., 0%] | [e.g., -33%] | [✅/❌] |
| Median time [Task X] | [e.g., 1400ms] | [e.g., 1150ms] | [e.g., -250ms] | [✅/❌] |
| WCAG [criterion] pass | [fail] | [pass] | [— ] | [✅/❌] |

**Re-pilot details**:
- **P5** (post-fix): [Variant - e.g., "Screen reader user, NVDA + keyboard"] - [Date piloted]
- **P6** (if applicable): [Variant] - [Date]

**Limitations / Honest reporting**:
[If metrics didn't improve or only modestly: explain why. Small sample size? Wrong fix? Needs more iteration? Be honest - valued over perfect results.]

---

## 6. Evidence Folder Contents

**Instructions**: List all files in your evidence/ folder. Provide context.

### Screenshots

| Filename | What it shows | Context/Link to finding |
|----------|---------------|-------------------------|
| before-sr-error.png | Error message without role="alert" | Finding #1 - SR errors not announced |
| after-sr-error.png | Error message WITH role="alert" added | Fix #1 verification |
| regression-axe-report.png | axe DevTools showing 0 violations | Verification Part A |
| [your-screenshot-3.png] | [Description] | [Which finding/fix this supports] |

**PII check**:
- [ ] All screenshots cropped to show only relevant UI
- [ ] Browser bookmarks/tabs not visible
- [ ] Participant names/emails blurred or not visible

---

### Pilot Notes

**Instructions**: Attach pilot notes as separate files (P1-notes.md, P2-notes.md, etc.). Summarize key observations here.

**P1** ([ Variant - e.g., "Standard mouse + HTMX"]):
- **Key observation 1**: [Quote + timestamp - e.g., "Struggled with filter button (09:47)"]
- **Key observation 2**: [Quote + timestamp]

**P2** ([Variant]):
- **Key observation 1**: [Quote + timestamp]
- **Key observation 2**: [Quote + timestamp]

[Repeat for P3, P4 if applicable]

---

## Evidence Chain Example (Full Trace)

**Instructions**: Pick ONE finding and show complete evidence trail from data → fix → verification.

**Finding selected**: [e.g., "Finding #1 - SR errors not announced"]

**Evidence trail**:
1. **Data**: metrics.csv lines 47-49 show P2 (SR user) triggered validation_error 3 times
2. **Observation**: P2 pilot notes timestamp 14:23 - Quote: "I don't know if it worked, didn't hear anything"
3. **Screenshot**: before-sr-error.png shows error message has no role="alert" or aria-live
4. **WCAG**: 3.3.1 Error Identification (Level A) violation - errors not programmatically announced
5. **Prioritisation**: findings-table.csv row 1 - Priority score 7 (Impact 5 + Inclusion 5 - Effort 3)
6. **Fix**: implementation-diffs.md Fix #1 - Added role="alert" + aria-live="assertive" to error span
7. **Verification**: verification.csv Part A row F2 - 3.3.1 now PASS (tested with NVDA)
8. **Before/after**: verification.csv Part B - SR error detection improved from 0% to 100%
9. **Re-pilot**: P5 (SR user) pilot notes - "Heard error announcement immediately, corrected and succeeded"

**Complete chain**: Data → Observation → Interpretation → Fix → Verification ✅

---

## Submission Checklist

Before submitting, verify:

**Files**:
- [ ] This completed template (submission-template.md)
- [ ] metrics.csv (or pasted into Section 3)
- [ ] Pilot notes (P1-notes.md, P2-notes.md, etc. OR summarised in Section 6)
- [ ] Screenshots folder (all images referenced above)
- [ ] Privacy statement signed (top of document)

**Evidence chains**:
- [ ] findings-table.csv links to metrics.csv lines AND/OR pilot notes timestamps
- [ ] implementation-diffs.md references findings from table
- [ ] verification.csv Part B shows before/after for fixes

**Quality**:
- [ ] No PII in screenshots (checked twice!)
- [ ] Session IDs anonymous (P1_xxxx format, not real names)
- [ ] Honest reporting (limitations acknowledged if metrics didn't improve)
- [ ] WCAG criteria cited specifically (e.g., "3.3.1" not just "accessibility")

**Pass criteria met**:
- [ ] n=2+ participants (metrics.csv has 2+ session IDs)
- [ ] 3+ findings with evidence (findings-table.csv complete)
- [ ] 1-3 fixes implemented (implementation-diffs.md shows code)
- [ ] Regression complete (verification.csv has 20 checks)
- [ ] Before/after shown (verification.csv Part B has data)

---

**Ready to submit?** Upload this file + evidence folder to Gradescope by end of Week 10.

**Estimated completion time**: 12-15 hours across Weeks 9-10

**Good luck!** 🎯