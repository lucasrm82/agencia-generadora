---
name: constitucion-agencia
description: Use al desplegar la agencia en un repo clonado o cuando el usuario pida (re)constituirla. Entrevista la carta (contexto, responsabilidades, funciones, objetivos, entregables, límites), la escribe en constitucion/ y crea todos los recursos iniciales.
---

# Constitución de la agencia

## 1. Entrevista de la carta (en orden, con la tool question)
- CONTEXTO: quién es el cliente, qué hace, entorno de trabajo.
- RESPONSABILIDADES: de qué responde la agencia.
- FUNCIONES: qué funciones cumple.
- OBJETIVOS: qué objetivos persigue y cómo se medirán.
- ENTREGABLES: qué entregables produce y formatos esperados.
- LÍMITES: presupuesto por trabajo, rondas máximas, alcance permitido/prohibido, nivel de autonomía (qué se hace sin preguntar).

## 2. Carta
Escribe constitucion/{contexto,responsabilidades,funciones,objetivos,entregables,limites}.md: compactos, en listas. límites.md con valores concretos y medibles.

## 3. Sprint de recursos iniciales (completo y óptimo)
- Fichas de empleados necesarias (plantilla/empleados/), derivadas de las funciones.
- Skills de dominio necesarias (.opencode/skills/), derivadas de entregables y funciones.
- Workflows (comandos) si el usuario lo pide (requieren reinicio de opencode).
- Propón al usuario cambios de config (modelos por rol, permisos) con justificación; no los apliques sin aprobación.

## 4. Cierre
- memoria/estado.md → estado: operando.
- Commit del conocimiento creado (mensaje: `agencia: constitución inicial`).
- Recuerda al usuario reiniciar opencode si se crearon skills/agentes/comandos.

## Reconstitución (estado evolutivo)
Si cambió la carta (contexto, objetivos, límites...): entrevista solo las secciones afectadas, reescribe esos archivos y reconstituye SOLO los recursos impactados. Estado → operando de nuevo.
