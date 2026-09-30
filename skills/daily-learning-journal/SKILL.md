---
name: daily-learning-journal
description: "When Alfonso shares what he learned today, format it as a concise Spanish learning journal and create a Google Doc through Zapier MCP."
user-invocable: true
---

# Diario de aprendizaje diario

1. Recoge la fecha, los aprendizajes, ejemplos y preguntas pendientes. Si falta
   el contenido principal, pide una lista breve antes de continuar.
2. Organiza el contenido en Markdown o HTML sencillo con estas secciones:
   `Resumen`, `Conceptos`, `Ejemplos`, `Preguntas abiertas` y `Siguiente paso`.
3. Inspecciona la accion de Google Docs antes de escribir. Usa
   `GoogleDocsV2CLIAPI` y la accion `newtxtdocument`; el titulo debe ser
   `Diario de aprendizaje - YYYY-MM-DD` y `file` debe contener la entrada.
4. Ejecuta la escritura con `execute_zapier_write_action` y confirma que la
   respuesta contiene un documento creado o un enlace valido.
5. Responde por Telegram con el titulo, un resumen de una frase y el enlace.

No inventes aprendizajes, enlaces ni resultados. Si la escritura falla, informa
del error y no confirmes que el documento existe.