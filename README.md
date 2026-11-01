# Lavash Restaurant — concept demo

A static, mobile-first pitch concept for Lavash Restaurant in Yerevan. Plain HTML, CSS and JavaScript; no build step or backend.

**Live demo:** https://robertp0ghosyan.github.io/lavash.github.io/

## Run locally

From this folder:

```bash
python -m http.server 8000
```

Open `http://localhost:8000`. GitHub Pages deploys the root of the `main` branch automatically.

## Edit before publication

- `js/main.js`: all translated UI copy, sample dishes, menu items, prices, gallery metadata, quotes, contact config and reservation API setting. The `MENU` array is the single source of menu items.
- `assets/`: all photographs are stored locally so the demo does not depend on remote image servers. `restaurant-interior.jpg` comes from [Lavash's own menu site](https://lavash.yeremyan.am/arm/groups); `official-*.jpg` comes from [Yeremyan Projects' Lavash gallery](https://www.yeremyanprojects.com/en/restaurants/lavash). `restaurant-entrance.jpg` is a photograph of the actual entrance from [Armenia Discovery](https://armeniadiscovery.com/en/articles/best-restaurants-in-yerevan). `restaurant-terrace.jpg` comes from the reference screenshot supplied by the user. Confirm usage rights for the first-party and third-party images before production use.
- `index.html`: metadata, map embed, contact links and JSON-LD. The address and two phone numbers are from the official Yeremyan Projects page. Opening hours were not verified, so the site asks visitors to call and the structured data leaves `openingHours` empty. Add verified hours to the page and JSON-LD when supplied.
- Sample prices and guest sentiments are explicitly labeled. Replace them with approved data. Dish imagery is illustrative of the concept and may not match current menu availability.

The reservation form validates locally. Until a backend exists, it never claims to have sent a booking. Set `CONFIG.API_ENDPOINT` in `js/main.js` and connect its `fetch` request to a reservation API; update the success copy once the API confirms bookings.

## Sources

- [Lavash / Yeremyan Projects](https://www.yeremyanprojects.com/en/restaurants/lavash): address, phone, restaurant description and source gallery.
- [UNESCO — Lavash tradition](https://ich.unesco.org/en/RL/le-lavash-preparation-signification-et-aspect-du-pain-traditionnel-en-tant-qu-expression-culturelle-en-armenie-00985): heritage claim.

The layout is designed for 360, 768, 1024 and 1440 px widths and honours reduced-motion preferences. Serve the entire project folder, not `index.html` alone, so the local `assets/` paths resolve.

