# Diseno de skills personalizadas

## 1. Diario de aprendizaje

**Que hace:** convierte puntos de aprendizaje del dia en una entrada ordenada
y la guarda en un Google Doc.

**Input:** fecha, temas aprendidos, ejemplos y preguntas pendientes. El agente
ya conoce el estilo conciso de Alfonso y debe usar la cuenta de prueba conectada.

**Buen output:** un documento titulado `Diario de aprendizaje - YYYY-MM-DD`
con secciones Resumen, Conceptos, Ejemplos y Preguntas abiertas, mas el enlace
al documento enviado por Telegram.

## 2. Plan de semana

**Que hace:** transforma objetivos y compromisos en un plan priorizado, lo
guarda en Google Docs y crea bloques de revision en Google Calendar.

**Input:** semana objetivo, objetivos, restricciones de horario y duracion de
las sesiones. El agente debe preguntar por fecha, zona horaria o duracion si
faltan datos.

**Buen output:** un documento con prioridades, sesiones y criterios de exito,
ademas de eventos creados con titulo, horario y enlace al documento en la
descripcion. El agente confirma cada enlace por Telegram.

## Restricciones comunes

- No usar cuentas personales ni mostrar credenciales.
- No crear eventos si falta fecha u hora.
- Verificar la respuesta de Google Docs y Calendar antes de confirmar.