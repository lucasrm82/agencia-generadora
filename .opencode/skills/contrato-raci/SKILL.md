---
name: contrato-raci
description: Use al iniciar cada trabajo o al cambiar sus recursos. Firma la matriz RACI por recurso en memoria/trabajos/<id>/contrato.md: un solo A (director por defecto), R ejecutor, C revisor, I memoria y usuario.
---

# Contratos RACI

## Reglas
- Un solo A por recurso; por defecto A = director (delegable solo explícitamente y por escrito en el contrato).
- R ejecuta el trabajo; puede haber varios R en recursos distintos.
- C es consultado (típicamente el revisor para los criterios de aceptación).
- I queda informado: memoria de la agencia y usuario (entrega final).
- Si cambian recursos o alcance: actualiza contrato.md y anótalo en el handoff.

## Plantilla contrato.md
````markdown
# Contrato RACI — <id> <título>

| Recurso | R (ejecuta) | A (responde) | C (consultado) | I (informado) |
|---|---|---|---|---|
| <p. ej. entregable principal> | empleado:<nombre> | director | revisor | memoria, usuario |
| <p. ej. criterios de aceptación> | director | director | revisor | memoria |

- Firmado: <fecha>
- Cambios: <fecha y motivo>
````
