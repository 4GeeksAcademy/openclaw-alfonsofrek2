# Registro de skills 4Geeks

## Seguridad comun

Todas las skills usan `BREATHECODE_STUDENT_TOKEN` desde el mecanismo de secretos
de OpenClaw y la cabecera `Authorization: Token ...`. El token no se guarda en
este archivo, en una skill, en una captura ni en Git. La base URL configurable es
`BREATHECODE_API_BASE_URL` y por defecto apunta a `https://breathecode.herokuapp.com`.

## Skill 1 - Autenticar

- Prompt conversacional: "Quiero que verifiques si mi cuenta de 4Geeks sigue conectada y si mi sesion es valida."
- Skill: `skills/4geeks-authenticate/SKILL.md`
- Endpoint: `GET /v1/admissions/user/me`
- Prueba: pendiente de ejecutar con el token de estudiante configurado de forma segura.

## Skill 2 - Obtener mis proyectos

- Prompt conversacional: "Muestrame los proyectos que tengo asignados y el estado de cada uno."
- Skill: `skills/4geeks-projects/SKILL.md`
- Endpoint: `GET /v1/assignment/user/me/task?task_type=PROJECT`
- Prueba: pendiente de ejecutar con una cuenta de estudiante autenticada.

## Skill 3 - Obtener trabajo pendiente

- Prompt conversacional: "Que me falta por entregar en el curso?"
- Skill: `skills/4geeks-pending-work/SKILL.md`
- Endpoint: `GET /v1/assignment/user/me/task?task_status=PENDING`
- Prueba: pendiente de ejecutar con una cuenta de estudiante autenticada.

## Skill 4 - Obtener resumen de progreso

- Prompt conversacional: "Que tan avanzado estoy en el curso? Resume mi actividad reciente."
- Skill: `skills/4geeks-progress-summary/SKILL.md`
- Endpoint: `GET /v1/activity/me`
- Prueba: pendiente de ejecutar con una cuenta de estudiante autenticada.

## Skill 5 - Certificados

- Prompt conversacional: "Que certificados de 4Geeks tengo disponibles?"
- Skill: `skills/4geeks-certificates/SKILL.md`
- Endpoint: `GET /v1/certificate/`
- Prueba: pendiente de ejecutar con una cuenta de estudiante autenticada.

## Skill 6 - Eventos proximos

- Prompt conversacional: "Que eventos proximos de 4Geeks deberia tener en cuenta?"
- Skill: `skills/4geeks-events/SKILL.md`
- Endpoint: `GET /v1/events/all?upcoming=true`
- Prueba: pendiente de ejecutar con una cuenta de estudiante autenticada.

## Conversacion de descubrimiento

OpenClaw recomendo separar autenticacion, proyectos, pendientes y actividad en
skills independientes, y anadir certificados y eventos como extensiones. Esa
separacion mantiene una responsabilidad por endpoint y evita mezclar lecturas
con entregas o cambios de datos.