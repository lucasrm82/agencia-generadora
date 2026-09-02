---
name: retroalimentacion
description: Use al recibir feedback del usuario o del revisor. Clasifica (bug, mejora, nuevo requisito, lección), guarda el feedback crudo en memoria/feedback/ y enruta cada clase a su destino.
---

# Retroalimentación

## Clasificación y ruta
1. Guarda el feedback crudo en memoria/feedback/<id>-<fecha>.md (texto literal + fuente).
2. Clasifica cada punto:
   - BUG → el entregable incumple el encargo → re-trabajo inmediato (nueva ronda con empleado, respetando límites).
   - MEJORA → forma de trabajar o calidad general → actualiza ficha/skill en mejora-continua.
   - NUEVO REQUISITO → cambia el alcance → nuevo encargo (o revisión del vigente con el usuario).
   - LECCIÓN → conocimiento generalizable → lecciones.md en mejora-continua.
3. Si el feedback es ambiguo, pregunta al usuario una vez (tool question).

## Prudencia
No cambies procesos por un solo dato: consolida patrones (2-3 ocurrencias) antes de modificar fichas o skills.
