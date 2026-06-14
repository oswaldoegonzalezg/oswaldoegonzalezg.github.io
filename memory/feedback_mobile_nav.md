---
name: feedback-mobile-nav
description: "Versión 1 DEFINITIVA del portafolio — desktop, mobile y tablet aprobados en modo oscuro y claro (v=43)"
metadata: 
  node_type: memory
  type: feedback
  originSessionId: 183b741d-9bff-4ca1-9533-69ef139a29b2
---

## ⚠️ VERSIÓN 1 DEFINITIVA (styles.css?v=43) — NUNCA MODIFICAR SIN APROBACIÓN EXPLÍCITA

Todas las secciones aprobadas en desktop, mobile y tablet (portrait y landscape), modo oscuro y claro. Esta es la única versión de referencia. Aunque el usuario pida cambios, NUNCA tocar lo listado aquí sin confirmación explícita.

**Fixes estructurales — NO REVERTIR:**
- `overflow:hidden` eliminado de `body.drawer-open` (solo `touch-action:none`) — fix crítico iOS scroll
- `visibilitychange` blur() eliminado — causaba scroll al volver del mail app / WhatsApp
- Botones email/WhatsApp: solo flash rojo, sin scroll ni loading state
- `#acerca{padding-bottom:72px}` — marquee dentro de Acerca, invisible al navegar a Casos
- `#casos{scroll-margin-top:48px}` — al navegar a Casos empieza directo en "02 Trabajo real"
- `#faq{padding-bottom:80px}` — border de última pregunta no se asoma en Contacto
- `#contacto{padding:72px 0 32px;min-height:unset;scroll-margin-top:48px}` — footer visible sin scroll
- FAQ: 5 preguntas (se eliminó "¿Cómo te mantienes actualizado...?" por bajo valor SEO)
- Marquee dentro de `#acerca` al final, antes del `</section>`
- `@media(max-width:900px){.marquee-wrap{margin-top:32px}}` — solo mobile

**Mejoras de calidad — NO REVERTIR:**
- `font-display:swap` en todas las fuentes (TTCommons, Hanson)
- `.metric-value{font-variant-numeric:tabular-nums}`
- `@media(prefers-reduced-motion:reduce){.marquee-track{animation:none}}`
- `alt="Bogotá, Colombia, donde vivo y trabajo como Social Media Manager"` en hero image
- Footer: ícono SVG outline LinkedIn solo (sin texto), color muted del sistema
- Focus trap en lightbox ya implementado
- `.tool-item:active` y `.tools-grid .tool-item:nth-child(2)` — typos de doble punto corregidos (v=35)
- CSS muerto eliminado: `.hero-sub`, `.hero` (landscape), `.nav-drawer-footer`, `.nav-drawer-logo`, `.section-deco-num`, `#drawer-theme-toggle`, `.drawer-theme-label`
- `::-webkit-scrollbar-thumb` siempre en `var(--accent)`, no solo en hover (v=36)

**Tablet (768px–1024px portrait y landscape) — NO REVERTIR:**
- `tools-grid`: `grid-auto-rows:210px`, `justify-items:stretch`, `gap:12px`, `tool-item width:100%` — todos los cards iguales (v=42)
- `contact-card`: una sola columna, botones full-width — fix para iPad landscape donde se cortaban (v=43)

**Why:** Cada fix resuelve un bug visual o de comportamiento confirmado y aprobado. Revertir cualquiera rompe algo.

**How to apply:** Antes de cualquier cambio, verificar que todos los fixes siguen intactos. Si algo puede afectar estas reglas, advertir primero.
