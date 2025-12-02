# Metrics CSV Schema

**File**: `data/metrics.csv`

**Columns**:
```csv
ts_iso,session_id,request_id,task_code,step,outcome,ms,http_status,js_mode

ts_iso = ISO 8601 TIMESTAMP
session_id = String (6-12)
Request Id - Unique request identifier
task_code - task identidfier from plan (t1_filter, t2_edit, t3_add, t4_delete)
step - event type (start/stop/success)
outcome - speicfic outcome for errors
ms - duration in milliseconds
https status - status code
js_mode - on (HTMX), off (NO-JS)
