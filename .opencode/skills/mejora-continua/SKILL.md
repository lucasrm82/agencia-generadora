---
name: mejora-continua
description: Use al cerrar cada trabajo o tras feedback consolidado. Consolida lecciones.md, actualiza fichas y skills, y commitea automáticamente el conocimiento de la agencia. Cambios de alto riesgo: aprobación del usuario.
---

# Mejora continua

## Al cerrar cada trabajo
1. LECCIONES: añade a memoria/lecciones.md solo lecciones generalizables (formato: fecha, título, trabajo origen, frase accionable). No dupliques lecciones existentes; refuérzalas con nueva evidencia.
2. FICHAS: actualiza la ficha del empleado participante: KPI (trabajos, nota del revisor) y "Historial de evolución" (una línea por cambio).
3. SKILLS: si un proceso falló o costó caro, propón el cambio concreto en la skill correspondiente (o pide al reclutador una nueva).
4. ESTADO: si procede, actualiza memoria/estado.md (p. ej. operando → maduro cuando el feedback correctivo sea mínimo).
5. COMMIT automático del conocimiento:
   `git add plantilla memoria constitucion salida .opencode/skills AGENTS.md`
   `git commit -m "agencia: <resumen breve>"`
   Nunca incluyas secrets ni archivos fuera de la agencia.

## Alto riesgo (requiere aprobación del usuario)
opencode.jsonc, permisos, modelos, MCP y agentes (.opencode/agents/). Propón el cambio con justificación y espera el sí.
