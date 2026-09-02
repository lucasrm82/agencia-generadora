# Agencia Generadora

Una AGENCIA de empleados virtuales IA que funciona sobre opencode. El usuario habla solo con el **director**, que orquesta el trabajo del resto de la agencia (empleados, revisor, reclutador) y la mantiene en mejora continua.

## Uso rápido
1. Abre opencode en esta carpeta.
2. Habla con el agente **director** (es el agente por defecto). Encárgale responsabilidades, funciones, objetivos, contexto, entregables y criterios de "completado". La agencia se adapta sola y crea los recursos que necesite.
3. Comandos disponibles:
   - `/encargo <trabajo>` — encarga un trabajo completo (intake → ejecución → revisión → entrega → mejora).
   - `/constituir` — (re)constituye la agencia: carta constitucional y recursos iniciales.
   - `/dotacion` — inventario de la agencia (empleados, skills, trabajos activos, estado).

## Primer despliegue (repo clonado)
1. Clona este repo y abre opencode en la carpeta clonada.
2. Ejecuta `/constituir`: el director te entrevistará (contexto, responsabilidades, funciones, objetivos, entregables, límites, directrices y procedimientos) y creará todos los recursos iniciales de forma completa.
3. Opcional: configura tu proxy LiteLLM en `opencode.jsonc` (bloque TODO comentado) y reinicia opencode.

## Cómo funciona
- Los agentes son empleados con expediente (`plantilla/empleados/`) y competencias (skills en `.opencode/skills/`, cargadas bajo demanda).
- Cada trabajo queda en `memoria/trabajos/<id>/` con encargo, contrato RACI y plan; los entregables van a `salida/<id>/`.
- La agencia se auto-mejora: consolida lecciones, actualiza expedientes, skills, procedimientos (SoP) y directrices, construye herramientas y commitea sus cambios automáticamente.
- Límites: la agencia respeta siempre `constitucion/limites.md`; si un trabajo excede un límite, te consulta antes de seguir.

## Estructura
- `constitucion/` — carta evolutiva: contexto, responsabilidades, funciones, objetivos, entregables, límites, directrices (funcionales/técnicas) y procedimientos SoP.
- `plantilla/empleados/` — expedientes de empleados.
- `herramientas/` — scripts y herramientas construidos por la agencia.
- `memoria/` — trabajos, feedback, lecciones y estado del ciclo de vida.
- `salida/` — entregables por trabajo.
- `.opencode/` — agentes, skills y comandos de la agencia.

## Notas
- Tras crear o modificar agentes, skills o comandos, reinicia opencode para que se activen.
- Los cambios de conocimiento se commitean automáticamente; los de alto riesgo (config, permisos, modelos, MCP) requieren tu aprobación.
