---
name: 4geeks-pending-work
description: "When Alfonso asks what he still needs to deliver, list only his pending 4Geeks assignments."
user-invocable: true
---

# Trabajo pendiente

Use `BREATHECODE_STUDENT_TOKEN` from the configured secret store and call:

```sh
curl --fail-with-body --silent --show-error \
  -H "Authorization: Token ${BREATHECODE_STUDENT_TOKEN}" \
  "${BREATHECODE_API_BASE_URL:-https://breathecode.herokuapp.com}/v1/assignment/user/me/task?task_status=PENDING&limit=100"
```

Group results by task type and show title, cohort, due date and the next action
when those fields exist. Distinguish an empty API response from an API error.