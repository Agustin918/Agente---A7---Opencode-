# Contexto Histórico — Sesión Madre (22/07/2026)

> Este documento resume ABSOLUTAMENTE TODO lo que se construyó y decidió en la sesión madre de OpenCode. Leerlo al inicio de cada nueva sesión para no perder el hilo.

---

## 1. QUIÉN SOY

- **Nombre:** Agustín
- **Rubro principal:** Arquitectura y diseño de interiores (estudio familiar con su papá)
- **Segundo emprendimiento:** Secret Spot — marca de indumentaria surfwear
- **Ubicación:** Buenos Aires, zona norte, Argentina
- **Perfil:** Dueño de estudio de arquitectura + emprendedor de indumentaria. Busca escalar ambos negocios con herramientas digitales, marketing y procesos.

---

## 2. ESTRUCTURA DE TRABAJO EN OPENCODE

Se crearon DOS proyectos completamente aislados para no mezclar contextos:

### Proyecto A: A7 Arquitectura
- **Carpeta:** `~\Documents\OpenCode\estudio-arquitectura\`
- **Git:** https://github.com/Agustin918/Agente---A7---Opencode-
- **Contexto:** Estudio de arquitectura sustentable, 100% personalizado, familiar
- **Rol del agente:** Project Manager Senior experto en arquitectura, costos, escalabilidad de servicios profesionales y gestión integral de obras y clientes.
- **Tono:** Profesional, técnico, confiable, español rioplatense, directo

### Proyecto B: Secret Spot
- **Carpeta:** `~\Documents\OpenCode\marca-ropa\`
- **Git:** https://github.com/Agustin918/Agente---Secret---Opencode
- **Contexto:** Marca surfwear argentina, público streetwear/surf/skate/playero, lifestyle costero-urbano
- **Rol del agente:** Experto en e-commerce, marketing digital, diseño de moda, gestión de stock y ventas
- **Tono:** Creativo, dinámico, moderno, español rioplatense, directo

---

## 3. CONFIGURACIÓN TÉCNICA DE CADA PROYECTO

Cada carpeta contiene:
- `CLAUDE.md` → personalidad, reglas, contexto del negocio
- `opencode.json` → skills, MCPs, permisos
- `.env` → API keys reales (no se sube a git — está en .gitignore)
- `.env.example` → template de las keys necesarias
- `memoria.md` → registro de sesiones
- `.gitignore`
- `00-contexto/contexto_historico.md` → este archivo (SOLO en arquitectura)

### Skills disponibles (ruta global `C:\Users\MSI\.opencode\skills`):
ads, ad-creative, brand-voice, brand, banner-design, content-engine, content-strategy, copywriting, copy-editing, cro, cold-email, competitor-profiling, crosspost, customer-research, design, design-system, deep-research, frontend-design, image, lead-magnets, marketing-ideas, marketing-plan, marketing-psychology, seo, seo-audit, social, slides, stop-slop, ui-styling, ui-ux-pro-max, video-editing, y más (40 skills en total)

### MCPs habilitados:
Firecrawl (scraping), GitHub (repos), Context7 (docs), Fal.ai (imagen/video/audio — solo en marca-ropa), Sequential Thinking, Memory

---

## 4. SISTEMA DE MEMORIA ENTRE SESIONES

### Comando "Guardar sesión" / "Terminamos por hoy":
1. Resumir tareas hechas, decisiones y próximos pasos
2. Sobrescribir `memoria.md` con ese resumen
3. `git add .` → `git commit -m "Actualización de memoria"` → `git push`

### Comando "Iniciar sesión" / "Traer cambios":
1. `git pull`
2. Leer `memoria.md` actualizado
3. Saludar al usuario con breve resumen de dónde se quedaron

---

## 5. REGLAS FUNDACIONALES (APLICAN SIEMPRE)

### Para ambos proyectos:
- **Regla de Lectura Autónoma:** No podés leer archivos nativamente. Usá `python .agents\scripts_lectura\lector_universal.py <ruta>` para leer imágenes, PDFs, DOCX, XLSX, videos. Nunca le digas al usuario "no puedo ver eso".
- **Aislamiento de contexto:** Arquitectura NO habla de moda. Moda NO habla de arquitectura.
- **Respuestas directas:** Sin vueltas, sin reformular lo que dijo el usuario, sin cortesías.
- **Español rioplatense:** Vos, che, tono directo.
- **Eficiencia de tokens:** Corto y denso por defecto. "corto" = 3 líneas. "puntual" = bullets. "expande" = ahí explayarse.
- **Organización continua:** Nunca archivos sueltos. Cada nuevo tema/herramienta = nueva subcarpeta.
- **Si algo no está claro:** Preguntar UNA sola cosa y seguir.

### Para A7 Arquitectura específicamente:
- Lenguaje técnico de construcción, BIM, project management
- Enfoque en procesos, estandarización, eficiencia
- Cliente premium-medium de zona norte y CABA
- Diferencial: sustentabilidad + 100% personalizado

### Para Secret Spot específicamente:
- Enfoque en ventas e imagen de marca
- Respuestas con viñetas, tablas, grillas de contenido
- Público: streetwear, surf, skate, playa, lifestyle relajado

---

## 6. PRÓXIMOS PASOS NATURALES (PENDIENTES)

### Para A7 Arquitectura:
- [ ] Definir y activar CRM de leads
- [ ] Armar y optimizar pauta de Meta Ads
- [ ] Crear web / landing page del estudio
- [ ] Estandarizar procesos de presupuestación y contratos
- [ ] Sistema de seguimiento de obras y clientes
- [ ] Estrategia de contenido para redes (Instagram)

### Para Secret Spot:
- [ ] Terminar de definir branding visual
- [ ] Configurar e-commerce (plataforma, catálogo)
- [ ] Campañas de lanzamiento y Meta Ads
- [ ] Embajadores / influencers surf
- [ ] Logística y stock inicial
- [ ] Pricing y estructura de costos

---

*Fin del contexto histórico. Documento creado el 22/07/2026.*
