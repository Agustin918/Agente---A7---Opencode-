# CRM — Estado y Gestión de Leads

> Actualizado: 03/08/2026

## El CRM
- **Stack:** Next.js 16 + Supabase (Postgres) + Vercel
- **URL:** a7-crm.vercel.app
- **Repo local:** `/Users/agustin/Documents/a7-crm/` (Mac) / `~\Documents\a7-crm\` (Windows)
- **Estructura:** Kanban (`/`), Dashboard (`/dashboard`), Leads (`/leads`), Detalle (`/leads/[id]`), Prioridades (`/prioridades`), Secuencias (`/secuencias`), Seguimientos (`/seguimientos`)

## Schema de la base (resumen)
- **Tabla `leads`:** id, full_name, phone, email, facebook_form_data (jsonb), ad_name, campaign_name, source, stage, temperature, notes (jsonb), next_action_text, next_action_date, revenue, created_at, updated_at
- **Etapas:** lead_entrante → conversacion_iniciada → llamada_realizada → reunion_encuentro → presupuesto_enviado → cerrado_ganado / cerrado_perdido
- **Temperatura:** frio / tibio / caliente
- **Tabla `lead_activity_log`:** historial de cambios de etapa por lead
- **Tabla `settings`:** key/value (guarda el token de Meta Ads)

## Bugs arreglados
- **"Invalid time value" en LeadDetail.tsx (línea 319):** dos leads (Lina Gorosito, Amalia Paz) tenían notas sin campo `created_at`. Se arregló en código para mostrar "—" si no hay created_at. Se creó error boundary (`/src/app/leads/[id]/error.tsx`). Deploy a Vercel exitoso.
- El script `fix_notes.js` convirtió notas de string a array pero sin created_at — eso originó el bug.

## Limpieza de duplicados (31/07)
Se detectaron y eliminaron 5 leads duplicados (mismo teléfono/email/nombre):
- Sabrina Morantes (dup 29/7) — original 21/7 en conversación
- Roberto Sanchez (dup 29/7)
- Lina Gorosito (dup 29/7)
- Sofía Young (dup 29/7, nombre con caracteres raros "sσғɪ ʏσᴜɴɢ")
- Amalia Paz (dup 17/7)

**Resultado:** 71 → 66 leads.
**Causa raíz:** la campaña de estáticos trajo leads repetidos el 29/7 y el 3/8. Los duplicados entran de nuevo cuando la persona vuelve a llenar el formulario o Meta duplica.

## Scripts de utilidad (en `/Users/agustin/Documents/a7-crm/`)
- `check_duplicates.js` — detecta duplicados por teléfono/email/nombre
- `delete_duplicates.js` — elimina duplicados
- `fix_notes.js` — convierte notes de string a array
- `scripts/update-crm.mjs` — actualiza CRM vía Supabase

## Leads en `lead_entrante` esperando contacto (3/08)
| # | Nombre | Teléfono | Proyecto | Presupuesto | Plazo | Prioridad |
|---|---|---|---|---|---|---|
| 1 | Sofía Young | +54 9 11 6999-7123 | Ya tiene croquis, 150-300m² | <150k | 3-6 meses | 🔴 Alta (espera desde 24/7) |
| 2 | Roberto Sánchez | +54 341 371-0556 | Casa para escapadas, <150m² | <150k | 3-6 meses | 🔴 Alta (espera desde 24/7) |
| 3 | Nora Elisabet | +54 11 4401-4545 | 1 planta 4 ambientes | — | **INMEDIATO** | 🟠 URGENTE |
| 4 | Sebastián | +54 9 11 3260-0875 | — | **150-250k** | — | 🟠 Mejor ticket |
| 5 | Juan Labado | +54 11 5414-6496 | Casa verano 4 dorm, terreno | — | 3-6 meses | 🟡 |
| 6 | Cecilia Aquino | +54 11 5595-7663 | Casa 1 planta 2-3 dorm, terreno | <150k | 3-6 meses | 🟡 |
| 7 | María de los Angeles | +54 11 3772-1982 | Mudarse a vivienda menor, en compra | <150k | 3-6 meses | 🟡 |
| 8 | Nancy Mouras | +54 11 3329-7420 | Terreno propio | <150k | 3-6 meses | 🟡 |

## Plan de contacto (chip nuevo WhatsApp)
| Día | Contactar |
|---|---|
| Día 1 (3/08) | Sofía + Roberto (ya esperan 9 días) |
| Día 2 | Nora (urgente) + Sebastián (mejor ticket) |
| Día 3 | Juan + Cecilia |
| Día 4 | María + Nancy |

**Máximo 2 por día.** Espaciar para no marcar el número nuevo. Mensajes cortos, individualizados, sin precios ni portfolio (según Guía de Contacto).

## Estado de otros leads (histórico)
- **Uriel** → 🔥 respondió: oficina/gym 36m² (13/7)
- **Paola Arcana** → 🔥 dijo "sábado a la mañana"
- **Jose Frustachi** → 🔥 confirmó reunión
- **Mariano Grandi** → respondió "gracias", esperando confirmación
- **Tincho** → meet link 13/7 17hs enviado
- **Carola (Las Banderitas)** → presupuesto enviado
- **Paula Marzia** → cerrado (construcción modular, no era perfil)
- **A D R I A N A (Miami)** → nutrición automática
- **Maxi Sandiyu** → frío, recuperándose
