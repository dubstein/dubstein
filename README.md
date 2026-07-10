# willsteinfeld.com — static site

Ready to push straight to a GitHub repo and serve with GitHub Pages.

## Deploy with GitHub Pages
1. Create a new GitHub repo and push the contents of this folder to it (as the root, or to a `docs/` folder — your choice).
2. In the repo's Settings → Pages, set the source to the branch/folder you pushed to.
3. Your site will be live at `https://<username>.github.io/<repo>/` — `index.html` (a copy of the homepage) is the entry point.

## Structure
- `index.html` / `Home.dc.html` — homepage (same content, `index.html` exists so GitHub Pages has a root document)
- `About.dc.html`, `Writing.dc.html`, `Radio.dc.html` — top-level pages
- `Photo Stories.dc.html` + `Photo Story - *.dc.html` — photo story index and detail pages
- `Personal - *.dc.html` — personal project pages
- `Nav.dc.html`, `Footer.dc.html`, `PhotoStack.dc.html` — shared components used across pages
- `images/` — photos committed directly into the site
- `support.js` / `image-slot.js` — runtime the pages depend on; keep alongside the HTML files
- `.image-slots.state.json` — saved photo crop/framing data for a couple of slots; keep alongside the HTML files

All pages are plain HTML + JS — no build step needed. Keep every file in the same folder (or mirror this structure) since pages reference each other and the shared assets with relative paths.
