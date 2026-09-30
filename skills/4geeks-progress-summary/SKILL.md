---
name: 4geeks-progress-summary
description: "When Alfonso asks how far along he is in 4Geeks, summarize his learning activity for an optional date range."
user-invocable: true
---

# Resumen de progreso

Use `BREATHECODE_STUDENT_TOKEN` from the configured secret store. Call only the
activity endpoint, adding `date_start` and `date_end` when Alfonso provides a
range:

```sh
curl --fail-with-body --silent --show-error \
  -H "Authorization: Token ${BREATHECODE_STUDENT_TOKEN}" \
  "${BREATHECODE_API_BASE_URL:-https://breathecode.herokuapp.com}/v1/activity/me"
```

Summarize the returned activity, completed work, time or exercise counts, and
the period covered. Do not invent a percentage when the API does not provide a
total denominator.