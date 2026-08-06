# Meta Ads — Estado de Campañas y Resultados

> Actualizado: 31/07/2026

## Cuentas publicitarias
- **act_773909325186389** — A7 Arquitectura ($45k gastados históricamente)
- **act_3003360063165090** — Asiete Arq ($12k gastados)
- **Form leads:** ID `1820003382294099`
- **Token:** guardado en Supabase tabla `settings`, refresca cada ~2h

## Campaña activa
- **Nombre:** "CBO - seg abierta - HyM 30/60 - Clientes potenciales"
- **Presupuesto:** $16/día (CBO — Meta reparte entre los adsets)
- **Objetivo:** Clientes potenciales (leads)

## Ad Sets
| Ad Set | Presupuesto | CPL | Estado |
|---|---|---|---|
| Estáticos | $10/día | $10.55 | 🟢 ACTIVO |
| Reels | $6/día | $12.14 | 🟢 ACTIVO |

## Estado de los anuncios (última revisión 31/07)

### Ad Set de Reels — ACTIVO
| Anuncio | Estado | Gasto (30d) | CPM | CTR | CPC | Frecuencia | Leads | Costo/Lead | Rol |
|---|---|---|---|---|---|---|---|---|---|
| **Reel - 1** | 🟢 ACTIVO | $21.24 | $13.62 | **2.95%** | **$0.46** | 1.59 | 0 | — | Atrae desconocidos (ToFu) |
| **Reel - 2** | 🟢 ACTIVO | $45.64 | $12.29 | 2.05% | $0.60 | 1.60 | **3** | **$15.21** | Convierte (el único con leads) |
| Reel - 3 | 🔴 PAUSED | $3.95 | $12.66 | 1.92% | $0.66 | 1.12 | 0 | — | Apagado |
| Reel - 4 | 🔴 PAUSED | $41.99 | $10.29 | 1.20% | $0.86 | 1.77 | 0 | — | Apagado (quemaba plata sin leads) |

### Ad Set de Estáticos — ACTIVO
| Anuncio | Gasto (30d) | CPM | CTR | CPC | Leads | Costo/Lead | Nota |
|---|---|---|---|---|---|---|---|
| **Estatico - 3** | $207.17 | **$6.37** | **3.51%** | **$0.18** | **12** | **$17.26** | MEJOR estático |
| **Estatico - 2 + CTA** | $64.03 | $6.57 | 3.25% | $0.20 | **5** | **$12.81** | Mejor costo/lead |
| Estatico - 2 | $18.23 | $7.99 | 2.85% | $0.28 | 0 | — | |
| Estatico - 4 | $3.59 | $7.57 | 0.63% | $1.20 | 0 | — | |
| Estatico - 5 | — | — | — | — | — | — | Activo, sin datos aún |
| Estatico - 6 | — | — | — | — | — | — | Activo |
| Estatico - 7 | — | — | — | — | — | — | Activo |
| Estatico - 8 | — | — | — | — | — | — | Activo |
| Estatico - 3 + CTA 2.0 | — | — | — | — | — | — | PAUSED |

## Decisiones tomadas (31/07)
1. **Se apagaron los reels que no rendían** (Reel 3 y Reel 4 — el 4 gastó $42 sin un solo lead).
2. **Se dejaron activos Reel 1 + Reel 2** (recomendación de los libros de marketing digital: mínimo 2-3 creativos, uno que atrae = ToFu y uno que convierte).
3. **Reel 2 arrancó lento post-reactivación** — en los primeros 7 días gastó solo $1.69. La campaña total gastó $42/7días pero los estáticos se llevaron $30.
4. **Decisión:** darle 48hs al Reel 2 para que Meta le asigne presupuesto. Si no gasta en 2-3 días, separarlo en su propio adset con presupuesto propio.

## Qué dicen los libros de marketing (NotebookLM)
- **Los reels son TOP OF FUNNEL** (atraer desconocidos, generar confianza). **Los estáticos son BOTTOM** (convertir a los que ya te conocen). NO apagar todos los reels o el embudo se seca.
- Antes de apagar un reel, mirar: **CPM bajo + frecuencia ~1.1** (buena prospección), **hook rate ≥ 30%** (frena el scroll). Solo apagar si tras 7-14 días: hook <25% Y retención <15% Y empeora el conjunto.
- **Método 322:** 3 creativos + 2 textos + 2 titulares en un flex ad. No mezclar formatos.
- Escalar presupuesto **gradualmente (20% cada 3 días)**, nunca de golpe.
- En arquitectura (alto ticket), los reels además **filtran curiosos sin plata**.

## Notas técnicas
- El adset de reels quedó PAUSED en un momento y no podía reactivarse: Meta rechazaba porque el **límite de gasto mínimo de los conjuntos superaba el presupuesto de campaña** ($16/día). Se resolvió al reactivar los ads individuales.
- Los leads nuevos del 3/8 vinieron todos de los adsets de estáticos (ad_ids 120248069000690124, 120249792405900124, 120249792405910124).
