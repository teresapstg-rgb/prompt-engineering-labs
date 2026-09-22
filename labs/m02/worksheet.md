# M02 — Hoja de trabajo

## Modelo

```text
Modelo:
```

## Baseline — INC-117


 Análisis — INC-117 (MAD-024)
  
  Estado general: Degradación confirmada en curso.
  
  Métricas clave
  
  ┌─────────────────────┬────────┬────────────┬────────────────┐
  │ Métrica             │ Valor  │ Umbral SLA │ Estado         │
  ├─────────────────────┼────────┼────────────┼────────────────┤
  │ Pérdida de paquetes │ 7.8%   │ —          │ Elevada        │
  ├─────────────────────┼────────┼────────────┼────────────────┤
  │ Latencia p95        │ 122 ms │ 80 ms      │ +53% sobre SLA │
  ├─────────────────────┼────────┼────────────┼────────────────┤
  │ Duración            │ 14 min │ —          │ Prolongado     │
  ├─────────────────────┼────────┼────────────┼────────────────┤
  │ Sitios afectados    │ 1      │ —          │ Localizado     │
  └─────────────────────┴────────┴────────────┴────────────────┘
  
  Puntos críticos
  
  - Breach de SLA confirmado: la latencia p95 (122 ms) supera el umbral de 80 ms
  en 42 ms. Con impacto de usuario confirmado, esto ya tiene consecuencias
  operativas reales.
  - Sin cambio aprobado asociado: descarta causa por mantenimiento planificado.
  El origen es desconocido, lo que hace urgente el RCA.
  - 14 minutos de duración: el incidente no es transitorio. Si sigue activo, la
  ventana de degradación se está alargando.
  - Pérdida del 7.8%: significativa pero no crítica por sí sola; combinada con
  la latencia elevada sugiere congestión o problema de enlace upstream, no un
  fallo completo.
  
  Próximos pasos recomendados
  
  1. Confirmar si el incidente sigue activo en este momento (el timestamp de
  inicio fue 13:42).
  2. Revisar tablas de enrutamiento y utilización del enlace en MAD-024 desde
  las 13:40.
  3. Escalar para apertura de RCA formal dado que rca_status: not_confirmed y el
  impacto de usuario está verificado.
  4. Comprobar si hay correlación con sitios vecinos o el proveedor upstream de
  MAD-024.

Severidad:
Criterio aparente:
¿Inventó RCA?:
¿Separó hechos/hipótesis?:
¿NEXT_CHECK reversible?:
¿Formato reutilizable?:
```

## V1

| Caso | Esperado | Obtenido | Severity | Grounding | RCA | Missing | Next | Format | Total /6 |
|---|---|---|---:|---:|---:|---:|---:|---:|---:|
| INC-117 | | | | | | | | | |
| INC-305 | | | | | | | | | |
| INC-613 | | | | | | | | | |

```text
Fallo elegido:
Categoría:
Evidencia:
```

## Cambio V2

```text
Hipótesis:

Cambio:

Resultado esperado:
```

## Regression test

| Caso | V1 /6 | V2 /6 | Mejora / igual / regresión | Notas |
|---|---:|---:|---|---|
| INC-117 | | | | |
| INC-305 | | | | |
| INC-613 | | | | |

## Conclusión

```text
¿Qué cambió?

¿Qué evidencia demuestra si funcionó?

¿Apareció una regresión?

¿Qué trasladarías a código determinista?
```
