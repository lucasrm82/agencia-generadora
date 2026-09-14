---
name: mejora-continua
description: Use al cerrar cada trabajo o tras feedback consolidado. Audita la carta, consolida lecciones y conocimiento de dominio, actualiza fichas, procedimientos SoP y normas operativas, vigila el tamaño de los ficheros de memoria, propone (con confirmación previa) skills nuevas o mejoradas, tools de plugin e integraciones MCP/API, y commitea el conocimiento. Cambios de alto riesgo: aprobación del usuario.
---

# Mejora continua

## Al cerrar cada trabajo
1. AUDITORÍA DE CARTA (obligatoria, 1 línea): ¿algo de constitucion/ quedó desactualizado con lo vivido? Si sí, corrígelo o prográmalo. Cada 10 trabajos: auditoría explícita completa y anota la fecha en memoria/estado.md ("Última auditoría de carta").
2. LECCIONES: añade a memoria/lecciones.md solo lecciones generalizables (formato: fecha, título, trabajo origen, frase accionable). No dupliques; refuerza con nueva evidencia.
3. CONOCIMIENTO DE DOMINIO: lo específico del cliente (glosario, formatos, APIs, esquemas) va a memoria/conocimiento/<tema>.md, compacto. Si se vuelve procedimiento recurrente, promuévelo a la sección de referencia de su skill (capa fría).
4. FICHAS: actualiza la ficha del empleado participante: KPI (trabajos, nota del revisor) y "Historial de evolución" (una línea por cambio).
5. SALUD DE ARCHIVOS (reactiva, sin umbrales fijos): si al trabajar detectas un fichero de memoria que se está volviendo demasiado grande (lecciones.md, conocimiento, fichas, handoffs acumulados), consolídalo en el momento: fusiona duplicados, poda lo obsoleto, generaliza, divide en varios ficheros. Actúa solo cuando el tamaño estorbe.
6. PROCEDIMIENTOS Y SKILLS (proponer, no imponer): si un proceso falló, costó caro, se repite de forma estructurada o una skill tiene un mal funcionamiento o una ampliación útil, PROPÓN la skill nueva o el cambio (qué se gana, coste, riesgo, dónde vive) y espera la confirmación explícita del usuario antes de implementarla. Un detalle vive en un solo sitio: skill = genérico, SoP = del cliente.
7. TOOLS: si una tarea se repite 2-3 veces y es automatizable, propón convertirla en tool de plugin en .opencode/plugin/ (receta abajo) y espera confirmación antes de implementarla. Los scripts de un solo uso viven en salida/<id>/ y no se versionan como tools.
8. INTEGRACIONES: si un trabajo necesita un sistema externo (MCP, API), propón la integración con justificación y coste. Alto riesgo → aprobación del usuario (cambia config).
9. NORMAS OPERATIVAS: mantén constitucion/normas-operativa.md al día (funcionales y técnicas) cuando la práctica lo cambie. La carta es evolutiva. directrices.md (fundamentales) NO se toca: solo la edita el usuario.
10. ESTADO: actualiza memoria/estado.md cuando proceda (operando → maduro si el feedback correctivo es mínimo; maduro → evolutivo si cambia la carta).
11. COMMIT automático del conocimiento:
    `git add plantilla memoria constitucion salida .opencode/skills .opencode/plugin AGENTS.md`
    `git commit -m "agencia: <resumen breve>"`
    Nunca incluyas secrets ni archivos fuera de la agencia.

## Receta: tool de plugin (.opencode/plugin/)
1. Crea <nombre>.ts en .opencode/plugin/ que exporte un Plugin con `tool: { <nombre>: { ... } }` (shape exacto de args/execute en https://opencode.ai/docs/plugins/ y en el skill customize-opencode).
2. Pruébala con `opencode run` antes de darla por buena (es un recurso frío).
3. Avisa al usuario del restart pendiente para activarla.

## Recursos fríos nuevos
Skills, agents, commands y plugins se activan solo al REINICIAR opencode. Si hay que usarlos de inmediato, ejecuta `opencode run "..."` (sesión hija con config fresca). Nunca reinicies ni mates la sesión del usuario; acumula los cambios fríos y avisa del restart pendiente.

## Alto riesgo (requiere aprobación del usuario)
opencode.jsonc, permisos, modelos, MCP, integraciones externas y agentes (.opencode/agents/). Propón el cambio con justificación y espera el sí.
