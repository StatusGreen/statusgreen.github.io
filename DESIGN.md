<!-- SEED: established with the user before implementation; re-run /impeccable document once the header/footer and hero are rebuilt to this direction, to capture the actual tokens and components. -->

---
name: Status Green Solutions
description: A light "systems status board" — a bold green highlight, two-tone headline type, and functional status color, built for a hospital-IT audience.
colors:
  primary: "#004f3b"
  highlight: "#6ae861"
  interop-blue: "#2f6fed"
  advisory-amber: "#f5a524"
  paper: "#faf8f4"
  grid-line: "#e8e4da"
  ink: "#1c1a15"
  surface-dark: "#1f2937"
  neutral-white: "#fbf9fa"
  divider-gray: "#9ca3af"
typography:
  display:
    fontFamily: "Plus Jakarta Sans, system-ui, sans-serif"
    fontSize: "clamp(2.5rem, 6vw, 4.25rem)"
    fontWeight: 800
    lineHeight: 1.05
    letterSpacing: "-0.01em"
  body:
    fontFamily: "system-ui, Avenir, Helvetica, Arial, sans-serif"
    fontSize: "1rem"
    fontWeight: 400
    lineHeight: 1.6
  mono:
    fontFamily: "IBM Plex Mono, ui-monospace, SFMono-Regular, monospace"
    fontSize: "1rem"
    fontWeight: 600
    letterSpacing: "0.01em"
  title:
    fontFamily: "system-ui, Avenir, Helvetica, Arial, sans-serif"
    fontSize: "1.5rem"
    fontWeight: 700
    lineHeight: "normal"
rounded:
  sm: "8px"
  md: "16px"
  full: "999px"
---

# Design System: Status Green Solutions

## Overview

**Creative North Star: "The Status Board"**

This redesign replaces the previous dark-console world ("The Green Light Protocol") with a light, structured status board: a plain warm paper ground, a bold green highlight used deliberately on the hero's key phrase, and functional status color instead of a purely achromatic palette. It's built from two references: Red Rover Health's bold two-tone headline treatment (a heavy sans headline with one phrase set in the accent color), and Teak's light, rounded, gridded-paper register with a monospace stat row and colored nav bullets — both translated for a hospital-IT audience rather than copied literally.

Two interpretive calls were made translating those references, worth confirming: **(1)** `terminal_banner.png` — PRODUCT.md records it as a confirmed brand commitment ("a systems-status/green-light metaphor consistent with the company name"), so rather than discarding it with the rest of the old dark world, it's kept alive as a smaller framed "console" proof module elsewhere on the page instead of the full-bleed header background. **(2)** Teak's nav uses decorative rainbow dots; here they're narrowed to three colors that carry real operational meaning (green = live, blue = interoperability, amber = advisory) rather than arbitrary decoration, matching PRODUCT.md's "controlled, precise, non-hype tone." Say so if either call is wrong.

The voice shifts from Quiet Confidence's flat restraint to something more assertive but still composed: confident, not clinical-cold. Bold type and one loud color moment are allowed; sprawling color, illustration, or gamified UI (Teak's literal register) are not — this is a hospital vendor's site, not a consumer app's.

**Key Characteristics:**
- Warm paper ground, a plain surface replacing the prior black console background — a grid-line texture was tried and deliberately dropped as a generated-UI cliché
- One bold green highlight band per view, behind the hero's key phrase — a deliberate, loud moment, not a rare accent
- Bold, two-tone display headlines: heavy sans weight, one phrase set in the highlight green
- Monospace stat row for real proof numbers (years in business, hospital networks served)
- Functional status-dot colors (green / blue / amber) in navigation and status chips — never decorative rainbow
- Rounded geometry throughout (chips, cards, pill buttons) — reverses the previous no-radius rule
- The terminal-banner asset survives as a framed proof module, not the page's dominant surface

## Colors

Mostly warm neutrals and one confident green, with two small functional colors reserved for status meaning.

### Primary
- **Deep Signal Green** (`#004f3b` / `{colors.primary}`): The SG wordmark; also the fill for primary buttons and icon marks needing full brand weight.

### Secondary
- **Signal Green** (`#6ae861` / `{colors.highlight}`): The bold highlight band behind one phrase in the hero headline, borrowed from Teak's highlight treatment. Promoted from "rare confirmation glyph" (the old world) to a deliberate, loud headline device — see The Single Highlight Rule.

### Tertiary
- **Interop Blue** (`#2f6fed` / `{colors.interop-blue}`): Status-dot color reserved for data-interoperability context (nav, status chips).
- **Advisory Amber** (`#f5a524` / `{colors.advisory-amber}`): Status-dot color reserved for advisory/attention context. Never used together decoratively — each carries one specific meaning wherever it appears.

### Neutral
- **Warm Paper** (`#faf8f4` / `{colors.paper}`): The new page background, replacing the prior pure-white/black-only ground.
- **Grid Line** (`#e8e4da` / `{colors.grid-line}`): Subtle borders and dividers on the paper ground (nav underline, hero/section rules, the service-column divider). Originally also used as a background texture grid; that application was tried, flagged by the design hook as a generated-UI cliché, and dropped — the token now lives only in structural lines, never as a decorative field.
- **Warm Ink** (`#1c1a15` / `{colors.ink}`): Body text color — a warm near-black, not pure black, matching the paper ground.
- **Slate Console** (`#1f2937` / `{colors.surface-dark}`): Kept from the prior world as the footer's dark closing band — deliberate contrast bookend against the now-light body.
- **Paper White** (`#fbf9fa` / `{colors.neutral-white}`): The light logo variant, used on the dark footer band.
- **Steel Divider** (`#9ca3af` / `{colors.divider-gray}`): The footer's divider rule.

### Named Rules
**The Single Highlight Rule.** Exactly one phrase per view gets the `{colors.highlight}` treatment — a background band behind text, never a repeated or full-bleed application. This supersedes the old world's "Confirmation-Only Rule," which forbade green from being used this boldly; the new direction intentionally promotes green to a headline device, once per view, not scattered.

**The Status Semantics Rule.** `{colors.interop-blue}` and `{colors.advisory-amber}` are never decorative. They appear only where they mean something specific — a nav category, a status chip, a proof-point icon — keeping the added color functional rather than ornamental for a hospital-IT audience.

## Typography

**Display Font:** Plus Jakarta Sans (bold weights), with system-ui fallback
**Body Font:** system-ui, Avenir, Helvetica, Arial, sans-serif (unchanged from the prior world)
**Mono Font:** IBM Plex Mono, with system monospace fallback — a new role, for stat-row numerals

**Character:** Heavy, slightly-rounded geometric display type paired with a plain body stack and a mono accent for numbers. The display face was chosen because both pinned references converge on the same shape independently — Red Rover Health's bold headline weight and Teak's rounded, friendly grotesk character — rather than defaulting to a generic display face.

### Hierarchy
- **Display** (800, `clamp(2.5rem, 6vw, 4.25rem)`, 1.05 line-height): The hero headline — two-tone, with exactly one phrase in `{colors.highlight}`.
- **Title** (700, 1.5rem, normal line-height): Section labels and the footer's "Contact Info" label — unchanged from the prior world.
- **Body** (400, 1rem, 1.6 line-height): Running text. Line-height opened up from the prior 1.5 to read comfortably on the new paper ground.
- **Mono/Label** (600, 1rem, mono, 0.01em tracking): Stat-row numerals (e.g., years in business, hospital networks served) — borrowed from Teak's stat row, applied to real PRODUCT.md proof points only.

## Layout

The page shell keeps its prior structure (full-height flex column, header and footer bookending the content) but the ground shifts from black to a plain Warm Paper surface. The header goes light: a nav bar with small colored status dots before each label (green/blue/amber, per The Status Semantics Rule), and the hero headline sits directly on the paper ground rather than inside a dark banner band. The existing terminal-banner asset is reframed as a smaller, contained "console" module — a proof point elsewhere on the page — rather than the full-bleed header background it was in the prior world. The footer keeps its dark Slate Console band unchanged in role, now reading as a deliberate contrast close against the lighter body above it.

None of this is built yet — the current code (`src/App.vue`) still reflects the prior dark-console header/footer. This section describes the target to build toward, not an extracted fact.

## Elevation & Depth

Mostly flat, matching the paper-and-ink register: no heavy drop shadows. One soft ambient shadow is permitted under a single floating callout element (a status-confirmation bubble, echoing Teak's toast-style badge) — used once, not as a general card treatment.

## Shapes

Rounded geometry is now the default, reversing the prior world's no-radius rule: `{rounded.sm}` (8px) for status chips and dots, `{rounded.md}` (16px) for cards, `{rounded.full}` (999px, pill) for buttons and nav dot indicators.

## Components

Nothing below is built yet — these are intended patterns for the next implementation pass, not extracted from working code.

### Navigation
- **Style:** Light bar on Warm Paper, logo left, nav labels each preceded by a small colored status dot (`{rounded.full}`, 8-10px) — green/blue/amber per The Status Semantics Rule, never decorative.

### Hero
- **Style:** Bold two-tone Display headline directly on the paper ground, one phrase carrying the `{colors.highlight}` band (The Single Highlight Rule). A Mono-styled stat row sits beneath the supporting copy, surfacing real PRODUCT.md numbers (years in business, hospital networks, team size) rather than invented metrics.

### Console proof module
- **Style:** The existing `terminal_banner.png` framed inside a contained card (`{rounded.md}`), used as a single proof point demonstrating the "systems status" metaphor — not the page's dominant surface.

### Footer
- **Style:** Unchanged from the prior world — Slate Console band, Paper White logo, contact block, Steel Divider rule, copyright line. See the prior scan-mode extraction for the exact structure; it still matches the live code.

## Do's and Don'ts

### Do:
- **Do** use `{colors.highlight}` exactly once per view, as a bold band behind one phrase — The Single Highlight Rule.
- **Do** keep `{colors.interop-blue}` and `{colors.advisory-amber}` tied to real status meaning wherever they appear — The Status Semantics Rule.
- **Do** surface only real PRODUCT.md numbers in the mono stat row; an invented metric is a factual claim, not a design choice.
- **Do** preserve `terminal_banner.png` as a proof module rather than discarding it — it's a confirmed PRODUCT.md brand commitment, not incidental old-world debris.

### Don't:
- **Don't** repeat the highlight-green treatment more than once per view, or let it become a full-bleed fill — it stays a deliberate, rare loud moment even though it's now bold.
- **Don't** add more than the three functional status colors (green/blue/amber), and don't use them decoratively — no rainbow nav, no arbitrary color-per-item.
- **Don't** carry over Teak's gamified UI register (toy mockups, reward-badge copy, illustrated app chrome) — the audience is hospital IT leadership, not consumer app users.
- **Don't** reintroduce the prior world's pure-black/pure-white-only palette or its no-radius rule; both are superseded here.
