# Workspace Guidelines: Mintt Marketing - Child Learning Centre (CLC) Redesign

## 1. Project Overview
- **Client**: Child Learning Centre (CLC) - childlearningcentre.in
- **Goal**: Complete modern, mobile-first, parent-centric website redesign.
- **Team**: Tanmay Amte, Aryan Pilankar, Mansi Shahu
- **Reference UI/UX**: Butterfly Learnings (butterflylearnings.com) & modern pediatric healthcare platforms.

---

## 2. Active Design Intelligence Skills (.agents/skills)
The following skills are installed and active in this workspace:
- **`ui-ux-pro-max`**: Searchable database of 79 UI styles, 192 color palettes, 74 font pairings, 119 UX guidelines, 17 GSAP presets, and automated design system generation (`search.py --design-system`).
- **`better-ui`**: Pixel-level optical alignment, exact border-radius relationships, box-shadow elevations, and transition timing.
- **`better-typography`**: Hierarchy, line-height scaling, font pairings, and responsive fluid font clamps.
- **`better-accessibility`**: WCAG 2.2 AA standards, 4.5:1 minimum text contrast, keyboard navigation focus rings, and `prefers-reduced-motion`.
- **`better-colors`**: Semantic design tokens, HSL palette harmonic tuning, and surface elevation tints.

---

## 3. Frontend Architecture & Rules

### Core Design Mandate
**Every page, card, and interaction MUST be:**
1. **Attractive**: Modern, polished layout inspired by shadcn/ui & Aceternity UI with generous breathing room, elegant micro-glows, and fluid typography.
2. **Trustworthy**: 100% credible clinical presentation. 13-year medical heritage, verified therapist qualifications, real Google reviews, zero gimmicks, and strictly no emojis.
3. **Good & Comforting to the Viewers**: Tailored specifically to anxious parents. Calming, sensory-friendly colors, empathetic language without cold jargon, and frictionless 2-click access to help.

---

### Implementation Standards
1. **TECH STACK**:
   - **Core**: Semantic **HTML5**, modern **CSS3** (CSS Variables, Flexbox, Grid), and lightweight **Vanilla JavaScript**.
   - **shadcn/ui aesthetic**: Accessible, clean modals, accordions, tabs, and form elements.
   - **Aceternity UI aesthetic**:
     - Subtle border glows, floating navigation bar, and smooth marquee testimonial scrolling.
     - **Aceternity Text Components (Vanilla JS / CSS)**:
       1. **Text Hover Effect**: Interactive SVG stroke reveal & gradient glow on hover for major section headings.
       2. **Text Generate Effect**: Staggered word-by-word blur-to-clear opacity reveal as sections enter view.
       3. **Flip Words (`@aceternity/flip-words`)**: Vertical flip & blur-rotate animation between pediatric milestone words in the headline (e.g., "Helping your child to *Speak* / *Focus* / *Thrive*").
       4. **Container Text Flip (`@aceternity/container-text-flip`)**: Dynamic pill badge/card container that flips letters/words vertically while smoothly animating its own container width and padding to snugly fit changing words in real time.
     - **Advanced Buttons & Surface Effects (Vanilla JS / CSS)**:
       4. **Stateful Button**: Interactive action button transitioning smoothly between Idle &rarr; Loading spinner &rarr; Success checkmark confirmation for the consultation booking flow.
       5. **Hover Border Gradient**: Smooth rotating/gliding gradient border on hover for key cards and primary CTAs using the 3-color palette.
       6. **Noise Background**: Sensory-friendly subtle SVG noise grain overlay that adds tactile warmth and premium depth to surfaces without digital glare.
       7. **Sketch Button**: Tailwind-style organic hand-drawn sketch border button providing warm, child-friendly approachability.
     - **Carousels, Sliders & Navigation (Vanilla JS / CSS)**:
       8. **Animated Testimonials**: Aceternity-style stacked card carousel featuring rotational depth transitions, subtle 3D card tilt, parent quote reveals, and circular SVG arrow controls for genuine Google reviews and clinical social proof.
       9. **Simple Navbar with Hover Effects (`@aceternity/simple-navbar-with-hover-effects`)**: Floating frosted-glass pill navbar with a physics-inspired sliding hover pill indicator that smoothly glides between navigation links, clinic branch dropdown, click-to-call, and the stateful "Book Consultation" action.
2. **STRICT RULE: NO EMOJIS ANYWHERE IN THE WEBSITE**:
   - Never use emoji characters anywhere in text, headings, badges, or buttons.
   - Always use clean, crisp, professional vector SVG icons (inline SVGs or Lucide icons).
3. **THE OFFICIAL BRAND COLOR SYSTEM (From CLC Official Brochure)**:
   - **Color 1: Deep Navy Blue (#16244F / #0F1D40)** — Primary clinical authority & trust anchor, hero headlines, top bar, floating pill navbar base, badges, and structural cards. (15:1 Contrast ratio, WCAG AAA).
   - **Color 2: Warm Carmine Red (#C8232C / #B91C26)** — Core CLC brand identity (from official logo, vision panel, and branch pins), primary CTA action buttons ('Book Consultation', 'Call Us'), milestone highlights, and attention triggers. (6.5:1 Contrast ratio, WCAG AA).
   - **Color 3: Crisp Medical White & Clean Porcelain (#FFFFFF / #F8FAFC)** — Open, breathable card surfaces, sensory-calming background, high legibility, and modern shadcn/ui micro-borders (#E2E8F0).
   - **Text Readability Base**: #0F172A (Obsidian Charcoal for H1-H6) & #334155 (Deep Slate for body text) with subtle #64748B (Muted Slate).
4. **Design Tokens**: All colors, fonts, spacing, shadows, and radiuses must be declared in `:root` CSS variables.
5. **Typography**: Headings use friendly, rounded fonts (e.g. Manrope or Varela Round); body text uses clean, legible fonts (Nunito Sans / Inter).
6. **Parent-Centric UX**:
   - 2-click booking rule (Book Consultation / WhatsApp accessible everywhere).
   - Real HTML text for all branch details, phone numbers, and services (never locked inside poster images).
   - Mobile-first layout with a sticky bottom bar (`Call`, `WhatsApp`, `Book`).
7. **Motion & Transitions**:
   - Short, purposeful transitions (150ms–350ms ease-out).
   - CSS transforms (`translateY`, `scale`, `opacity`) only.
   - Always honor `@media (prefers-reduced-motion: reduce)`.
