# Ligno Pack Builder, password-protected version (standalone page)

`index.html` holds the encrypted application (AES-256-GCM) and a login page. The password entered decrypts the application in the browser; nothing is sent to a server and no account is needed. Three passwords are accepted (one per person); to remove or change one, ask Claude to rebuild the page.

Going online: drop the files of this folder on any static hosting (Cloudflare Pages "Upload assets", Netlify Drop, GitHub Pages, any web host). The address must be https (the default at these hosts): in-browser decryption requires it.

Files: `index.html` (application + login), `_headers` (security headers for Cloudflare Pages or Netlify), `robots.txt` (no indexing), `404.html`.

Saved packs: in each person's browser. To pass a composition on: Export Excel or Copy summary. "Remember on this device" keeps the key in the browser; do not tick it on a shared computer.
