---
name: Niseko 2027 Trip Page
description: A two-ink screenprint the club pulled for the trip; black stock, maize ink, nothing else.
colors:
  maize-ink: "#ffc72c"
  black-stock: "#0e0d0b"
  bone: "#efe6c8"
  bone-dim: "#b3aa90"
  spent-rule: "#3a362c"
typography:
  display:
    fontFamily: "\"Big Shoulders Display\", \"Arial Narrow\", sans-serif"
    fontSize: "clamp(92px, 27vw, 232px)"
    fontWeight: 900
    lineHeight: 0.8
    letterSpacing: "-0.005em"
  headline:
    fontFamily: "\"Big Shoulders Display\", \"Arial Narrow\", sans-serif"
    fontSize: "clamp(42px, 8vw, 72px)"
    fontWeight: 900
    lineHeight: 0.9
    letterSpacing: "0"
  title:
    fontFamily: "\"Big Shoulders Display\", \"Arial Narrow\", sans-serif"
    fontSize: "clamp(28px, 5vw, 36px)"
    fontWeight: 900
    lineHeight: 1
    letterSpacing: "0.01em"
  intro-title:
    fontFamily: "\"Fraunces\", Georgia, serif"
    fontSize: "min(12vw, 18vh)"
    fontWeight: 900
    fontStyle: "italic"
    lineHeight: 0.86
    letterSpacing: "-0.02em"
  body:
    fontFamily: "\"Atkinson Hyperlegible\", system-ui, -apple-system, \"Segoe UI\", sans-serif"
    fontSize: "17px"
    fontWeight: 400
    lineHeight: 1.6
    fontFeature: "\"tnum\" 1"
  label:
    fontFamily: "\"Atkinson Hyperlegible\", system-ui, -apple-system, \"Segoe UI\", sans-serif"
    fontSize: "13px"
    fontWeight: 700
    lineHeight: 1.6
    letterSpacing: "0.12em"
rounded:
  none: "0px"
spacing:
  page-gutter: "clamp(20px, 5.5vw, 48px)"
  nav-height: "52px"
  section-top: "72px"
  column-gap: "56px"
  block-inset: "20px 22px"
  list-row: "16px"
components:
  button-primary:
    backgroundColor: "{colors.maize-ink}"
    textColor: "{colors.black-stock}"
    typography: "{typography.label}"
    rounded: "{rounded.none}"
    padding: "14px 20px"
  button-primary-hover:
    backgroundColor: "{colors.black-stock}"
    textColor: "{colors.maize-ink}"
  button-line:
    backgroundColor: "transparent"
    textColor: "{colors.maize-ink}"
    rounded: "{rounded.none}"
    padding: "14px 20px"
  button-line-hover:
    backgroundColor: "{colors.maize-ink}"
    textColor: "{colors.black-stock}"
  button-disabled:
    backgroundColor: "transparent"
    textColor: "{colors.bone-dim}"
  ink-slab:
    backgroundColor: "{colors.maize-ink}"
    textColor: "{colors.black-stock}"
    rounded: "{rounded.none}"
  stamp-box:
    backgroundColor: "{colors.black-stock}"
    textColor: "{colors.bone}"
    rounded: "{rounded.none}"
    padding: "20px 22px"
  index-link:
    textColor: "{colors.bone-dim}"
    typography: "{typography.label}"
    padding: "16px 0 13px"
  index-link-active:
    textColor: "{colors.maize-ink}"
  included-item:
    backgroundColor: "{colors.maize-ink}"
    textColor: "{colors.black-stock}"
    padding: "9px 14px"
  checkbox:
    rounded: "{rounded.none}"
    size: "22px"
---

# Design System: Niseko 2027 Trip Page

## Overview

**Creative North Star: "The Club Screenprint"**

The page is a two-colour poster the club pulled by hand for the trip: uncoated near-black stock, one maize ink, and bone where the ink has been cleared so text can be read. Every surface is either stock or a solid block of ink; anything in between is a halftone of those two inks, never a third colour or a translucent tint. Paper grain sits over everything at a barely-there 5% opacity, and the two ink slabs (the cover band under the hero art and the footer) have seeded rough-cut edges, so the page reads as an object rather than a screen.

Structure comes from printed rules, not boxes. Sections open on a condensed poster headline in maize, and content runs in open columns separated by solid maize ink rules (2-3px) between blocks and a 1px spent-rule hairline between rows inside a list. The density is a run sheet: practical facts set plainly in a highly legible humanist sans, with the display face carrying the stoke in headings, day numerals, prices and step counters.

The build refuses the dark SaaS landing page: no rounded cards, no pill chips, no glass, no drop shadows, no smooth colour-to-colour gradients.

**Key Characteristics:**
- Two inks on black stock; bone is cleared stock, not a third colour.
- Square corners everywhere (0px).
- Ink rules and quiet hairlines replace cards and borders.
- Condensed poster display face, uppercase, weight 900; Atkinson Hyperlegible for reading.
- Rough-cut SVG-masked edges on full-bleed ink slabs only.
- Falling bone snow on a canvas behind content.

## Colors

One ink, one stock, and the stock showing through.

### Primary
- **Maize Ink** (`maize-ink`): the only colour. Section headlines, day numerals, prices, step counters, links, ink rules, the active index underline, progress fills, included-item blocks, primary button fills, the cover slab and footer slab, focus rings, selection and scrollbar thumb.

### Neutral
- **Black Stock** (`black-stock`): the page ground, and the knocked-out text colour on any maize block (slab, footer, primary button, included item, today tag, emergency block).
- **Bone** (`bone`): reading text and h3/title text on stock; also the snow flakes.
- **Bone Dim** (`bone-dim`): secondary text: section intros, labels, inactive index and day links, metadata, FAQ answers, checked packing items, unticked checkbox borders.
- **Spent Rule** (`spent-rule`): row hairlines inside lists, the 1px rule between schedule days, progress-bar tracks, and the keyline of a disabled button.

### Named Rules
**The Two Inks Rule.** Maize and black stock are the only inks. Tints exist only as halftone dot patterns of one ink over the other (7px dot grid, 6px on progress tracks); never as opacity washes, smooth blends or new hues.

**The Knockout Rule.** Text on a maize block is always black stock; text on stock is bone, bone-dim, or maize. Bone never sits on maize.

## Typography

**Display Font:** Big Shoulders Display 900 (with Arial Narrow, sans-serif)
**Body Font:** Atkinson Hyperlegible 400/700 (with system-ui, -apple-system, Segoe UI, sans-serif)
**Intro Lettering:** Fraunces italic 900/600 (with Georgia, serif), on the wave intro only

**Character:** A tall condensed poster face set in uppercase does the shouting; a sturdy, legibility-first humanist sans does the explaining, readable on a phone outdoors. Tabular figures are on page-wide so times, prices and counts align.

### Hierarchy
- **Display** (900, clamp(92px, 27vw, 232px), 0.8): the cover headline (the trip dates) knocked out of the maize slab, and nowhere else. Deliberately overruns its column into the right gutter and never wraps. A secondary line under it sits at 0.27em.
- **Headline** (900, clamp(42px, 8vw, 72px), 0.9, uppercase, maize): section h2s.
- **Title** (900, clamp(28px, 5vw, 36px), 1.0, uppercase, bone): block and packing-group h3s; house names enlarge to clamp(40px, 7vw, 58px) in maize. Display-face numerals at 28-92px set prices, step counters, day numbers and emergency numbers in maize.
- **Intro title** (Fraunces italic 900, min(12vw, 18vh), 0.86, mixed case, maize; subtitle Fraunces italic 600 in bone): "Niseko 2027" and "Powder Pilgrimage · Jan 3–9" on the wave intro, right-aligned clear of the wave. Echoes the italic serif on the cover art; used nowhere else.
- **Body** (400, 17px, 1.6): all reading text; section intros at 18px in bone-dim with a 58-62ch measure; list headings at 18px/700; secondary notes 15px.
- **Label** (700, 13px, 0.1-0.14em, uppercase): index strip links, day-strip links, fact table terms (14px), slot times, contact roles. Labels name a field or a place; they are never a decorative line above a heading.

### Named Rules
**The Poster Face Rule.** The display face is always weight 900 and uppercase (numerals excepted), never used for running text.

**The Plain Facts Rule.** Times, prices, dates and deadlines in body copy are set in Atkinson at 700, not in a decorative treatment.

## Layout

A single centred column, max 1080px, with a fluid gutter of clamp(20px, 5.5vw, 48px). The hero art runs edge to edge at 16:9 (capped at 72vh, 56vh from 900px), immediately followed by the full-bleed maize slab; from 900px the slab splits into a 1.3fr / 1fr grid with the lede on the left and the ruled fact table on the right, the cover headline spanning both.

Under the slab, a sticky printed index strip (52px, padded by the top safe-area inset so it covers the phone status bar) on black stock with a 2px maize base rule scrolls horizontally on phones. Sections open with 72px of top space; reading measures are capped at 58-62ch for prose and 720-760px for lists. Two-up layouts (sign-ups, houses, contacts) collapse to one column below roughly 720-860px with a 56px gap; packing goes three-up from 820px.

The schedule is the signature layout: from 900px a 170px sticky SVG rail sits beside the days with a 48px gap; below 900px it becomes a sticky day strip under the index with a 4px progress line. Mobile is first: every row is full width and thumb-reachable, and the back-to-top square appears only from 760px.

## Elevation & Depth

Flat. There are no drop shadows anywhere at rest. Depth comes from three printed effects: the paper-grain noise overlay (11% opacity, screen blend) over the whole page; halftone dot fields that read as a lighter ink pass; and stacking order, with the falling snow canvas sitting behind the content (z-index 1, content at 2) so flakes drift through the gutters and stock but never over the text. During the intro banner only, the snow is raised above it.

`box-shadow` appears only as an inset 2px ink keyline (outline buttons, optional items, legend swatch), which is a printed border, not elevation.

### Named Rules
**The Flat Stock Rule.** Nothing floats. If a surface needs to stand out, it becomes a solid ink block or gets an ink rule; it never gets a shadow, blur or glow.

## Shapes

Every corner is square (0px). The only irregular silhouette is the rough-cut edge: a seeded jagged SVG mask (14px tall) on the bottom edge of the cover slab and the top edge of the footer, the two full-bleed ink slabs, as if the ink were pulled to a torn paper edge. Inner elements stay square and clean.

Separation is by rule weight. Section-level and block-level divisions use solid maize ink rules: 3px atop a sign-up block or a stamp box, 2px between days, under the index, at the head of house and contact grids, and as a vertical divider between two-up houses. Rows inside a list (schedule slots, add-ons, steps, travel legs, mountain and town lists, packing items, FAQ entries, contacts) are separated by a 1px spent-rule hairline, so maize is saved for real emphasis. Small marks are drawn, not typed: the FAQ plus is two crossed 3px ink bars that rotate 45 degrees to a cross when open; the packing tick is a hand-drawn maize SVG stroke.

### Named Rules
**The Rule Hierarchy Rule.** Solid ink rule between sections and blocks; 1px spent-rule hairline between rows inside a list and between schedule days. Never a full border box around a list row.

## Components

### Buttons
Square ink blocks with stamped uppercase labels and a small stroked SVG arrow.
- **Shape:** square (0px), padding 14px 20px, 15px/700 uppercase at 0.06em, 10px gap to a 14px icon.
- **Primary:** solid maize ink with black-stock text.
- **Hover / Focus:** the inks swap: stock fill, maize text, 2px inset maize keyline; 150ms colour transition (none under reduced motion). Focus uses the global 3px maize outline offset 3px.
- **Line:** transparent with maize text and a 2px inset maize keyline; on hover it fills with maize and knocks the text out to stock.
- **On the slab:** inverted (stock fill, maize text); hover fills maize with a 2px stock keyline.
- **Disabled:** no fill, bone-dim text, spent-rule keyline, no pointer events.

### Cards / Containers
There are no cards. Three containers exist:
- **Ink slab:** full-bleed maize band with a rough-cut edge; plain ink, no dot field.
- **Stamp box:** 3px maize border, stock fill, 20px 22px padding, max 640px; a display-face maize title over plain body. Used once per section at most for the single fact a reader must not miss.
- **Ink block:** solid maize, stock text, 20px 22px padding (emergency numbers).

### Inputs / Fields
- **Checkbox:** 22px square, 2px bone-dim border; maize border on hover and when checked, with a hand-drawn maize tick overflowing the box. The checked label dims to bone-dim with a 2px maize strike-through.
- **Progress bar:** 6px spent-rule track, solid maize fill scaling from the left (350ms ease-out).

### Navigation
- **Printed index strip:** sticky, stock ground, 2px maize base rule. Links are 13px/700 uppercase labels at 0.1em in bone-dim, bone on hover; the current section turns maize with a 4px maize underline that overprints the base rule. Scrolls horizontally on phones with the scrollbar hidden.

### Schedule Rail (signature)
One maize line threads the week. Desktop: a sticky SVG rail of day dots (stock fill, 2.5px maize stroke) that fill solid as days pass and grow when active, with labels turning maize. Phone: a sticky day strip of labels over a 3px spent-rule track with a solid maize fill tracking scroll progress. Each day opens with a large maize display numeral; included items are solid maize blocks with stock text, optional items carry a 2px inset maize keyline, and slots are separated by hairlines. A day with no plan yet collapses to one compact line (bone-dim numeral, "Plan TBA" label). A small square maize "today" tag marks the current day.

## Do's and Don'ts

### Do:
- **Do** keep every surface either black stock or solid maize ink; express in-between values as halftone dots.
- **Do** separate sections and blocks with 2-3px solid maize rules, and rows inside a list with a 1px spent-rule hairline.
- **Do** set section headlines in Big Shoulders Display 900 uppercase in maize, and all reading text in Atkinson Hyperlegible.
- **Do** swap inks on button hover (maize fill to stock fill with a maize keyline, or the reverse).
- **Do** keep corners square (0px) on every element.
- **Do** keep the snow canvas behind content so flakes never cross text.

### Don't:
- **Don't** introduce a third hue, a translucent tint, or a smooth colour-to-colour gradient (CSS gradients that draw halftone dots, rules and marks are the world's own tools and are fine).
- **Don't** use rounded cards, pill chips, glass panels or drop shadows; the page is printed, not layered.
- **Don't** use offset hard shadows on buttons; hover is an ink swap.
- **Don't** put a decorative uppercase line above a section headline; headlines stand alone.
- **Don't** apply the rough-cut edge to inner containers; it belongs to the full-bleed slabs only.
- **Don't** set bone text on maize.
