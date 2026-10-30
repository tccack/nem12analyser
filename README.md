# Battery Sizer SA (public build)

A single-page tool for homeowners. It reads a NEM12 meter file in the browser, sizes a battery,
inverter and solar array, and shortlists systems. Nothing is uploaded; there is no server.

## Files
- `index.html` - the whole site (data and code embedded)
- `LICENSE` - all rights reserved
- `_headers` - security headers (used by Cloudflare Pages; ignored by GitHub Pages)
- `.nojekyll` - tells GitHub Pages to serve the files as they are

## Deploy on Cloudflare Pages
1. Cloudflare dashboard > Workers & Pages > Create > Pages > connect this GitHub repository.
2. Build command: none. Output directory: `/` (the repository root).
3. Later: add a custom domain, Australia-only firewall rule, rate limiting and Web Analytics.
   To keep it private while testing, protect it with Cloudflare Access (allow your own email only).

## Deploy on GitHub Pages
Settings > Pages > Deploy from a branch > `main` / root. Note: the published site is public
even if the repository is private (needs a paid plan for private repositories).

## Do NOT upload to this repository
The database (`energy_sizing.db`), the CSV tables, build scripts, any station or NMI data,
or the private ranking notes. Keep those in a separate private repository.

## `noindex`
`index.html` asks search engines not to list it. Remove the `robots` meta tag when you want it findable.
