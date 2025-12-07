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

Record in `/submission/consent/consent-log.md`:
Date: 2025-10-15 Participant code: P1 Session ID: X7kL9p Consent: Verbal consent givem.

**Opt-out path**: If participant requests deletion:
1. Open `data/metrics.csv`
2. Delete all rows where `session_id=X7kL9p`
3. Note in `consent-log.md`: "Data deleted on request [date]"
