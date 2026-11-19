# Ligno Pack Builder, password-protected version (standalone page)

`index.html` holds the encrypted application (AES-256-GCM) and a login page. The password entered decrypts the application in the browser; nothing is sent to a server and no account is needed. Three passwords are accepted (one per person); to remove or change one, ask Claude to rebuild the page.

Going online: drop the files of this folder on any static hosting (Cloudflare Pages "Upload assets", Netlify Drop, GitHub Pages, any web host). The address must be https (the default at these hosts): in-browser decryption requires it.

Files: `index.html` (application + login), `_headers` (security headers for Cloudflare Pages or Netlify), `robots.txt` (no indexing), `404.html`.

Saved packs: in each person's browser. To pass a composition on: Export Excel or Copy summary. "Remember on this device" keeps the key in the browser; do not tick it on a shared computer.

`configurateur.html`: the page "Ligno: configurator, where we stand" (demonstration of the engine and the generator, in 3D, French and English), protected by the same three passwords; its content key is sealed by the site key, so "Remember on this device" covers both pages. Address: the application's, followed by `configurateur.html`.

`avec-mes-pieces.html`: the page "Ligno: with my pieces" (path A of the configurator, internal version: pick packs or pieces, catalogue models you can build, step-by-step 3D assembly; catalogue only, no generation on demand), protected by the same three passwords, key sealed the same way. Address: the application's, followed by `avec-mes-pieces.html`.
