# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users
Members of the Ross Ski & Snowboard Club (RSSC) going on the Niseko trip, Jan 3–9, 2027. University of Michigan students, about 17 people across two houses. They open the page on their phones: in the weeks before the trip to book flights, sign up for add-ons and dinners, and pack; during the trip to check the day's plan.

## Product Purpose
One shared trip-info page for the Niseko trip: schedule, sign-ups, travel and arrival, housing, mountain and town notes, packing list, FAQs and contacts. Success is that nobody has to ask the group chat a question the page already answers, and that sign-ups happen through the linked sheet.

## Positioning
Inspired by the Kellogg ski trip site (kelloggskitrip.com) in structure, but its own identity. It is a club page for friends, not a commercial travel product.

## Operating Context
- Hosted on GitHub Pages at mikeandrews-umich.github.io/niseko-trip, from the repo mikeandrews-umich/niseko-trip. Static HTML, CSS and JS in one `index.html`, no build step.
- Sign-ups live in the "Niseko 2027 Sign-ups" Google Sheet (Dinners and Optional Events tabs). The page links out to it; guests type their name in a cell.
- Organizers edit the page by changing the `EDIT HERE` data block (LINKS, SCHEDULE, PACKING, CONTACTS).

## Capabilities and Constraints
- Must keep: the full-screen "Powder Pilgrimage" intro banner, the falling snow, the day-by-day schedule that tracks scroll progress, and the packing checklist that saves on the device.
- Schedule details, contacts, meeting point and room assignments are still TBA placeholders.
- Public page: no house addresses or phone numbers.

## Brand Commitments
- Black and yellow (maize) palette, from the club's info-session deck. User confirmed they like it.
- "Niseko 2027: Powder Pilgrimage" cover art (`img/hero.jpg`), taken from the deck.
- Voice: ski-bum storyteller. Some color and excitement about powder, onsen and Hokkaido, but practical and clear where it matters (deadlines, flights, sign-ups).
- Spell out "Ross Ski & Snowboard Club" once near the top; RSSC after that.

## Evidence on Hand
- Info-session deck facts: about 50 ft of snow a season, 4 resorts on the Ikon Pass, 2,191 acres; arrive CTS by 3 PM Jan 3, chartered bus at 4 PM; houses Mori C (sleeps 7, 2 bathrooms) and Whiskey Woods (sleeps 10, 5 bathrooms, tatami room); add-on prices.
- No photos ship besides the cover art and trail map. No testimonials or past-trip photos exist; do not invent any.

## Product Principles
- Answer the question before it hits the group chat.
- Phones first: thumb-reachable, fast, readable outdoors.
- Practical facts stay plain; the stoke lives around them, never instead of them.
- Easy for organizers to update without touching layout code.
