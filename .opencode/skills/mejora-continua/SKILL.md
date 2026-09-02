---
name: mejora-continua
description: Use al cerrar cada trabajo o tras feedback consolidado. Consolida lecciones, actualiza fichas, skills, procedimientos SoP y directrices, construye o mejora herramientas, propone integraciones MCP/API y commitea el conocimiento. Cambios de alto riesgo: aprobación del usuario.
---

# Mejora continua

## Al cerrar cada trabajo
1. LECCIONES: añade a memoria/lecciones.md solo lecciones generalizables (formato: fecha, título, trabajo origen, frase accionable). No dupliques; refuerza con nueva evidencia.
2. FICHAS: actualiza la ficha del empleado participante: KPI (trabajos, nota del revisor) y "Historial de evolución" (una línea por cambio).
3. PROCEDIMIENTOS Y SKILLS: si un proceso falló o costó caro, corrige la skill correspondiente, el prompt del agente implicado o los SoP de constitucion/procedimientos/ (sop-usuario, sop-ejecucion). Los prompts de .opencode/agents/ se proponen al usuario antes de aplicarlos.
4. HERRAMIENTAS: si una tarea se repite 2-3 veces y es automatizable, construye o mejora un script en herramientas/ (elige el lenguaje adecuado a la tarea). Pruébalo antes de darlo por bueno y documenta su uso en el propio script o en su skill asociada.
5. INTEGRACIONES: si un trabajo necesita un sistema externo (MCP, API), propón la integración con justificación y coste. Alto riesgo → aprobación del usuario (cambia config).
6. DOCUMENTOS DE CONOCIMIENTO: el conocimiento específico de dominio se guarda DENTRO de la skill que lo usa (sección de referencia), no suelto en lecciones.
7. DIRECTRICES: mantén constitucion/directrices.md al día (funcionales y técnicas) cuando la práctica lo cambie. La carta es evolutiva.
8. ESTADO: actualiza memoria/estado.md cuando proceda (p. ej. operando → maduro si el feedback correctivo es mínimo; maduro → evolutivo si cambia la carta).
9. COMMIT automático del conocimiento:
   `git add plantilla memoria constitucion salida herramientas .opencode/skills AGENTS.md`
   `git commit -m "agencia: <resumen breve>"`
   Nunca incluyas secrets ni archivos fuera de la agencia.

## Alto riesgo (requiere aprobación del usuario)
opencode.jsonc, permisos, modelos, MCP, integraciones externas y agentes (.opencode/agents/). Propón el cambio con justificación y espera el sí.
