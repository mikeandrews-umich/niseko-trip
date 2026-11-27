# Handoff: picking this up on another machine

Live site: https://rossjapow.com (GitHub Pages, repo `mikeandrews-umich/niseko-trip`, branch `main`).
Everything the site needs is in this repo. Nothing lives only on the old machine.

> This file is public (the repo is public and Pages serves it). Keep emails, phone numbers,
> house addresses and private sheet links out of it.

## Get set up

```
git clone https://github.com/mikeandrews-umich/niseko-trip.git
cd niseko-trip
python -m http.server 8000
```

Open http://localhost:8000. No build step. To publish, commit and `git push` to `main`;
Pages redeploys in about a minute.

If you open the folder in Claude Code, point it at this file first ("read HANDOFF.md").

## What's where

| File | What it is |
|---|---|
| `index.html` | The whole site: CSS, markup, and JS in one file |
| `index.html` → `EDIT HERE` block (near the bottom) | Sign-up links and deadlines, schedule, packing list, contacts. Organizers edit here. See README.md |
| `js/gsap/` | GSAP 3.15.1 core + ScrollTrigger, MorphSVGPlugin and DrawSVGPlugin (minified, from the official download). Loaded just before the `EDIT HERE` script. Same rule as the intro: animate only `transform`/`opacity` |
| `js/leaflet/` | Leaflet 1.9.4 (checked against its published checksums) for the "Around Hirafu" map. Loaded only when you scroll near the map. Tiles are standard OpenStreetMap tiles, darkened with a CSS filter on `.leaflet-tile-pane`. No API key. Pins come from `SPOTS` in the `EDIT HERE` block |
| `img/wave.svg` | Great-wave engraving for the intro (compacted, ~1.3 MB, ~480 KB gzipped) |
| `index.html` → `.poster` | Top banner: Mt. Yotei as five inline-SVG print layers (sky halftone, sun, mountain, ridge, trees). GSAP prints them in one pass at a time, a few px out of register, then snaps them into register; on scroll the layers drift at different speeds and the sun sets. Waits for the intro to finish (`intro:done` event). The days-to-go figure rolls in like an odometer |
| `img/hero.jpg` | Link-preview image (`og:image`) only; no longer shown on the page |
| `img/trail-map.jpg` | Trail map in the Mountain section |
| `DESIGN.md` | The design system: two-ink screenprint, maize on near-black stock, rules instead of boxes |
| `PRODUCT.md` | Who the site is for and what it has to do |
| `CNAME` | `rossjapow.com`. Don't delete it or the custom domain drops |
| `.impeccable/config.json` | Design-detector exceptions (everything else in `.impeccable/` is gitignored scratch) |

## How the intro works (the part most likely to need tweaking)

- First visit per tab shows a full-screen wave intro (`#intro`); `sessionStorage` key `rssc-intro` skips it after.
- The wave image is created in JS (`new Image()` → `img/wave.svg`); once it has decoded and the Fraunces
  lettering font is in (2.5 s cap), a GSAP timeline plays the entrance: the wave surges in, then the letters of
  "Niseko 2027" rise one by one (each letter is its own `.c` span). The swell's idle rocking, the 7 s top bar and
  the exit are GSAP tweens too. CSS only holds the starting state. If GSAP fails to load, the intro is skipped.
- Title and subtitle are right-aligned on every screen size, so the wave (bottom left) never covers them.
- SVG effects: a brushstroke under the title is painted in with DrawSVG (it draws the centre line of a mask over
  the dry-brush shape). The wipe's foam lip (`.lip`) morphs with MorphSVG: it builds as you drag, then breaks and
  spills as the screen wipes up. All lip shapes come from one recipe (`lipShape` in the intro script), so they
  share the same points. Neither touches `img/wave.svg`.
- **Performance rule:** only `transform` and `opacity` animate. The SVG has ~2,900 paths, so anything that
  repaints it every frame (clip-path, filters, big scale changes, canvas effects over it) makes it jerky.
- Exit: swipe up (pointer events follow the finger; past 18% of the screen or a flick finishes it),
  tap, scroll wheel, or Enter/Space/Esc/↓. The screen wipes upward with a wavy foam "lip" (`.lip` SVG).
  It auto-opens after 7 s; if the art never loads, the site shows after 6 s.
- Portrait phones get a wider wave (`max-aspect-ratio:1/1` media query) and a shorter lip (8vh).

## Other things worth knowing

- The sticky menu (`.index`) has `padding-top: env(safe-area-inset-top)` so page text doesn't show
  above it under the iPhone status bar. A `ResizeObserver` keeps `--nav-h` in sync.
- `html { scroll-behavior: smooth }`: in scripts or devtools use `scrollTo({top, behavior: "instant"})`.
- Sign-ups point at the public sign-up Google Sheet (Optional Events and Dinners tabs). The organizers'
  private planning workbook must never be linked from the site.
- No house addresses or phone numbers go on the public page.

## Domain

- Registered at GoDaddy. DNS: four `A` records on `@` → 185.199.108.153 / .109 / .110 / .111,
  plus `www` CNAME → `mikeandrews-umich.github.io`.
- HTTPS is enforced; GitHub renews the certificate automatically. `www` and the old
  github.io URL redirect to https://rossjapow.com.
- Keep auto-renew on for the domain at GoDaddy.
- If the certificate ever gets stuck, remove the custom domain in repo Settings → Pages and add it back.

## Open items

- [ ] Check the menu on a real notched iPhone: scroll and confirm no text shows above the menu bar.
- [ ] Optional: verify the domain in GitHub (profile Settings → Pages → Add a domain) to stop
      anyone else's repo from claiming it.
- [x] Schedule filled in for all 7 days, with an "After dark" panel on days 1 to 6.
- [x] Schedule TBAs all filled in (last one: Blo*Blo après at 3 PM, Tue Jan 5).
- [ ] Deadlines and contacts in the `EDIT HERE` block.

## Recent history

```
454ad2d Serve the site at rossjapow.com
4c3bb8f Distill the page; keep the menu bar over the iPhone status bar
707626c Smoother wave intro with a swipe-up wipe
510885a Wave intro: the great wave swells in and wipes away to enter
3319f19 Redesign as a two-ink screenprint
```
