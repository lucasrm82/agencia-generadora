---
name: intake-encargo
description: Use cuando el director recibe una petición de trabajo del usuario. Convierte objetivo, contexto, entregables y criterios de completado (DoD) en memoria/trabajos/<id>/encargo.md con plantilla fija; pregunta solo si falta información crítica.
---

# Intake de encargos

## Pasos
1. Asigna ID: siguiente número de la serie en memoria/trabajos/ (T-001, T-002, ...).
2. Crea memoria/trabajos/<id>/encargo.md con la plantilla fija de abajo.
3. Si falta información CRÍTICA (objetivo, entregable o DoD ambiguos), pregunta al usuario con la tool question: una sola ronda, máximo 4 preguntas. Lo demás: documenta supuestos en el encargo y continúa.
4. Registra los límites aplicables (de constitucion/limites.md) en el campo Límites.

## Plantilla encargo.md
````markdown
# Encargo <id>: <título>

- Solicitado por: <usuario>
- Fecha: <fecha>

## Objetivo
<qué se quiere lograr, en una frase>

## Contexto
<información y recursos relevantes; punteros, no copias>

## Entregables
1. <entregable> → salida/<id>/

## Criterios de aceptación (DoD)
- [ ] <criterio verificable y concreto>

## Límites aplicables
<presupuesto, rondas, alcance, prohibiciones>

## Supuestos
<decisiones tomadas ante información faltante>
````
