# Conny Scheitz — website (v2)

Plain HTML/CSS/JS. No build step, no framework — any static file host works.

## Files
- `index.html` — home page
- `about.html` — bio, "What drives me", career timeline
- `passthemic.html` — #PassTheMic intro + conversation slider (1 real entry, extensible)
- `talks.html` — speaking themes, "recent conversations" placeholder, contact CTA
- `community.html` — mentorship / alumni / community roles
- `contact.html` — contact info (placeholder email — see below)
- `styles.css` — all styling
- `script.js` — mobile menu toggle only
- `images/passthemic-*.jpg` — the real published graphics for each #PassTheMic conversation, pulled from the docs in your Drive's "Posted" folder (Kate Adam, Ariane Wilson, Daisy Heinsen, Danny Ryan). Mei-yen Shipek's write-up is in too, but her source doc was too large to export automatically — send that image separately.

## Adding a new #PassTheMic conversation
Also add a line to the `.article-list` in the "All articles" section at the bottom of `passthemic.html`.
In `passthemic.html`, inside `.mic-slider`, copy the first `<a class="mic-card">` block and swap in:
image path, the guest's name (eyebrow), the post title, a one-line description, and the real LinkedIn post permalink (`href`).

## Still needs from you
- **Email address** for the Contact page — currently a placeholder (`hello@example.com`) in `contact.html`.
- **Facebook / Instagram URLs** — footer links are still `#` placeholders on every page.
- **Recent talks** — dates, venues, links — for the "Recent conversations" section on `talks.html`.
- Two Community org names (Beyond the Pond, Alumni & Friends Stiftung GmbH) only have short tags — send a line on each if you want fuller descriptions.

## Run it locally
Open `index.html` directly in a browser, or serve it:
```
cd site
python3 -m http.server 8000
```
Then visit http://localhost:8000

## Self-hosting options
**Simplest (free, no server to manage):**
- Netlify or Vercel: drag the `site` folder into their dashboard, or connect a GitHub repo — done in a couple of minutes.
- GitHub Pages: push this folder to a repo and enable Pages in the repo settings.

**Your own server (VPS, e.g. via nginx):**
1. Copy the folder to the server, e.g. `/var/www/connyscheitz`.
2. Point an nginx `server` block's `root` at that folder.
3. Point your domain's DNS A/AAAA record at the server's IP, then add HTTPS (Certbot/Let's Encrypt is the usual free option).

## Known follow-ups
- All photos are now local files in `images/` (hero, banner, About portrait, "What Drives Me" cards, #PassTheMic cards). Nothing is hot-linked from Wix anymore.
- Social links (LinkedIn, Facebook, Instagram) and the policy links in the footer are placeholders (`#`) — the versions on the Wix site pointed to Wix's own demo pages, not real accounts. Swap in the real URLs when ready.
- About, #PassTheMic, and Talks & Events are placeholder pages since those routes weren't published on the source site yet.
