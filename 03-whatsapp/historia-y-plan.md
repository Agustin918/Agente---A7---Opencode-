# WhatsApp — Historia del Bloqueo y Plan de Calentamiento

> Actualizado: 03/08/2026

## ⚠️ LA REGLA NÚMERO UNO — LEE ESTO PRIMERO

**EL BRIDGE DE WHATSAPP ESTÁ PROHIBIDO. NUNCA ENCENDERLO.**

Meta detecta el bridge (whatsapp-mcp-vgp) y **RESTRINGE LA CUENTA DE WHATSAPP**. Fue exactamente lo que pasó con la línea anterior de Agustín. El puente marca al número como actividad no humana y la línea termina bloqueada.

## Qué pasó (historia completa)

1. Se usó un bridge de WhatsApp no oficial (`whatsapp-mcp-vgp`) para automatizar mensajes.
2. **Meta detectó el bridge y RESTRINGIÓ la cuenta de WhatsApp** de Agustín (su número personal).
3. Cada vez que Agustín contactaba leads nuevos desde el número marcado, **WhatsApp lo bloqueaba de nuevo**, incluso a baja frecuencia (1 persona cada 2-3 días).
4. La causa: el número quedó marcado por el uso previo del bridge, y el **algoritmo de 2026** acumula mensajes sin respuesta en una ventana de 30 días.

## Cómo funcionan los bloqueos de WhatsApp en 2026

- El algoritmo usa un **contador acumulativo de 30 días** que rastrea mensajes enviados sin respuesta en 48hs.
- **La tasa de respuesta importa más que el volumen.** Si la gente no te responde, el contador sube aunque mandes poco.
- Patrón sospechoso: mandar muchos mensajes a desconocidos en poco tiempo, texto repetido, o actividad no humana (bridge).
- **Contactos mutuos** (agendados en ambos lados) = señal de confianza que protege el número.

## Decisión tomada: línea nueva

- **Agustín compró un chip nuevo** (nueva línea WhatsApp).
- El número anterior queda para conversaciones ya abiertas, el nuevo es la línea principal de contacto de leads.

## Reglas de oro (las que rompieron la línea anterior)

1. **NUNCA** puentear WhatsApp — solo app oficial (WhatsApp Web / app de escritorio).
2. **No** mandar el mismo mensaje a varios contactos seguidos (patrón de spam).
3. **No** arrancar con mensajes largos de venta — primero presentarse.
4. Si un contacto nuevo no responde, **no recontactarlo a las 48hs en frío**; esperar días.
5. **Agendar SIEMPRE los contactos** antes de escribirles (nombre completo + foto).
6. Máximo **2-3 mensajes por día** a desconocidos durante el calentamiento.

## Plan de calentamiento del chip nuevo

### Días 1-3 — Usar como número personal
- Registrar en WhatsApp solo con app oficial.
- Cargar perfil: foto, nombre real, descripción (que parezca persona de verdad).
- Chatear con familia y amigos, responder rápido.
- Entrar a 2-3 grupos y escribir algo.
- **NO mandar nada a desconocidos.**

### Días 4-7 — Actividad moderada
- Contactar clientes existentes (los que ya respondieron antes).
- Máximo 2-3 mensajes por día.
- Llamadas de voz breves con conocidos.
- Guardar contactos con nombre completo + foto.

### Días 8-12 — Escalar con cuidado
- Sumar leads tibios (los que respondieron alguna vez).
- Mantener 3-5 mensajes por día, espaciados.
- Responder SIEMPRE que le escriban (tasa de respuesta > volumen).

### Día 13+ — Uso normal pero cauteloso
- Recién acá contactar leads nuevos.
- Respetar el contador de 30 días: si un lead no responde en 48hs, ese mensaje cuenta en contra por un mes.

## Nota sobre los 8 leads pendientes
Los leads que llenaron el formulario **no son fríos**: están esperando el mensaje. Eso juega a favor (tasa de respuesta alta protege el número). Plan de contacto espaciado en 4 días, 2 por día (ver `02-gestion/leads/estado-crm.md`).

## Estado de contacto (03/08)
- ✅ **Sofía Young** y **Roberto Sánchez**: mensajes enviados el 3/08 con el chip nuevo.
- ⏳ Pendientes: Nora, Sebastián, Juan, Cecilia, María, Nancy (2 por día).

## Acceso a mensajes (solo lectura de DB local)
Si se necesita revisar mensajes viejos de la línea anterior, se usa directamente la DB:
```
sqlite3 whatsapp-mcp-vgp/whatsapp-bridge/store/messages.db
```
- Puerto bridge: 8080 (mantener cerrado siempre)
- Token bridge (NO USAR): `842de7712adb7c9153ba9ec5be8c2fab2d80a671a1563c6c9e1852f9251d5a56`
