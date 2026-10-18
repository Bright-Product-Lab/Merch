# I Tape Plays

No-server storefront. Data lives in the visitor's browser (localStorage key `snapshotz.store.v4`); export from Backend → Stats & data for backup.

## Deploy
Upload `index.html` and `reel-bin-app.html` together to any static host (GitHub Pages, Netlify, Cloudflare Pages). `reel-bin-app.html` must sit beside `index.html`.

## Layout
- `index.html` – bundled, self-contained site (generated; don't edit)
- `reel-bin-app.html` – Clip Maker download
- `source/SnapShotz Store.dc.html` – editable source (Design Component)
- `source/SnapShotz Store -standalone src-.dc.html` – same source plus bundler thumbnail, input for rebuilding `index.html`
- `source/support.js`, `source/assets/` – runtime and images (`tape-mark.png` is the logo)

## Routes
`#/` home, `#/reels`, `#/app`, `#/training`, `#/book`, `#/merch`, `#/clips/<link-name>` customer clip gallery, `#admin` backend (6-digit code).

## Notes
- Backend code is casual protection only, not server security.
- Edits made in Backend stay in that browser. To ship content to all visitors, bake it into `seed()` in the source and rebuild.
- Clips: file/preview links point to external hosting; unlock codes are checked in the browser. Gumroad recommended for paid delivery.
- Formspree endpoint (contact form) is set in Backend → Branding.
