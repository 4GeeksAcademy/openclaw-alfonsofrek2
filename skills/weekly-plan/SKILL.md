---
name: weekly-plan
description: "When Alfonso asks for a weekly study plan, create a prioritized Google Doc and schedule review blocks in Google Calendar through Zapier MCP."
user-invocable: true
---

# Plan de semana

1. Recoge la semana, objetivos, compromisos, restricciones, zona horaria y
   duracion de cada sesion. Pregunta solo por los datos que falten.
2. Divide los objetivos en prioridades y sesiones pequenas. No programes mas de
   tres bloques sin confirmacion cuando el usuario no indique una cantidad.
3. Crea primero el documento con `execute_zapier_write_action`, usando
   `GoogleDocsV2CLIAPI`, accion `newtxtdocument`, titulo
   `Plan semanal - YYYY-MM-DD` y el plan como `file`.
4. Verifica el documento y usa su enlace en la descripcion de cada evento.
5. Inspecciona la accion `detailed_event` de `GoogleCalendarCLIAPI`, resuelve el
   calendario dinamico si hace falta y crea cada bloque con `summary`,
   `start__dateTime`, `end__dateTime`, `description` y `calendarid`.
6. Verifica cada respuesta de Calendar y envia por Telegram el enlace del Doc y
   el resumen de eventos creados.

Pide confirmacion antes de crear eventos si hay ambiguedad horaria. No declares
que el plan esta completado si alguna escritura externa fallo.