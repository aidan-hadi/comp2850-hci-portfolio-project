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

| Finding | Data Source | Observation (Quote/Timestamp) | WCAG | Impact (1-5) | Inclusion (1-5) | Effort (1-5) | Priority |
|---------|-------------|------------------------------|------|--------------|-----------------|--------------|----------|
| SR errors not announced | pilot-notes P4 | P2: "I didn't hear any error" | 3.3.1 Level A | 5 | 5 | 3 | 7 |
| No task delete confirmation in noJS| pilot-notes P3 T4 |"Literally 1 or two things were wrong I think one of them was with the lack of confirmation with deleting tasks, it felt really weird. | WCAG 2.2.3 | 3 | 4 | 2 | 5 |
|Button is not contrasted enough, espeically in sunlight | pilot-notes P2-debrief|"Though I would love it if the colours used for the selection was more contrasty, sometimes it was hard to see if the item was selected" | WCAG 2.2.1 | 4 | 4 | 1 | 7 |
| No screen reader output for comfirmation of task added read out | pilot-notes.csv - debreif P4 | (asked about confirmation) "Oh yeah, theres no confirmation, and sometimes I missed the text and had to repeat it."| WCAG 3.2.1 | 5 | 4 | 3 | 6  |
| add a check for duplicate tasks | backlog.csv - self found | self-found, no quote avaliable | WCAG 3.3.2 | 2 | 2 | 1 | 3 |

**Priority formula**: (Impact + Inclusion) - Effort

**Top 3 priorities for redesign**:
1. Button selection contrast too low - Priority 8
2. Screen reader confirmations not announced - Priority 7
3. Screen reader error not announced - Priority 7

---

## 3. Pilot Metrics (metrics.csv)


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

**Participant cookies**:
- **P1**: P1_5zljfj
- **P2**: P2_JUisui
- **P3**: P3_1FhG3d
- **P4**: P4_AEh6u7


**Total participants**: n = 4

---

## 4. Implementation Diffs


### Fix 1: Button Selection Contrast is too low

**Addresses finding**: Button selection contrast is very low, its very hard to read what is selected and what isn't, espeically for people who have low vision or cannot see due to facots like sunlight etc.  

**Before** /template/layout/base.peb LINE 52 - 56 :
```html
    /* Override Pico.css button color for WCAG 1.4.3 AA compliance */
    button[type="submit"],
    button {
      color: white !important; /* White text on blue background for better contrast */
    }
```

**After** /template/layout/base.peb LINE 52 - 63:
```html
    /* Override Pico.css button color for WCAG 1.4.3 AA compliance */
    button[type="submit"],
    button {
      color: white !important; /* White text on blue background for better contrast */
    }

    button:hover,
    button[type="submit"]:hover {
      background-color: #519de9ff !important; /* lighter blue hover */
      color: #fff !important;               /* keep text white */
    }
```

**What changed**: I added a button:hover class so the button hover will be lighter than the defualt given by the stylesheet. This is much more effective and properly complies with the WCAG 1.4.3 Guidelines.

**Evidence**: Evidence submitted in the Evidence Folder (fix1-1), the "Apply filter" task is hovered, and there is barely a colour change in the button. (fix1-2) shows the fix, the colour contrast is much better and is more visible.

**Why**: WCAG 1.4.3, we had an issue with accessibility, where, espeically on keyboards, that the highlighted input was not very obvious to the user, espeically for people who are visually impaired or colourblind. 

**Impact**: This fixes this issue by increasing the contrast of buttons that are pressed, by manually overriding the button hover colour. This also (in my opinion) makes the UX nicer, by using a different shade of blue which is nicer on the eyes than the original colour.

---

### Fix 2: Delete Message Confirmation

**Addresses finding**: Fixing the delete message dialogue not appearing in noJS mode 

**Before**: /templates/tasks/_item.peb LINE 11 - 17
```html

<form action="/tasks/{{ task.id }}/delete/" method="get" style="display:inline;"
      hx-delete="/tasks/{{ task.id }}"
      hx-target="#task-{{ task.id }}"
      hx-swap="outerHTML"
      hx-confirm="Delete the task '{{ task.title }}'?">
  <button type="submit" aria-label="Delete task: {{ task.title }}">Delete</button>
</form>
```

**After**:   

/templates/tasks/_item.peb LINE 11 - 17   
This changes the delete button to the confirm page if HTMX is not being used
```html

<form action="/tasks/{{ task.id }}/delete/confirm" method="get" style="display:inline;"
      hx-delete="/tasks/{{ task.id }}"
      hx-target="#task-{{ task.id }}"
      hx-swap="outerHTML"
      hx-confirm="Delete the task '{{ task.title }}'?">
  <button type="submit" aria-label="Delete task: {{ task.title }}">Delete</button>
</form>
```   
/src/main/taskRoutes.kt LINE 180 - 195 (NEW LINES)   
These handle the routing to a new page if HTMX is not used
```kotlin
private suspend fun ApplicationCall.handleDeleteConfirm(store: TaskStore) {
    val id = parameters["id"] ?: run {
        respond(HttpStatusCode.BadRequest, "Missing task ID")
        return
    }

    val task = store.getById(id)
    if (task == null) {
        respond(HttpStatusCode.NotFound, "Task not found")
        return
    }

    // Render a confirmation page template
    val html = renderTemplate("tasks/confirm_delete.peb", mapOf("task" to task.toPebbleContext()))
    respondText(html, ContentType.Text.Html)
}
```   
   
/templates/tasks/confirm_delete.peb   
This is the new page that is shown if HTMX is not being used, and javascript cannot be used. This is needed to send the confirmation message to the user   
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>{% block title %}COMP2850 Task Manager{% endblock %}</title>
  
  {# Pico CSS for baseline accessible styles (WCAG 2.2 AA compliant) #}
  <link rel="stylesheet" href="https://unpkg.com/@picocss/pico@2/css/pico.min.css">
  
  {# HTMX for progressive enhancement #}
  <script src="https://unpkg.com/htmx.org@1.9.12"></script>
  
  <style>
    /* Visually hidden but accessible to screen readers (WCAG 1.3.1) */
    .visually-hidden {
      position: absolute !important;
      height: 1px;
      width: 1px;
      overflow: hidden;
      clip: rect(1px, 1px, 1px, 1px);
      white-space: nowrap;
    }
    
    /* Skip link for keyboard navigation (WCAG 2.4.1) */
    .skip-link {
      position: absolute;
      left: -10000px;
      width: 1px;
      height: 1px;
      overflow: hidden;
    }
    .skip-link:focus {
      position: static;
      width: auto;
      height: auto;
      background: #1976d2;
      color: white;
      padding: 0.5rem 1rem;
      text-decoration: none;
      font-weight: bold;
      z-index: 9999;
    }
    
    /* Pagination styles */
    .pagination {
      display: flex;
      gap: 0.5rem;
      align-items: center;
    }

    /* Override Pico.css button color for WCAG 1.4.3 AA compliance */
    button[type="submit"],
    button {
      color: white !important; /* White text on blue background for better contrast */
    }

    button:hover,
    button[type="submit"]:hover {
      background-color: #519de9ff !important; /* lighter blue hover */
      color: #fff !important;               /* keep text white */
    }
  </style>
</head>
<body>
  {# Include header with navigation and accessibility features #}
  {% include "_layout/_header.peb" %}
  
  {# Main landmark for screen readers (WCAG 1.3.1) #}
  {# tabindex="-1" allows programmatic focus for skip link #}
  <main id="main" class="container" tabindex="-1">
    {% block content %}
    {# Page-specific content goes here #}
    {% endblock %}
  </main>
  {# Include footer with helpful links and session info #}
</body>
</html>

<h2>Confirm deletion</h2>
<p>Are you sure you want to delete "{{ task.title }}"?</p>

<form action="/tasks/{{ task.id }}/delete" method="post"style="display:inline;">
  <button type="submit">Yes, delete</button>
  <a href="/tasks">Cancel</a>
</form>
```

**What changed**: I added a fallback confiramtion page for noJS, as the item would otherwise be deleted instantly

**Evidence**: fix 2-1 shows the fix, a new confirm delete screen for noJS. The functionality with javascript stays the exact same, and works flawlessly.   

**Why**: Because otherwise there is no confirmation in noJS of an item being deleted, and therefore the user can accidently delete items from the list accidentally.

**Impact**: Users who do not have access to javascript and htmx will find it easier to use the program for its intended purposes.

## 5. Verification Results

### Part A: Regression Checklist (20 checks)

**Instructions**: Test all 20 criteria. Mark pass/fail/n/a + add notes.

| Check | Criterion | Level | Result | Notes |
|-------|-----------|-------|--------|-------|
| **Keyboard (5)** | | | | |
| K1 | 2.1.1 All actions keyboard accessible | A | [pass] | Tab and enter buttons worked on every button, tested multiple times with and without JS. No extra buttons or any selections options are present. |
| K2 | 2.4.7 Focus visible | AA | [pass] | Now with the hover colour darker, it is much easier to figure out what is hovered on and not.  |
| K3 | No keyboard traps | A | [pass] | No keyboard traps detected |
| K4 | Logical tab order | A | [pass] | Top to bottom through every button, and if the buttons are next to eachother then it works left to right before going down. It works in the list, making sure every button in the list is ordered first before moving out of the list.|
| K5 | Skip links present | AA | [n/a] | Not implemented |
| **Forms (3)** | | | | |
| F1 | 3.3.2 Labels present | A | [pass] | All inputs have <label>|
| F2 | 3.3.1 Errors identified | A | [pass] | Errors have "role=Alert" as they should have|
| F3 | 4.1.2 Name/role/value | A | [pass] | All form controls have accessible names |
| **Dynamic (3)** | | | | |
| D1 | 4.1.3 Status messages | AA | [pass] | Status div has role=status |
| D2 | Live regions work | AA | [pass] | Tested with NVDA, announces 'Task added' |
| D3 | Focus management | A | [pass] | Focus will always move to the error when an error occurs|
| **No-JS (3)** | | | | |
| N1 | Full feature parity | — | [pass] | All CRUD operations work fine without NO-JS, will be further tested with a new pilot in a later point |
| N2 | POST-Redirect-GET | — | [pass] | Only submitted once, and appears in the CSV|
| N3 | Errors visible | A | [pass] | Errors work in both noJS and HMTX |
| **Visual (3)** | | | | |
| V1 | 1.4.3 Contrast minimum | AA | [pass] | With the colour fix, 7.1:1 via CCA is met. |
| V2 | 1.4.4 Resize text | AA | [pass] | No context lost at small and large zoom levels, and the base zoom level is adequite for most devices and people, with high readability. |
| V3 | 1.4.11 Non-text contrast | AA | [pass] | Indicators are contrasted properly etc.|
| **Semantic (3)** | | | | |
| S1 | 1.3.1 Headings hierarchy | A | [pass] | No out of place headings at all |
| S2 | 2.4.1 Bypass blocks | A | [pass] | Correct blocks are used |
| S3 | 1.1.1 Alt text | A | [pass] | No images in interface, so no Alt text needed for images. |

**Summary**: [20/20 pass], [0/20 fail]
**Critical failures** (if any): No critical failiures which can impact the usability of the program.

---

### Part B: Before/After Comparison

**Instructions**: Compare Week 9 baseline (pre-fix) to Week 10 (post-fix). Show improvement.

| Metric | Before (Week 9, n=X) | After (Week 10, n=Y) | Change | Target Met? |
|--------|----------------------|----------------------|--------|-------------|
| Accidental deletion rate on noJS| [33%] | [0%] | [-33%] | [✅] |
| WCAG [2.2.1] pass | [fail] | [pass] | [-Changed button contrast] | [✅] |

**Re-pilot details**:
## Pilot 5
Date: 2025-06-12 
Participant code: P5 
Session ID: P5_1FHG6  
Variant: Keyboard and NoJS (HTML, keyboard, NoJS)  
### Pretest Notes:   
P5 has already done this before, and will test and comment on the changes.  

### Debrief P5:  
- "I think the new webpage is very good and definitely will help me to not delete random tasks accidentally"
- "Paired with the new button hover colour, I think this will prevent accidentally pressing wrong buttons, submitting blank forms, etc."


**Limitations / Honest reporting**:   

Overall, I think that I did a good job adding small improvements to the program based off feedback. I think that the fixes were complex enough to challenge me, espeically since I have not had much experience coding in HTML before, however simple enough that they only took a couple hours, while having (hopefully) a large impact on users.   



## 6. Evidence Folder Contents

**Instructions**: List all files in your evidence/ folder. Provide context.

### Screenshots

| Filename | What it shows | Context/Link to finding |
|----------|---------------|-------------------------|
| fix1-1.png | The hover without the fix | Fix #1, changing the button contrast to be more visible |
| fix1-2.png | The hover with the fix | Fix #1 verification |
| fix2-1.png | The new fix, with a new confirmation screen for noJS | Fix #2 Verification |

**PII check**:
- [ ✅ ] All screenshots cropped to show only relevant UI
- [ ✅ ] Browser bookmarks/tabs not visible
- [ ✅ ] Participant names/emails blurred or not visible

---

### Pilot Notes

**Instructions**: Attach pilot notes as separate files (P1-notes.md, P2-notes.md, etc.). Summarize key observations here.

**P1** Standard (HTMX, mouse, JS-on):
- **Key observation 1**: "No "no result found" message ever" 
- **Key observation 2**: "It worked well enough that i can navigate the system easily" 

**P2** Keyboard (HTMX, keyboard, JS-on):
- **Key observation 1**: " I thought the system worked well, even though I did not have much past experience using a keyboard as the only input"  
- **Key observation 2**: "Though I would love it if the colours used for the selection was more contrasty, sometimes it was hard to see if the item was selected" 

**P3** noJS (HTMX, mouse, noJS):
- **Key observation 1**: "Literally 1 or two things were wrong I think one of them was with the lack of confirmation with deleting tasks, it felt really weird.  
- **Key observation 2**: "I thought that this was quite easy to use"

**P4** Screen Reader (HTMX, mouse allowed (but keyboard actually used), JS-on) :
- **Key observation 1**: (asked about confirmation) "Oh yeah, theres no confirmation, and sometimes I missed the text and had to repeat it."  
- **Key observation 2**: "It was really hard to visualise the website, but that was expected as I didn't do anything like this before"  

**P5** Keyboard and NoJS (HTML, keyboard, NoJS) (RETEST)  :  
- **Key observation 1**: "I think the new webpage is very good and definitely will help me to not delete random tasks accidentally"  
- **Key observation 2**: "Paired with the new button hover colour, I think this will prevent accidentally pressing wrong buttons, submitting blank forms, etc." 

---

## Evidence Chain Example (Full Trace)

**Instructions**: Pick ONE finding and show complete evidence trail from data → fix → verification.

**Finding selected**: Finding 2, no-JS deletion confirmation missing

**Evidence trail**:
1. **Data**: pilot-notes.md - P3 task T4
2. **Observation**: Confirmation didn't work, and the task was suddenly deleted, and it caught the user off guard
3. **Screenshot**: fix2-2.png shows the confirmation not working, instant transmission back to task screen
4. **WCAG**:
5. **Prioritisation**: findings-table.csv row 2 - Priority score 7 (Impact 5 + Inclusion 5 - Effort 3)
6. **Fix**: assessment.md FIX 2, fixes shown in kotlin and HTMX to make a new results page
7. **Verification**: pilot-retest.md - P5 reverified that the task worked successfully.
8. **Before/after**: error confirmation screen is always shown in noJS
9. **Re-pilot**: - I think the new webpage is very good and definitely will help me to not delete random tasks accidentally

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