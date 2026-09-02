---
name: constitucion-agencia
description: Use al desplegar la agencia en un repo clonado o cuando el usuario pida (re)constituirla. Entrevista la carta (contexto, responsabilidades, funciones, objetivos, entregables, límites, directrices y procedimientos SoP), la escribe en constitucion/ y crea todos los recursos iniciales.
---

# Constitución de la agencia

## 1. Entrevista de la carta (en orden, con la tool question)
- CONTEXTO: quién es el cliente, qué hace, entorno de trabajo.
- RESPONSABILIDADES: de qué responde la agencia.
- FUNCIONES: qué funciones cumple.
- OBJETIVOS: qué objetivos persigue y cómo se medirán.
- ENTREGABLES: qué entregables produce y formatos esperados.
- LÍMITES: presupuesto por trabajo, rondas máximas, alcance permitido/prohibido, nivel de autonomía (qué se hace sin preguntar).
- DIRECTRICES: reglas funcionales (cómo trabajar, estilo, formato) y técnicas (stack, convenciones de código, herramientas). Las mantiene el director de forma evolutiva.
- PROCEDIMIENTOS (SoP): cómo interactuar con el usuario (frecuencia de reportes, formato de entregas, cuándo preguntar) y cómo ejecutar con los agentes (delegación, revisión, handoffs).

## 2. Carta (constitucion/)
Escribe, compactos y en listas:
- contexto.md, responsabilidades.md, funciones.md, objetivos.md, entregables.md, limites.md (valores concretos y medibles).
- directrices.md: funcionales y técnicas (sección funcional + sección técnica).
- procedimientos/sop-usuario.md: SoP de interacción con el usuario.
- procedimientos/sop-ejecucion.md: SoP de ejecución con los agentes (ciclo operativo, dotación, RACI, revisión, handoff, mejora).

## 3. Sprint de recursos iniciales (completo y óptimo)
- Fichas de empleados necesarias (plantilla/empleados/), derivadas de las funciones.
- Skills de dominio necesarias (.opencode/skills/), derivadas de entregables y funciones.
- Herramientas (scripts) si las funciones las requieren (herramientas/).
- Workflows (comandos) si el usuario lo pide (requieren reinicio de opencode).
- Propón al usuario cambios de config (modelos por rol, permisos) con justificación; no los apliques sin aprobación.

## 4. Cierre
- memoria/estado.md → estado: operando.
- Commit del conocimiento creado (mensaje: `agencia: constitución inicial`).
- Recuerda al usuario reiniciar opencode si se crearon skills/agentes/comandos.

## 5. Evolución de la carta
La carta es EVOLUTIVA: directrices y procedimientos (SoP) se actualizan continuamente en mejora-continua cuando la práctica los contradice o el usuario pide cambios.

## Reconstitución (estado evolutivo)
Si cambió la carta (contexto, objetivos, límites...): entrevista solo las secciones afectadas, reescribe esos archivos y reconstituye SOLO los recursos impactados. Estado → operando (o maduro directamente si el impacto fue mínimo).
