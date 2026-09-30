---
name: 4geeks-projects
description: "When Alfonso asks which projects are assigned to him in 4Geeks, list his assigned PROJECT tasks and their current statuses."
user-invocable: true
---

# Proyectos asignados

Use the configured secret `BREATHECODE_STUDENT_TOKEN` and call only the
assignments collection endpoint:

```sh
curl --fail-with-body --silent --show-error \
  -H "Authorization: Token ${BREATHECODE_STUDENT_TOKEN}" \
  "${BREATHECODE_API_BASE_URL:-https://breathecode.herokuapp.com}/v1/assignment/user/me/task?task_type=PROJECT&limit=100"
```

Return a compact table with project title, status, cohort when available, and
delivery/review dates. Do not claim a project is missing when pagination has
not been exhausted.