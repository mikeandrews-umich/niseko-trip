# RSSC Niseko trip site

One static page: `index.html` plus photos in `img/`. No build step.

## Editing
Open `index.html` and scroll to the `EDIT HERE` block near the bottom:

- `SCHEDULE`: add items to `morning` / `afternoon` / `evening` for each day.
  `type: "inc"` = included (maize), `"opt"` = optional (dashed), `"plain"` = no tag.
  ```js
  { day:"Day 01", name:"Sunday", date:"Jan 3",
    afternoon:[{t:"Arrive CTS", type:"plain"}, {t:"Private shuttle to Niseko", type:"inc"}] }
  ```
- `PACKING`: packing list groups and items.
- `CONTACTS`: role, name, email, phone (phone gets Call/Text buttons).

Anything still marked "TBA" in the HTML (meeting point, room assignments, add-on sign-up) is plain text you can edit in place.

## Preview locally
```
python -m http.server 8000
```
then open http://localhost:8000.

## Deploy
- **Netlify Drop** (fastest): drag this folder onto https://app.netlify.com/drop.
- **GitHub Pages**: push to a repo → Settings → Pages → deploy from `main` / root.
