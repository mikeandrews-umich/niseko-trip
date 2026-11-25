# RSSC Niseko trip site

One static page: `index.html` plus photos in `img/`. No build step.

## Editing
Open `index.html` and scroll to the `EDIT HERE` block near the bottom:

- `LINKS`: the add-ons and dinner sign-up sheet URLs, plus deadlines. Buttons say "Link coming soon" while a URL is empty.
- `SCHEDULE`: add items to `morning` / `afternoon` / `evening` for each day.
  `type: "inc"` = included (solid maize block), `"opt"` = optional (maize outline), `"plain"` = plain line.
  A day with no items collapses to one line marked "Plan TBA".
  Add `link: "dinners"` or `link: "addons"` to an item to show a sign-up link.
  Add `map: "Place name, Niseko"` to an item (or a meetup) to show a "Map" link that searches Google Maps.
  Set `title` for the day's headline.
  ```js
  { day: 1, name: "Sunday", date: "2027-01-03", title: "Arrival day",
    afternoon:[{t:"Arrive CTS", type:"plain"}, {t:"Private shuttle to Niseko", type:"inc"}] }
  ```
- `afterDark` (optional, per day): the night plan shown in a framed "After dark" panel under Evening.
  `theme` (a chip, leave "" for none), `items` (same shape as slot items, [] for none) and
  `meetup: { name, note, link }` (the bar to meet at).
- `PACKING`: packing list groups and items.
- `CONTACTS`: role, name, email, phone (phone gets Call/Text buttons).

Anything still marked "TBA" in the HTML (meeting point, room assignments, add-on sign-up) is plain text you can edit in place.

## Preview locally
```
python -m http.server 8000
```
then open http://localhost:8000.

## Deploy
GitHub Pages serves `main` at https://rossjapow.com. Commit and push; it updates in about a minute.
See HANDOFF.md for the full picture (domain, intro animation, open items).
