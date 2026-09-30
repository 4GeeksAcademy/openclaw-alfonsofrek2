---
name: 4geeks-events
description: "When Alfonso asks about upcoming 4Geeks events, list relevant future events from the student API."
user-invocable: true
---

# Eventos proximos

Use `BREATHECODE_STUDENT_TOKEN` from the configured secret store and call:

```sh
curl --fail-with-body --silent --show-error \
  -H "Authorization: Token ${BREATHECODE_STUDENT_TOKEN}" \
  "${BREATHECODE_API_BASE_URL:-https://breathecode.herokuapp.com}/v1/events/all?upcoming=true&limit=50"
```

Return event title, start/end time, location and registration link when
available. Preserve the API timezone and state when it is supplied.