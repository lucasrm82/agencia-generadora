---
name: handoff-protocolo
description: Use cuando un trabajo es demasiado grande para una sola sesión de subagente. Divide en paquetes de trabajo con plan.md, cada subagente cierra con handoff.md y el siguiente retoma leyendo solo el handoff.
---

# Protocolo handoff (trabajos grandes)

Los archivos son la memoria compartida; los subagentes no comparten conversación.

## Procedimiento del director
1. Divide el trabajo en PAQUETES (máx. lo que un empleado termina en una sesión). Cada paquete: objetivo, entradas (rutas), salidas (rutas) y DoD parcial.
2. Crea memoria/trabajos/<id>/plan.md: tabla de paquetes con estado (pendiente / en curso / hecho / bloqueado).
3. Delega paquete a paquete, en secuencia. Entre tandas, actualiza plan.md con los resúmenes devueltos.

## Plantilla plan.md
````markdown
# Plan — <id>

| # | Paquete | Entradas | Salidas | Estado |
|---|---|---|---|---|
| 1 | ... | ... | ... | hecho |
````

## Plantilla handoff.md (la escribe el empleado al cerrar)
````markdown
# Handoff — <id> paquete <n>

- Estado: completado | parcial | bloqueado
- Decisiones: <qué y por qué>
- Artefactos: <rutas en salida/<id>/>
- DoD: <criterio → hecho/no hecho>
- Pendientes: <qué queda y quién lo retoma>
- Siguiente paso recomendado: <...>
````

## Regla de oro
El siguiente subagente lee SOLO: encargo, su expediente, el handoff del paquete anterior y los artefactos que su paquete consume. Nunca el historial completo.
