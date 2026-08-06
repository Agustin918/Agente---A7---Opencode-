# Contexto Histórico — A7 Arquitectura

> Este documento resume ABSOLUTAMENTE TODO lo que se construyó y decidió. Leerlo al inicio de cada nueva sesión para no perder el hilo.

---

## 1. QUIÉN SOY

- **Nombre:** Agustín Salado
- **Estudio:** A7 Arquitectura (estudio familiar con su papá Nicolás Salado Castro)
- **Rol:** Agustín opera el CRM y el marketing, habla con los leads. El papá es el arquitecto proyectista.
- **Web:** a7studio.lat
- **Instagram:** @a7.arq
- **Ubicación:** Buenos Aires y alrededores (capital, zona norte, San Sebastián, Maschwitz)
- **Perfil:** Estudio de arquitectura residencial y comercial — viviendas unifamiliares, consultorios, oficinas
- **Segundo emprendimiento:** Secret Spot — marca de indumentaria surfwear (proyecto separado, aislado)
- **WhatsApp personal:** +54 9 11 4419 8394

---

## 2. ESTRUCTURA DE TRABAJO

### Proyecto A: A7 Arquitectura (ESTE REPO)
- **Carpeta Mac:** `/Users/agustin/Documents/a7-crm/` (el CRM real)
- **Carpeta Windows:** `~\Documents\OpenCode\estudio-arquitectura\`
- **Git:** https://github.com/Agustin918/Agente---A7---Opencode-
- **Rol del agente:** Project Manager Senior experto en arquitectura, costos, escalabilidad, gestión de obras y clientes
- **Tono:** Profesional, técnico, confiable, español rioplatense, directo

### Proyecto B: Secret Spot (SEPARADO)
- **Git:** https://github.com/Agustin918/Agente---Secret---Opencode
- **Contexto:** Marca surfwear argentina — NO mezclar con arquitectura

---

## 3. STACK REAL (lo que está funcionando hoy)

### CRM
- **Stack:** Next.js 16 (app router) + Supabase (Postgres) + Vercel
- **URL:** a7-crm.vercel.app
- **Repo local:** `/Users/agustin/Documents/a7-crm/`
- **Estructura:** Kanban, Dashboard, Leads, Detalle, Prioridades, Secuencias, Seguimientos
- **Detalle completo:** ver `02-gestion/leads/estado-crm.md`

### Meta Ads
- **Cuentas:** `act_773909325186389` (A7, $45k) y `act_3003360063165090` (Asiete, $12k)
- **Campaña activa:** "CBO - seg abierta - HyM 30/60 - Clientes potenciales" ($16/día)
- **Detalle completo:** ver `01-meta-ads/estado-campanas.md`

### NotebookLM
- **Guía de Contacto Prospectos:** notebook ID `48c6b3f2-936c-4033-b99c-725d93d5348b`
- **Libros Marketing Digital 1:** `8ab4bbd4-af9b-4a3d-b0c4-137288196e2a`
- **Libros Marketing Digital 2:** `0036f575-c4f0-46aa-869d-a5597cbc3dd2`
- CLI: `nlm query notebook <id> "pregunta"`
- **SIEMPRE consultar la Guía antes de sugerir mensajes a leads**

### WhatsApp
- **⚠️ BRIDGE PROHIBIDO — NUNCA ENCENDERLO** (ver `03-whatsapp/historia-y-plan.md`)
- Línea nueva comprada (chip nuevo), en plan de calentamiento
- Solo app oficial

---

## 4. SISTEMA DE MEMORIA ENTRE SESIONES

### "Guardar sesión" / "Terminamos por hoy":
1. Resumir tareas, decisiones y próximos pasos
2. Sobrescribir `memoria.md`
3. `git add .` → `git commit -m "Actualización de memoria"` → `git push`

### "Iniciar sesión" / "Traer cambios":
1. `git pull`
2. Leer `00-contexto/contexto_historico.md` + `memoria.md`
3. Saludar con resumen de dónde se quedaron

---

## 5. REGLAS FUNDACIONALES

### Para ambos proyectos:
- **Regla de Lectura Autónoma:** Usar `python .agents/scripts_lectura/lector_universal.py <ruta>` para leer imágenes/PDFs/DOCX. Nunca decir "no puedo ver eso".
- **Aislamiento de contexto:** Arquitectura NO habla de moda. Moda NO habla de arquitectura.
- **Español rioplatense:** Vos, che, directo.
- **Eficiencia de tokens:** Corto y denso por defecto. "corto" = 3 líneas. "puntual" = bullets. "expande" = explayarse.
- **Organización continua:** Nunca archivos sueltos. Cada nuevo tema = nueva subcarpeta.
- **Si algo no está claro:** Preguntar UNA sola cosa y seguir.

### Para A7 específicamente:
- Lenguaje técnico de construcción, BIM, project management
- Enfoque en procesos, estandarización, eficiencia
- **NO enviar mensajes a leads sin consultar primero** — Agustín los envía manualmente desde su celu
- **Consultar SIEMPRE la Guía de Contacto (NotebookLM)** antes de redactar mensajes
- **No dar precios por mensaje, no mandar portfolio en primer contacto** (regla de la guía)

### Reglas de seguridad
- **NUNCA** subir tokens de Meta Ads, Supabase keys ni el token del bridge a git
- Los secrets viven en `.env.local` (no se sube)
- El token de Meta Ads se guarda en Supabase tabla `settings`, refresca cada ~2h

---

## 6. PRÓXIMOS PASOS PENDIENTES

### Contacto de leads (URGENTE — en curso)
- [ ] Contactar Nora (plazo inmediato) + Sebastián (150-250k) — día 2
- [ ] Contactar Juan + Cecilia — día 3
- [ ] Contactar María + Nancy — día 4
- [ ] Actualizar CRM a medida que respondan

### Marketing
- [ ] Monitorear Reel 2 en 48hs (si no gasta, separarlo en adset propio)
- [ ] Armar reel de "4 fases de proyecto" (guión ya listo)
- [ ] Definir stack de redes sociales (PostPlanify $12/mes recomendado, o Apaya/Storylayer)

### CRM
- [ ] Considerar fix en DB para notas sin created_at (Lina y Amalia — originales quedaron)
- [ ] Evaluar Dewx ($49/mes) o IntoAEC para unificar CRM + WhatsApp + proyectos

### Nota: skills de storytelling instaladas (10)
storytelling-hooks, carousel-narratives, long-form-youtube, titles-and-thumbnails, email-hooks, wireframe-writer, wireframe-reviewer, channel-formula, retention-audit, storytelling-expert

---

*Fin del contexto histórico. Actualizado: 03/08/2026.*
