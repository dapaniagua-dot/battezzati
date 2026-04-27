# CLAUDE.md

> Archivo de contexto para **Claude Code**. Leer **siempre** antes de empezar a trabajar.

---

## 1. Qué es este proyecto

Sitio web institucional y comercial de una **empresa de venta de materiales eléctricos** (mayorista + minorista), en etapa de crecimiento.

**Importante:** El código de este repositorio **NO se está armando desde cero**. Fue **generado originalmente con Claude Design** (visualizer) y luego exportado a este proyecto. La tarea acá es **refinar, mejorar y profesionalizar** ese código base, no reescribirlo.

---

## 2. Rol de Claude Code en este repo

Claude Code actúa como **diseñador y desarrollador frontend senior** que toma el código exportado y lo lleva a calidad de producción.

### Qué tiene que hacer Claude Code

1. **Leer primero el skill `frontend-design`** disponible en su entorno antes de tocar HTML, CSS o JSX.
   - Ubicación típica: `/mnt/skills/public/frontend-design/SKILL.md`
   - Este skill define los estándares de diseño profesional que se deben aplicar (tipografía, jerarquía, escalas, espaciado, microinteracciones, evitar la "estética AI genérica").
2. **Auditar lo que ya está exportado** y detectar:
   - Inconsistencias visuales
   - Problemas de jerarquía tipográfica
   - Espaciados arbitrarios
   - Colores fuera del sistema
   - Componentes que parecen genéricos / templated
   - Falta de respiro o exceso de relleno
3. **Proponer las mejoras antes de aplicarlas** cuando sean estructurales.
4. **Aplicar refinamientos directos** cuando sean cosas chicas (espaciados, hovers, microcopys, accesibilidad, responsive).
5. **Mantener intacta la identidad visual** (paleta y logo).

### Qué NO tiene que hacer

- ❌ Rehacer el sitio desde cero.
- ❌ Cambiar el stack o introducir frameworks (React, Astro, Next, Tailwind por CDN, etc.) **sin consultar antes**.
- ❌ Modificar el logo o reemplazar la tipografía base.
- ❌ Borrar secciones existentes sin avisar.
- ❌ Ignorar el skill `frontend-design`. Es obligatorio leerlo al inicio.

---

## 3. Identidad visual (no negociable)

### Paleta

| Rol | Color | Uso |
|---|---|---|
| Base | **Negro** `#0A0A0A` (ajustar al exacto del logo) | Header, footer, bloques fuertes, tipografía principal |
| Acento | **Amarillo** `#FFD500` (ajustar al exacto del logo) | CTAs, hovers, destacados, detalles |
| Fondo | **Blanco** `#FFFFFF` | Fondo de las secciones de contenido |
| Gris auxiliar | `#F4F4F4` | Separadores, fondos sutiles |
| Gris texto | `#444444` | Texto secundario |

> Usar **CSS variables en `:root`**. Si algún color del código exportado quedó hardcodeado, migrarlo a variable.

### Estilo

- Moderno, **industrial**, líneas marcadas, contraste alto.
- Nada de pasteles, sombras exageradas o gradientes innecesarios.
- Animaciones **sutiles** al hacer scroll.
- Mobile first.

---

## 4. Stack y workflow

- **Frontend:** HTML + CSS + JS (lo que haya exportado Claude Design). Mantener.
- **Editor:** VS Code.
- **Versionado:** Git + GitHub.
- **Deploy:** Railway (deploy automático al hacer push).

```
Claude Code → git add . → git commit -m "..." → git push → Railway redeploy
```

Commits chicos, en español:
- `feat: agrega seccion de marcas`
- `style: ajusta jerarquia tipografica del hero`
- `fix: corrige overflow del header en mobile`
- `refactor: migra colores hardcodeados a CSS variables`

---

## 5. Secciones que tiene el sitio

(Ya generadas por Claude Design — revisar y refinar)

1. Header fijo + menú
2. Hero / portada con CTAs ("Ver catálogos" y "Solicitar presupuesto")
3. Por qué elegirnos
4. Marcas que trabajamos (placeholders de logos)
5. Catálogos (placeholders de PDFs)
6. Formulario de presupuesto (mayorista / minorista)
7. Nosotros en redes (placeholder)
8. Contacto y ubicación
9. Footer

---

## 6. Tareas concretas pendientes

### Refinamiento de diseño (prioridad alta)
- [ ] Pasar el sitio entero por el skill `frontend-design` y aplicar mejoras de jerarquía, espaciado y tipografía.
- [ ] Auditar contraste y accesibilidad (WCAG AA mínimo).
- [ ] Revisar consistencia de los CTAs (tamaños, hovers, estados).
- [ ] Refinar microinteracciones (hover en tarjetas, botones, links del menú).
- [ ] Verificar responsive en breakpoints reales (375px, 768px, 1024px, 1440px).
- [ ] Migrar todos los colores a CSS variables.

### Funcional
- [ ] Cargar logos reales de marcas en `/assets/logos-marcas`.
- [ ] Cargar catálogos reales en `/assets/catalogos` y linkearlos.
- [ ] Conectar el formulario de presupuesto a email o WhatsApp Business.
- [ ] Botón flotante de WhatsApp (mobile y desktop).
- [ ] Datos finales de contacto, mapa real.

### SEO y meta
- [ ] Meta tags + Open Graph.
- [ ] Favicon.
- [ ] `sitemap.xml` y `robots.txt`.

---

## 7. Convenciones

### HTML
- Indentación de 2 espacios.
- Etiquetas semánticas (`<header>`, `<section>`, `<nav>`, `<footer>`).
- `alt` obligatorio en todas las imágenes.

### CSS
- CSS variables en `:root`.
- Mobile first.
- Breakpoints: `480px`, `768px`, `1024px`, `1280px`.
- Si conviene, BEM (`.tarjeta__titulo--destacada`).

### JS
- Vanilla, sin dependencias externas salvo justificación.
- Comentarios en bloques no obvios.

### Idioma
- Todo el contenido visible al usuario en **español**.
- Comentarios de código pueden ir en español o inglés (consistencia dentro de un mismo archivo).

---

## 8. Reglas de oro

1. **Leer el skill `frontend-design` al iniciar la sesión.** No saltearlo.
2. **Antes de tocar algo estructural, explicar y esperar OK.**
3. **No borrar lo que generó Claude Design** sin avisar — refinar, no reemplazar.
4. **Respetar paleta, logo y tipografía.**
5. **No agregar dependencias** sin consultar.
6. **Dejar placeholders claros** (`<!-- TODO: ... -->`) cuando falten assets.
7. **Commits chicos y descriptivos.**
8. **Siempre justificar las decisiones de diseño** apoyándose en el skill.

---

## 9. Cómo levantar el proyecto

```bash
# desde la raíz
npx serve .
# o Live Server de VS Code
```

---

## 10. Datos del proyecto

- **Responsable:** Diego Alejandro Paniagua
- **Ubicación:** Ciudad Autónoma de Buenos Aires
- **Cliente:** [completar nombre de la empresa de materiales eléctricos]
- **Origen del código base:** Claude Design (visualizer), exportado a este repo.
- **Refinamiento y desarrollo continuo:** Claude Code + VS Code.

---

_Última actualización: abril 2026_