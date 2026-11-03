# Universal Planet Gym

A responsive website for Universal Planet Gym in Taytay, Rizal, built with HTML, CSS, and locally bundled jQuery.

The design uses a black-and-lime strength campaign hero, rectangular community photography, a light gym introduction, a clear **₱500 monthly membership**, FAQs, and direct Facebook/Waze links. The circular gym logo is preserved.

## Run locally

No installation, API keys, or build step is required. From the repository root:

```sh
python3 -m http.server 8080 --directory dist
```

Open `http://localhost:8080`.

## Structure

- `dist/index.html` — page content, membership, contact links, FAQs, and photo dialog
- `dist/styles.css` — design tokens and responsive layouts
- `dist/app.js` — mobile navigation, photo viewer, and jQuery animations
- `dist/assets/` — reference image, decorative hero, display font, and jQuery with licenses
- `PROJECT_PLAN.md` — three-phase plan, sources, and verification status
- `.openai/hosting.json` — existing Sites deployment configuration

## Interactions

The mobile menu, photo viewer, keyboard controls, and native FAQ details work without jQuery. The locally bundled full jQuery 4.0.0 build adds entrance/scroll reveals, smooth anchor navigation, menu and FAQ slides, and photo fades. Motion respects `prefers-reduced-motion`, including changes while the page is open.

Facebook links open the gym's page. Visitors choose Message there; the website does not send messages, collect personal details, accept payments, or book visits.

## Content and imagery

The supplied Facebook screenshot is the source for the logo, actual community photographs, 20+ years of history, equipment, trainers, and open-daily information. The project owner's updated **₱500/month** price supersedes the older screenshot's fee statement. Confirm exact hours, membership inclusions, and separate coaching fees with the gym.

`iron-hero.png` is an AI-generated decorative equipment photograph, not a photograph of the actual premises. See `dist/assets/ASSET_NOTES.md` for provenance and the generation prompt. The real community photos remain limited by the resolution of the supplied screenshot.

## Validation

```sh
node --check dist/app.js
node --check dist/assets/vendor/jquery-4.0.0.min.js
git diff --check
```

JavaScript syntax, local asset references, navigation anchors, unique IDs, HTML structure, and updated pricing were checked. Browser visual and interaction verification for this redesign remains unverified: automatic browser approval review was blocked by a session usage limit. Prior-version browser results do not validate this redesign.

## Hosting

Upload the contents of `dist/` to a static host. When changing the live domain, update the canonical and Open Graph URLs in `dist/index.html`. The existing Sites deployment is private; committing this repository does not enable GitHub Pages.
