---
name: 4geeks-authenticate
description: "When Alfonso asks whether his 4Geeks account is connected or his student session is valid, verify it with the current-user endpoint."
user-invocable: true
---

# Autenticar cuenta 4Geeks

Use the configured secret `BREATHECODE_STUDENT_TOKEN`. Never ask the user to
paste it into chat and never include it in output. Call:

```sh
curl --fail-with-body --silent --show-error \
  -H "Authorization: Token ${BREATHECODE_STUDENT_TOKEN}" \
  "${BREATHECODE_API_BASE_URL:-https://breathecode.herokuapp.com}/v1/admissions/user/me"
```

Report only whether authentication succeeded and the user's display name or
email returned by the API. Treat HTTP 401/403 as an invalid or expired token.