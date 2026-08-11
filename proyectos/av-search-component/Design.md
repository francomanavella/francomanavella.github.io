# Design System — Design.md
> Documento de referencia para mantener consistencia visual en todos los diseños y componentes del producto.
> **Regla de oro:** Antes de crear cualquier pantalla, componente o elemento visual, consultá este archivo.

---

## 1. Identidad Visual

| Atributo       | Valor                                                          |
|----------------|----------------------------------------------------------------|
| **Nombre**     | AV Principal Design                                            |
| **Tono visual**| Limpio, moderno, con confianza. Minimalista pero no frío.      |
| **Audiencia**  | Profesionales entre 25–45 años, acostumbrados a herramientas digitales. |
| **Principios** | Claridad · Consistencia · Accesibilidad · Propósito            |

---

## 2. Colores

> ⚠️ NUNCA usar valores hexadecimales hardcodeados. Siempre referenciar tokens semánticos.

### Escala de Grises (Primitivos)
```
--gray-0:    #FFFFFF   → Blanco puro
--gray-100:  #FAFAFA
--gray-200:  #F5F5F5
--gray-300:  #E9E9E9
--gray-400:  #D9D9D9
--gray-500:  #C4C8C5
--gray-600:  #B6B6B6
--gray-700:  #969696
--gray-800:  #6C6C6C
--gray-900:  #5A5A5A
--gray-1000: #494949
--gray-1100: #393838
--gray-1200: #1B1B1B   → Negro base
```

### Brand
```
--color-primary:         #1B1B1B   → Acción principal, CTA, fondo de botones primarios (gray1200)
--color-primary-hover:   #494949   → Estado hover de botones primarios (gray1000)
--color-primary-press:   #6C6C6C   → Estado press de botones primarios (gray800)
--color-primary-light:   #EEF0FD   → Fondos sutiles, badges, highlights
--color-secondary:       #F4A623   → Acento, notificaciones, destacados
--color-secondary-hover: #D4891A   → Estado hover de elementos secundarios

color.logo.avianca.primary: #FF0000   → Logo Avianca · Light mode: red500 · Dark mode: #FF0000

--color-danger:       #FF0000   → Botón Danger default (red500)
--color-danger-hover: #D90000   → Botón Danger estado hover
--color-danger-press: #C20000   → Botón Danger estado pressed
```

### Neutros
```
--color-text-primary:    #1B1B1B   → Texto principal, títulos (gray1200)
--color-text-secondary:  #6C6C6C   → Texto de soporte, descripciones (gray800)
--color-text-disabled:   #5A5A5A   → Texto inactivo, placeholders (gray900)
--color-text-inverse:    #FFFFFF   → Texto sobre fondos oscuros (gray0)

--color-background:      #FFFFFF   → Fondo de página (gray0)
--color-surface:         #FAFAFA   → Cards, panels, inputs (gray100)
--color-surface-raised:  #FFFFFF   → Modales, dropdowns (con sombra)
--color-border:          #E9E9E9   → Bordes de componentes (gray300)
--color-border-strong:   #D9D9D9   → Bordes con mayor énfasis (gray400)

--color-hover:          #E9E9E9   → Fondo/overlay en estado hover
--color-pressed:        #D9D9D9   → Fondo/overlay en estado pressed/active
--color-disabled:       #d9d9d9   → Fondo de elementos disabled (ej. botón disabled, input disabled)
```

### Link
```
--color-link-default:    #177F8C   → Links en estado default (blue800)
--color-link-active:     #0E4C54   → Links en estado hover/active (blue900)
```

### Feedback
```
--color-success:         #10B981   → Confirmaciones, estados positivos
--color-success-light:   #ECFDF5   → Fondo de mensajes de éxito
--color-warning:         #F59E0B   → Alertas, advertencias
--color-warning-light:   #FFFBEB   → Fondo de mensajes de advertencia
--color-error:           #EF4444   → Errores, validaciones fallidas
--color-error-light:     #FEF2F2   → Fondo de mensajes de error
--color-info:            #3B82F6   → Información contextual
--color-info-light:      #EFF6FF   → Fondo de mensajes informativos
```

### Modo Oscuro (Dark Mode)
```
--color-background-dark:     #0F0F1A
--color-surface-dark:        #1A1A2E
--color-text-primary-dark:   #F3F4F6
--color-text-secondary-dark: #9CA3AF
--color-border-dark:         #2D2D44
```

---

## 3. Tipografía

### Familias
```
--font-primary: 'Red Hat Display', sans-serif   → Toda la UI: títulos, cuerpo, labels, botones
--font-mono:    'IBM Plex Mono', mono            → Código, datos técnicos, IDs, tokens
```

### Pesos disponibles
```
font.weight.300 → Light
font.weight.400 → Regular
font.weight.600 → SemiBold
font.weight.700 → Bold
font.weight.900 → Black
```

### Escala de Tamaños

| Token                 | px  | Uso                            |
|-----------------------|-----|--------------------------------|
| `font.size.x-tiny`    | 10  | Micro labels, metadata         |
| `font.size.tiny`      | 12  | Captions                       |
| `font.size.small`     | 14  | Labels, descripciones          |
| `font.size.normal`    | 16  | Cuerpo principal               |
| `font.size.medium`    | 18  | Cuerpo destacado               |
| `font.size.large`     | 20  | Títulos de componentes         |
| `font.size.x-large`   | 24  | Subsecciones, card titles      |
| `font.size.huge`      | 32  | Secciones principales          |
| `font.size.x-huge`    | 36  | Títulos de página              |
| `font.size.x-x-huge`  | 44  | Hero, landing                  |
| `font.size.gigantic`  | 52  | Display                        |

### Letter Spacing
```
font.letter-spacing.dense  → -0.2   → Títulos grandes
font.letter-spacing.normal →  0     → Uso general
font.letter-spacing.loose  →  0.5   → Overlines, etiquetas
```

### Estilos de Texto — Botones
```
text.button.B100 → Red Hat Display Bold, 14px, ls: 0   → Botón pequeño (sm)
text.button.B200 → Red Hat Display Bold, 20px, ls: 0   → Botón default
```

### Estilos de Texto — Links
```
text.link.default.L100 → Red Hat Display Regular, 14px + underline → Link small, default
text.link.default.L200 → Red Hat Display Regular, 20px + underline → Link default
text.link.bold.L100    → Red Hat Display Bold,    14px + underline → Link small, hover/active
text.link.bold.L200    → Red Hat Display Bold,    20px + underline → Link hover/active
text.link.bold.L300    → Red Hat Display Bold,    28px + underline → Link en títulos H600
text.link.bold.L400    → Red Hat Display Bold,    32px + underline → Link en títulos H700
```

---

## 4. Espaciado

> Base unit: **4px**. Todos los espaciados son múltiplos de esta base.

```
--space-0:   0px
--space-1:   4px    → Micro espaciado, íconos internos
--space-2:   8px    → Padding de chips, badges
--space-3:   12px   → Padding de inputs pequeños
--space-4:   16px   → Padding estándar de componentes
--space-5:   20px   → Espaciado entre elementos relacionados
--space-6:   24px   → Padding de cards
--space-8:   32px   → Separación entre secciones menores
--space-10:  40px   → Separación entre componentes
--space-12:  48px   → Márgenes de sección
--space-16:  64px   → Separación entre secciones grandes
--space-20:  80px   → Padding de hero, secciones de página
--space-24:  96px   → Espaciado extra generoso
```

---

## 5. Bordes y Radio

```
--radius-sm:   4px    → Badges, chips, tags
--radius-md:   8px    → Botones, inputs, cards pequeñas
--radius-lg:   12px   → Cards, modales
--radius-xl:   16px   → Panels, sheets
--radius-2xl:  24px   → Elementos destacados, ilustraciones
--radius-full: 9999px → Pills, avatares, toggles

--border-width:        1px
--border-width-strong: 2px
```

---

## 6. Sombras

```
--shadow-sm:   0 1px 2px rgba(0,0,0,0.05)
--shadow-md:   0 4px 6px -1px rgba(0,0,0,0.07), 0 2px 4px -1px rgba(0,0,0,0.05)
--shadow-lg:   0 10px 15px -3px rgba(0,0,0,0.08), 0 4px 6px -2px rgba(0,0,0,0.04)
--shadow-xl:   0 20px 25px -5px rgba(0,0,0,0.10), 0 10px 10px -5px rgba(0,0,0,0.04)
--shadow-focus:    0 0 0 3px rgba(0,167,167,0.35)   → Reservado para inputs y elementos no-botón
--color-focus-ring: #1D9BF0                         → Ring de focus en botones · outline 2px · offset 2px
```

---

## 7. Iconografía

- **Librería:** Lucide Icons (stroke, no fill)
- **Tamaños permitidos:** 16px · 20px · 24px · 32px
- **Stroke width:** 1.5px (estándar) / 2px (énfasis)
- **Color:** heredar del contexto (`currentColor`)
- ❌ No mezclar librerías de íconos distintas en una misma pantalla.

> ⚠️ **Nota de conflicto (sin resolver):** la librería documentada en 7.1 (Figma "AV | Components · Tokens") usa íconos **filled/solid**, no stroke. Coexiste con la regla de Lucide de arriba. Queda pendiente que el Design Lead defina si son dos sistemas distintos (ej. Lucide para UI general, esta librería para íconos específicos de producto/app AV) o si uno reemplaza al otro.

---

## 7.1 Librería de Íconos AV (Figma)

> Fuente: Figma · *AV | Components · Tokens* · página "Icons"
> Link: https://www.figma.com/design/ECDGWyRzZJC2AJxzmRNls2/AV-%7C-Components---Tokens?node-id=20001-1646

### Especificaciones generales

```
Estilo:          Filled / solid (no stroke) · monocromo negro (#1B1B1B) por defecto
Tamaño base:     24 × 24 px (todas las categorías icon/*)
Color:           hereda del contexto salvo excepción indicada (flags, payment, brand)
Naming:          icon/{categoría}/{nombre}  · ej. icon/action/search
```

### Categoría: Action (`icon/action/*`) — 133 íconos

Add, Backup, Basura2, BookMark, BookMark-Outline, Hide, view, Pause, Play, Remove, Slash, add, Minus, accessibility, accessibility_dots, addpeople, alarm, alarm_add, alarm_off, alarm_on, android, aspect_ratio, assessment, assignment, assignment_ind, assignment_late, assignment_return, bug_report, done_all, cached, download, camera_mic, class, contact_cal, speaker_notes, assignment_returned, data_setting, attachment, delete, autorenew, device_info, badge, dns, edit, edit_underline, exit_to_app, explore, favorite, favorite_outline, find_in_page, find_replace, flip_to_back, flip_to_front, add_shopping_cart, tune, loyalty, group_work, media, invert_colors, membership, label, label_outline, note_add, open_in_browser, language, launch, lock, lock_open, open_with, pageview, phone_msg, picture_in_picture, polymer, rotation, scan_wifi, track_changes, search, settings, settings_applications, settings_backup_restore, settings_display, settings_ethernet, settings_input_component, settings_input_hdmi, settings_input_svideo, settings_overscan, settings_phone, settings_power, settings_bluetooth, settings_cell, settings_remote, settings_voice, shop, shop_two, translate, spellcheck, star_rate, stars, grade, supervisor_account, swap_horiz, swap_horiz_light, swap_vert, swap_vert_circle, trending_neutral, trending_up, trending_down, system_update_tv, tab, tab_unselected, unread_mailbox, turned_in, verified_user, thumb_up, thumb_down, thumbs_up_down, dashboard, view_agenda, view_array, view_carousel, view_column, view_day, subject, view_headline, view_list, view_module, view_quilt, view_stream, view_week, Add_lineal, Remove_lineal, bars_chart_curved, Save_icon, mobile, copy, wifi, wifi_off, sync_alt

### Categoría: Alert (`icon/alert/*`) — 20 íconos

Block, success, check_circle_outline, check_circle, active, Denied, Notification, notifications_off, notifications_on, Important-Notification, Important, Error, announcement, Report, error, info, New-Releases, help, price, New-Promo

### Categoría: Items (`icon/items/*`) — 29 íconos

FlightLand, takeoff, theaters, Mail, offer, wallet, Puzzle, phone, grocery_store, timer, pizza, calendar-month, cake, poll, schedule, credit_card, print, coffee, event, receipt, attach_money, events, school, monetization, file, shopping_basket, giftcard, takeon, battery_alert

### Categoría: Maps (`icon/maps/*`) — 51 íconos

Adventure_nature, car_wash, drink, Bank, convenience_store, florist, apartament, directions, gas_station, Destination, directions_bike, Location, Pin_keep, directions_bus, hospital, World, directions_car, hotel, airport, directions_ferry, bar, directions_subway, beenhere, directions_train, cafe, location_city, restaurant, mall, satellite, map, see, my_location, shipping, navigation, snow, parking, store, laundry_service, pharmacy, taxi, layers, pin_drop, terrain, layers_clear, playa_y_sol, traffic, atm, library, rate_review, airplanemode_active, airplane_inactive

### Categoría: Navigation (`icon/navigation/*`) — 23 íconos

apps, fullscreen_exit, unfold_more, unfold_less, arrow_back, arrow_forward, home, list, cancel, list order up, chevron_left, chevron_right, expand_less, expand_more, menu, more_horiz, more_vert, close, open_in_new, refresh, fullscreen, Dot, Heart

### Categoría: Services (`icon/services/*`) — 36 íconos

Advance flight, baby_car, ChangeFlight, carry-on-baggage, Luggage, airplaneTicket, Maleta1, Maleta2, Maletas2, update, Refund, LifeMiles, NewLifemiles, LifeMiles_new_simple, LifeMiles_new, Silla1, SillaVacia, visibility_off, Silla2, pets, neurodivergent, bike, medical_assistance, travel, hearing_disabled, special_services, change_flight, priority_boarding, small_backpack, lounges, asistenciaViajes, carry-on-baggage-single, on-board-menu, accesibility-person, directions_walk, directions_run

### Categoría: Social (`icon/social/*`) — 35 íconos

Messenger, people, wc, account_box, group_add-outline, sms02, account_circle, person, ccount_child, person_add, face_unlock, plus_one, group_add, question_answer, history, share, whatshot, sms, mood, Exclusive, notifications_paused, child, facebook, twitter, linkedIn, instagram, tiktok, youtube, whatsapp, facebook-no-circle, twitter-no-circle, instagram-no-circle, youtube-no-circle, tiktok-no-circle, linkedin-no-circle

### Flags (`flag/*`) — 21 × 15 px · 24 países/regiones

Argentina, Colombia, EstadosUnidos, RepublicaDominicana, Bolivia, CostaRica, Guatemala, Panama, Uruguay, Brasil, Ecuador, Mexico, Nicaragua, Honduras, Peru, France, UK, Paraguay, Chile, Canada, Europe, ElSalvador, Spain, Others

### Payment (`payment/*`) — 40 × 24 px · 10 métodos

amex, diners, discover, masterCard, visa, applePay, Nequi, daviplata, PSE, aCredits

> Color: se respeta el color de marca de cada logo (no monocromo). Usar el set `paymentMethodsAvailable` (masterCard, visa, applePay, Nequi, PSE) como agrupación default para mostrar métodos de pago disponibles.

### App Icons — navegación inferior (`appIcon/*`) — 24 × 24 px · 10 íconos · 2 estados

home, logo, myTrips, offers, flightStatus, profile, options, pin, add, search

```
Estado default: outline/lineal
Estado active:  filled/solid
```

---

## 8. Componentes Base

### Botones

| Variante  | Default BG              | Default Border          | Hover BG               | Hover Border              | Pressed BG             | Pressed Border         | Texto                   |
|-----------|-------------------------|-------------------------|------------------------|---------------------------|------------------------|------------------------|-------------------------|
| Primary   | --color-primary #1B1B1B | --color-primary #1B1B1B | --color-primary-hover  | --color-primary-hover     | --color-primary-press  | --color-primary-press  | --color-text-inverse    |
| Secondary | --color-background #FFF | --color-primary #1B1B1B | --color-hover #E9E9E9  | --color-primary-hover #494949 | --color-pressed #D9D9D9 | --color-primary #1B1B1B | --color-text-primary   |
| Danger    | --color-danger #FF0000  | --color-danger #FF0000  | --color-danger-hover #D90000 | --color-danger-hover | --color-danger-press #C20000 | --color-danger-press | --color-text-inverse  |
| Link      | transparent             | none                    | —                      | —                         | —                      | —                      | --color-link-default    |

**Disabled (todas las variantes excepto Secondary):** bg --color-disabled #D9D9D9 · border #D9D9D9 · texto --color-text-disabled
**Secondary disabled:** bg --color-hover #E9E9E9 · border --color-border-strong #D9D9D9 · texto --color-text-disabled
**Focused (todas las variantes):** mismo visual que default + outline 2px #1D9BF0 offset 2px

```
Height:        52px (fixed)
MinWidth:      100px
Padding:       0px top/bottom · 24px left/right
Border-radius: --radius-full (9999px) → pill
Border-stroke: 2px (Secondary default y todos los Active)
Font default:  text.button.B200 → Red Hat Display Bold, 20px
Font small:    text.button.B100 → Red Hat Display Bold, 14px
Focus state:   outline: 2px solid --color-focus-ring (#1D9BF0) · outline-offset: 2px (separado 2px del borde del botón)

-- Visual states (map to tokens):
```
Hover:   background-color = var(--color-hover) or component-specific hover token (e.g. --color-primary-hover)
Pressed: background-color = var(--color-pressed) or component-specific press token (e.g. --color-primary-press)
Disabled: background-color = var(--color-disabled); color = var(--color-text-disabled)
```

Nota: Los tokens `--color-hover`, `--color-pressed` y `--color-disabled` se aplican por defecto a los botones de variante `Secondary`. Para `Primary` y otras variantes, priorizar tokens específicos de variante (`--color-primary-hover`, `--color-primary-press`, etc.).

Link — Default:      Regular weight, sin underline
Link — Hover/Press/Active: Bold weight + underline
```

### Input

Patrón de label siempre visible: el label se muestra en 14px cuando el campo está vacío, y se reduce a 12px cuando el campo está activo (focused) o con contenido.

```
Height (field):   64px
Height total:     87px — field 64px + gap 4px + helperText 19px
Padding:          12px top/bottom · 16px left/right
Border:           1px solid
Border-radius:    4px (--radius-sm)
Gap field→helper: 4px (--space-1)
Font label default:  14px · Regular · Red Hat Display · #5a5a5a
Font label active:   12px · Regular · Red Hat Display · #5a5a5a
Font value:          16px · Bold   · Red Hat Display · #1b1b1b
Font helperText:     14px · Regular · Red Hat Display · #5a5a5a
Transition label: font-size 150ms ease
```

**Tokens de Input:**
```
--color-border-input-default: #949494   → Borde default y filled
--color-border-input-active:  #1ea93c   → Borde hover y active (verde)
--color-border-input-error:   #ff1c46   → Borde estado error
--color-input-bg-disabled:    #f5f5f5   → Fondo disabled y readOnly
--color-input-text-disabled:  #c4c8c5   → Texto label y valor en disabled
```

**Mapa de estados (de Figma `w8sBabOOJai0hs5ClT2QIN` nodo 22121-177):**

| Estado   | Border   | BG       | Label size · color  | Value color    |
|----------|----------|----------|---------------------|----------------|
| default  | #949494  | #ffffff  | 14px · #5a5a5a      | —              |
| hover    | #1ea93c  | #ffffff  | 14px · #5a5a5a      | —              |
| active   | #1ea93c  | #ffffff  | 12px · #5a5a5a      | #1b1b1b Bold   |
| filled   | #949494  | #ffffff  | 12px · #5a5a5a      | #1b1b1b Bold   |
| error    | #ff1c46  | #ffffff  | 12px · #c20000      | #1b1b1b Bold   |
| disabled | #d9d9d9  | #f5f5f5  | 12px · #c4c8c5      | #c4c8c5 Bold   |
| readOnly | #d9d9d9  | #f5f5f5  | 12px · #5a5a5a      | #5a5a5a Bold   |

### PillTabs

```
Height:        40px (fixed)
Width:         HUG (crece con el contenido)
Padding:       10.5px top/bottom · 18px left/right
Border-radius: --radius-full (9999px) → pill
Font:          text.button.B100 → Red Hat Display Regular, 14px
Gap interno:   8px (entre radio/checkbox y label) · 18px (entre label 1 y label 2)

Estado Default: bg #FFFFFF (gray0)
Estado Hover:   bg #E9E9E9 (gray-300) → --color-border
Estado Focus:   bg #FFFFFF + stroke 2px #1D9BF0 en ring externo (x=-2, y=-2, radius=9999)
```

### Cards

```
Background:     --color-surface-raised
Border:         1px solid --color-border
Border-radius:  --radius-lg
Padding:        --space-6
Shadow:         --shadow-md
Hover shadow:   --shadow-lg (si es interactiva)
Transition:     box-shadow 200ms ease
```

---

## 9. Grid y Layout

```
--grid-columns:     12
--grid-gutter:      24px   → Desktop
--grid-gutter-md:   16px   → Tablet
--grid-gutter-sm:   12px   → Mobile

--container-sm:     640px
--container-md:     768px
--container-lg:     1024px
--container-xl:     1280px
--container-2xl:    1440px
```

### Breakpoints
```
sm:   640px
md:   768px
lg:   1024px
xl:   1280px
2xl:  1536px
```

---

## 10. Motion y Animación

```
--duration-fast:    100ms   → Micro-interacciones (hover, focus)
--duration-normal:  200ms   → Transiciones estándar
--duration-slow:    350ms   → Entradas de componentes
--duration-slower:  500ms   → Animaciones de página

--ease-default:     cubic-bezier(0.4, 0, 0.2, 1)   → General
--ease-in:          cubic-bezier(0.4, 0, 1, 1)      → Salidas
--ease-out:         cubic-bezier(0, 0, 0.2, 1)      → Entradas
--ease-spring:      cubic-bezier(0.34, 1.56, 0.64, 1) → Elementos que "rebotan"
```

---

## 11. Reglas de Uso

### ✅ Siempre hacer
- Usar tokens semánticos en lugar de valores hardcodeados.
- Mantener contraste mínimo de **4.5:1** para texto sobre fondo (WCAG AA).
- Usar `--shadow-focus` en todos los elementos interactivos con foco de teclado.
- Aplicar transiciones en interacciones (hover, focus, active).
- Respetar la escala de espaciado al diseñar layouts.
- Usar `--font-display` solo para títulos grandes (h1, h2, display).

### ❌ Nunca hacer
- Inventar colores nuevos que no estén en el sistema.
- Usar más de 2 familias tipográficas en una misma pantalla.
- Crear espaciados arbitrarios fuera de la escala definida.
- Usar colores de feedback (success, error, warning) con fines puramente decorativos.
- Usar fuentes genéricas como Arial, Roboto o system-ui.
- Mezclar estilos de borde (algunos con radius, otros sin) en el mismo componente.
- Usar sombras muy fuertes en modo oscuro.

---

## 12. Accesibilidad

- **Contraste mínimo:** 4.5:1 texto normal / 3:1 texto grande (WCAG AA).
- **Tamaño mínimo de tap target:** 44×44px en móvil.
- **Focus visible:** siempre usar `--shadow-focus`, nunca `outline: none` sin reemplazo.
- **Texto alternativo:** todos los íconos funcionales deben tener `aria-label`.
- **Reducción de movimiento:** respetar `prefers-reduced-motion` desactivando animaciones.

---

## 13. AI Design Instructions

> Esta sección es para que una IA (como Claude) la lea antes de generar cualquier diseño.

Cuando generes pantallas, componentes o elementos visuales para este producto:

1. **SIEMPRE** referenciá los tokens definidos en este documento. Nunca uses valores hardcodeados.
2. **NUNCA** inventes colores, tipografías o espaciados que no estén en el sistema.
3. **USA** `--font-primary` (Red Hat Display) para toda la UI — títulos, cuerpo y botones.
4. **MANTENÉ** el tono visual: limpio, moderno, con aire. Generoso en espaciado.
5. **RESPETÁ** la escala de espaciado basada en 4px.
6. **APLICÁ** `--radius-full` (9999px) para botones pill y `--radius-xl` (16px) para cards/panels.
7. **VERIFICÁ** contraste antes de combinar colores de texto y fondo.
8. Si necesitás un token que no existe, **indicalo explícitamente** en vez de improvisar.
9. **PRIORIZÁ** la versión desktop-first a menos que se indique lo contrario.
10. Ante la duda, **menos es más**: preferí espaciado generoso y jerarquía tipográfica clara.
11. **BOTONES**: usá siempre `text.button.B200` (Bold 20px) como tamaño default y `B100` (Bold 14px) para variante small.
12. **LINKS**: Default = Regular, Hover/Active = Bold + underline. Color: `--color-link-default` / `--color-link-active`.

---

## 15. Componente Banner

> Referencia: DCXD-408 · AV Enablement | Design "Banner" component

### Tipos de Banner

**Tipo A — Full Image** (imagen ocupa el 100% del banner · 1248 × 300 px)

| ID | Variante                              | Descripción                                      | Status |
|----|---------------------------------------|--------------------------------------------------|--------|
| A1 | Solo imagen                           | Full bleed sin overlay de texto                  | ✅     |
| A2 | Con texto                             | Gradient izquierda + título/subtítulo blanco      | ✅     |
| A3 | Con precio                            | Gradient + texto + price tag "Desde COP X"        | ✅     |
| A4 | Con botón                             | Gradient + texto + CTA button primario            | ✅     |
| A5 | Con carrusel + paginación             | Gradient + texto + flechas prev/next + 5 dots     | ✅     |

**Tipo B — Split** (738 px imagen + 510 px texto, lado a lado · 1248 × 300 px total)

| ID  | Variante                              | Color área texto  | Status |
|-----|---------------------------------------|-------------------|--------|
| B6  | Sin botón                             | Teal #89D4E1      | ✅     |
| B7  | Con botón                             | Rojo #FF0000      | ✅     |
| B8  | Con carrusel                          | Rosa #FF3093      | ✅     |
| B9  | Con carrusel + paginación             | Teal #89D4E1      | ✅     |
| B10 | Con contador de ofertas               | Rojo #FF0000      | TBC    |

---

### Paleta de colores AV para área de texto (Split Banner)

Los banners tipo B pueden usar estos colores de marca AV como fondo del área de texto:

```
--color-av-red:  #FF0000   → Rojo corporativo AV
--color-av-blue: #1D9BF0   → Azul AV (coincide con --color-focus-ring)
--color-av-pink: #FF3093   → Rosa AV
--color-av-teal: #89D4E1   → Teal AV (fondo default del área de texto, B6 y B9)
```

**Regla de color de texto por fondo:**
| Fondo              | Color de texto       |
|--------------------|----------------------|
| `--color-av-teal`  | `#FF0000` (AV Red)   |
| `--color-av-red`   | `#FFFFFF` (blanco)   |
| `--color-av-pink`  | `#FFFFFF` (blanco)   |
| `--color-av-blue`  | `#FFFFFF` (blanco)   |

---

### Layout del Split Banner

**Posición imagen/texto:**
- Imagen derecha + Texto izquierdo
- Imagen izquierda + Texto derecha

**Alineación del texto dentro del área de texto:**
- Left
- Center
- Right

**Breakpoints:**
```
Desktop  ≥ 992px  → Split horizontal: imagen% y texto% lado a lado
Tablet & Mobile ≤ 991px → Stacked: imagen arriba, área de texto abajo
```

---

### Especificaciones técnicas

**Dimensiones (Figma · desktop):**
```
Banner completo:   1248 × 300 px
  Tipo A imagen:   1248 × 300 px (full bleed)
  Tipo B imagen:    738 × 300 px
  Tipo B texto:     510 × 300 px
```

**Full Image Banner (Tipo A):**
```
Imagen:           object-fit: cover · 1248 × 300 px
Gradient overlay: linear-gradient →  (izquierda → derecha)
  0%  rgba(0,0,0,0.65) · 45% rgba(0,0,0,0.28) · 72% rgba(0,0,0,0)
Text overlay:     x=48, y=80 desde esquina sup-izq del banner
  · SmallLabel    Red Hat Display Bold  · 16px  · blanco
  · LargeLabel    Red Hat Display Bold  · 34px  · blanco
  · InfoLabel     Red Hat Display Regular · 13px · blanco 75% opacidad
Price tag (A3):   "Desde COP X.XXX.XXX" alineado debajo del InfoLabel
Botón (A4):       White pill · Red Hat Display Bold 14px · dark (#1B1B1B)
Carrusel (A5):    slides de imagen; texto puede ser fijo o rotatorio
Paginación (A5):  5 dots · 8px diámetro · 8px gap · centered · y=272
```

**Split Banner (Tipo B):**
```
Desktop (≥ 992px):
  Imagen:       738 × 300 px · izquierda · object-fit: cover
  Área texto:   510 × 300 px · derecha · fondo en color AV brand
    padding:    24px todos los lados (--space-6)
    Botón:      posición bottom-right dentro del área de texto
    Texto:      en fondos rojo/rosa → blanco; en teal → rojo AV #FF0000

Tablet & Mobile (≤ 991px):
  Layout:       stacked vertical
  Imagen:       100% width · aspect-ratio definido
  Área texto:   100% width · padding: --space-8 (32px)
```

**Anatomía interna del área de texto (Tipo B · 510 × 300 px):**
```
┌─────────────────────────────────────────────────────────┐ 300px
│  ┌─────────────────────────────────┐ ┌──────────────┐  │
│  │  Banner text + price tag        │ │  Logo +      │  │
│  │  x=24  y=24  w=385  h=252      │ │  button      │  │
│  │                                 │ │  x=421 y=24  │  │
│  │  SmallLabel  (Bold 36px / 36lh) │ │  w=65  h=252 │  │
│  │  LargeLabel  (Bold 44px / 44lh) │ │              │  │
│  │  InfoLabel   (Reg  16px / 20lh) │ │  [Logo 65×42]│  │
│  │  [Price tag  — hidden default]  │ │  at top      │  │
│  │                                 │ │              │  │
│  │                                 │ │  [Button     │  │
│  │                                 │ │  132×30      │  │
│  │                                 │ │  at y=222]   │  │
│  └─────────────────────────────────┘ └──────────────┘  │
└─────────────────────────────────────────────────────────┘
 ←24px→ ←──── 385px ────→ ←12px→ ←65px→ ←24px→
                              510px total
```

**Tipografía del área de texto (Tipo B — del componente Banner text tag):**
```
SmallLabel:  Red Hat Display Bold   · 36px · line-height: 36px · 1 línea
LargeLabel:  Red Hat Display Bold   · 44px · line-height: 44px · 2 líneas max
InfoLabel:   Red Hat Display Regular · 16px · line-height: 20px · 1 línea
```

**Botón de acción (Tipo B):**
```
Label:         "Comprar ahora" · Red Hat Display Bold · 14px
Tamaño:        132 × 30 px (sigue spec Button B100 small)
Posición:      bottom-right del área de texto · x=421, y=246 en texto content 510px
Variante:      Primary (default dark #1B1B1B) sobre cualquier fondo AV
```

**Flechas de carrusel (Tipo A y B):**
```
Tamaño:        40 × 40 px · border-radius: 999px
Fondo:         blanco 88% opacidad
Ícono:         chevron · 8 × 16 px · stroke 2.5px · color #1B1B1B
Posición y:    (frame_height - 40) / 2  →  y = 130 en frame 300px
Posición x (Tipo B, en área imagen 738px):   izq x=16 · der x=682
Posición x (Tipo A, en banner 1248px):        izq x=16 · der x=1192
```

**Pagination dots:**
```
Cantidad:      5 dots
Diámetro:      8 px
Gap:           8 px entre dots  →  ancho total 72 px
Posición:      centrado horizontalmente · y = frame_height − 28  (y=272 en 300px)
Opacidad:      dot activo 100% · inactivos 35%
Color:         blanco sobre imagen
```

---

### Accesibilidad mínima

| Elemento                | Requerimiento                                                                     |
|-------------------------|-----------------------------------------------------------------------------------|
| Banner completo (interactivo) | `tabindex="0"` + `role="region"` + `aria-label` descriptivo + focus ring visible |
| Botón dentro del banner | Focus estándar del componente Button: `outline: 2px solid #1D9BF0` offset 2px    |
| Carrusel — navegación   | Flechas prev/next con `aria-label="Previous"` / `aria-label="Next"`              |
| Carrusel — live region  | `aria-live="polite"` en el contenedor de slides para anunciar cambios             |
| Paginación — dots       | `role="tablist"` + cada dot con `role="tab"` + `aria-selected` + `aria-label="Slide X of Y"` |
| Imágenes                | `alt` descriptivo siempre; decorativas → `alt=""`                                 |
| Contraste texto/fondo   | Mínimo 4.5:1 (WCAG AA) para texto normal; 3:1 para texto grande (≥18px bold)     |

**Focus ring en banner interactivo:**
```
outline: 2px solid var(--color-focus-ring, #1D9BF0)
outline-offset: 2px
```

---

### Motion del carrusel

```
Transición entre slides:  translateX · duration: --duration-slow (350ms) · ease: --ease-out
Auto-play:                opcional; debe pausarse en hover y cuando prefers-reduced-motion: reduce
Indicadores (dots):       transición de escala/opacidad · duration: --duration-fast (100ms)
```

---

## 14. Changelog

| Versión | Fecha       | Cambios                                                                 |
|---------|-------------|-------------------------------------------------------------------------|
| 1.0.0   | 2026-05-07  | Versión inicial del Design System                                       |
| 1.1.0   | 2026-05-29  | Actualización de colores (gray scale), tipografía (Red Hat Display), escala de tamaños, estilos de botón (B100/B200) y link (L100-L400), specs de Button component, focus ring teal |
| 1.2.0   | 2026-06-22  | Renombre de producto a "AV Principal Design", agregado token color.logo.avianca.primary (#FF0000 · red500 · light & dark) |
| 1.3.0   | 2026-06-22  | Variante Danger para botones (--color-danger/hover/press), corrección focus state: outline 2px #1D9BF0 offset 2px (--color-focus-ring) |
| 1.4.0   | 2026-06-22  | Specs de botones extraídos de Figma: Secondary hover border #494949, Secondary disabled bg #E9E9E9/border #D9D9D9, tabla completa con BG+Border por estado |
| 1.5.0   | 2026-06-22  | Componente Input completo desde Figma (22121-177): floating label 14px→12px, 7 estados (default/hover/active/filled/error/disabled/readOnly), 5 tokens de input, altura 64px, border-radius 4px |
| 1.6.0   | 2026-07-01  | Componente Banner (DCXD-408): 10 casuísticas — Tipo A Full Image (A1–A5, 1248×300, gradient overlay) + Tipo B Split (B6–B10, 738+510px, fondos AV brand), paleta AV (#FF0000/#FF3093/teal), texto blanco en fondos rojo/rosa, specs carousel arrows 40×40 y pagination dots 8px, breakpoints 992px, accesibilidad WCAG AA |
| 1.6.1   | 2026-07-03  | Banner — specs de tipografía Tipo B desde componente Figma: SmallLabel Bold 36px, LargeLabel Bold 44px, InfoLabel Reg 16px; anatomía interna del área de texto 510px; token --color-av-teal #89D4E1; tabla de color de texto por fondo; specs del botón de acción 132×30px B100 |
| 1.7.0   | 2026-07-03  | Nueva sección 7.1 — Librería de Íconos AV desde Figma ("AV \| Components · Tokens"): 327 íconos filled/solid 24×24 en 7 categorías (Action, Alert, Items, Maps, Navigation, Services, Social), 24 flags de países (21×15), 10 métodos de pago (40×24, color de marca), 10 app icons de navegación inferior con estados default/active (outline/filled). Nota de conflicto sin resolver con la regla Lucide de la sección 7 |

---

*Mantenido por el equipo de Diseño. Ante dudas, consultá con el Design Lead antes de modificar tokens existentes.*
