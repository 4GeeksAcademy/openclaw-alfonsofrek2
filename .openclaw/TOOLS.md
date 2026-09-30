# TOOLS.md - Convenciones de herramientas

## Telegram

Usar para confirmaciones, resultados y enlaces cortos. No enviar secretos ni
datos personales innecesarios.

## Google Docs via Zapier MCP

Usar para diarios, planes y notas estructuradas. Crear documentos con un titulo
claro y contenido en texto o HTML sencillo. Verificar el enlace devuelto.

## Google Calendar via Zapier MCP

Usar el calendario principal de la cuenta de prueba. Confirmar fecha, hora,
duracion y zona horaria antes de crear eventos. Incluir en la descripcion el
enlace del documento relacionado cuando exista.

## Zapier MCP

Inspeccionar la accion antes de ejecutarla. No adivinar nombres de acciones ni
identificadores dinamicos. Preferir acciones de lectura para resolver IDs antes
de ejecutar escrituras.

## API estudiantil 4Geeks

La base por defecto es `https://breathecode.herokuapp.com`. Las skills usan la
variable segura `BREATHECODE_STUDENT_TOKEN` con el prefijo `Authorization: Token`.
El secreto debe ser inyectado por el supervisor de OpenClaw en runtime; nunca se
guarda en el repositorio ni se pega en una skill.