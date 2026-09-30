---
name: 4geeks-certificates
description: "When Alfonso asks which 4Geeks certificates he has earned, list the certificates returned for his account."
user-invocable: true
---

# Certificados

Use `BREATHECODE_STUDENT_TOKEN` from the configured secret store and call:

```sh
curl --fail-with-body --silent --show-error \
  -H "Authorization: Token ${BREATHECODE_STUDENT_TOKEN}" \
  "${BREATHECODE_API_BASE_URL:-https://breathecode.herokuapp.com}/v1/certificate/"
```

Return certificate name, cohort, issue date and public URL/token only when
returned. Never expose the student authentication token.