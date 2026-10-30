# Battery Sizer SA (public build)

A single-page homeowner tool. It reads a NEM12 meter file in the browser, sizes a battery,
inverter and solar array, and shortlists systems. Nothing is uploaded and there is no server.

## Layout
- `public/` - the only folder that is published (`index.html`, `_headers`, `.nojekyll`)
- `wrangler.jsonc` - Cloudflare config; publishes `./public` only
- `LICENSE` - all rights reserved
- `README.md` - this file (not published)

## Cloudflare
Build settings: no build command; deploy command `npx wrangler deploy`.
`preview_urls` is off. When ready, add a custom domain, an Australia-only firewall rule,
rate limiting and Web Analytics. To keep it private while testing, protect it with
Cloudflare Access (allow your own email only).

## Do not add to this repository
The database, CSV tables, build scripts, station or NMI data, or ranking notes.
Keep those in a separate private repository.

## noindex
`public/index.html` asks search engines not to list it. Remove the `robots` meta tag when you want it findable.
