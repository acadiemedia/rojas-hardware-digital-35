
## Ferretería Rojas — Local hardware store website

A bold blue & white, mobile-first site for the Cayma neighborhood ferretería, built around WhatsApp as the primary conversion channel (the way business actually gets done in Peru).

### Pages

**1. Home (`/`)**
- Hero: shop name "Ferretería Rojas", tagline ("Tu ferretería de confianza en Cayma"), location chip (📍 Cayma, Arequipa), and two prominent CTAs: **"Pedir por WhatsApp"** (primary, opens `wa.me/...`) and **"Cómo llegar"** (scrolls to map / opens Google Maps).
- Trust strip: 3 short value props — *Atención personalizada* · *Envíos a obra en Cayma* · *Yape / Plin / Efectivo*.
- Quick catalog: 5 large icon cards (Plomería, Electricidad, Construcción, Herramientas, Pinturas y Acabados) linking to `/catalogo`.
- "Por qué elegirnos" — 3 short blocks reinforcing local proximity, expert advice, and delivery to job sites.
- Location preview: embedded Google Map of Cayma + address + hours.
- Final CTA band: big WhatsApp button.

**2. Catálogo (`/catalogo`)**
- Intro line explaining "consulta disponibilidad y precios por WhatsApp".
- 5 category sections, each with: icon, category name, short description, and a bullet list of representative items (e.g. Plomería → tubos PVC, conexiones, grifería, llaves de paso, accesorios de baño).
- Each category card has its own **"Consultar por WhatsApp"** button that pre-fills a message like *"Hola, quisiera consultar sobre productos de plomería"*.

**3. Contacto (`/contacto`)**
- Big WhatsApp CTA at the top (the main action).
- Address, hours (Lun–Sáb / Domingo), phone (tap-to-call on mobile).
- Embedded Google Map of the Cayma location.
- Payment methods accepted (Yape, Plin, efectivo).
- Note about *Envíos a obra* in Cayma and surrounding areas.

### Global elements

- **Sticky floating WhatsApp button** in the bottom-right on every page (green circle, pulse animation on first load).
- Header with logo wordmark "Ferretería Rojas" + nav (Inicio · Catálogo · Contacto) + a compact "WhatsApp" button on desktop. Mobile: hamburger menu.
- Footer with address, hours, WhatsApp, social (placeholder), and copyright.
- Spanish copy throughout (Peruvian phrasing).

### Visual design — Bold blue & white

- **Primary blue** matching the storefront sign (deep saturated blue, ~ oklch ~0.42 0.20 255).
- **White** backgrounds, strong blue headings, dark gray body text.
- **Accent**: WhatsApp green only for WhatsApp CTAs (so they stand out and read as "tap to chat").
- Typography: bold geometric sans for headings (industrial/utility feel), clean sans for body.
- Category icons: simple line/solid icons in blue circles on white, white icons on blue on hover.
- Subtle texture or diagonal stripe accents echoing the painted blue/white storefront — used sparingly in section dividers and the hero.
- Generous touch targets, mobile-first layout (the viewport you're previewing is narrow — verified).

### WhatsApp wiring

- Single config constant `WHATSAPP_NUMBER` used everywhere. Once you give me the number, every CTA (hero, sticky FAB, category cards, contact page, footer) will link to `https://wa.me/<number>?text=<context-aware message>`.
- Until then I'll use `+51 000 000 000` as a placeholder so nothing breaks.

### SEO / metadata

- Per-route `head()` with unique title + description targeting *"ferretería en Cayma, Arequipa"*, plus og:title / og:description.
- Home og:image will use a hero photo of the storefront once provided (you can upload a cleaner shot later).

### Out of scope (can add later)

- Full searchable product database with prices.
- Online ordering / cart.
- Brand pages (Pavco, Indeco, Siderperu, etc.) — easy to add once you confirm which brands he stocks.
- Blog / DIY guides for SEO.
