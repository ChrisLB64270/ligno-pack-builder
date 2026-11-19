# Ligno Pack Builder, password-protected version (standalone page)

`index.html` holds the encrypted application (AES-256-GCM) and a login page. The password entered decrypts the application in the browser; nothing is sent to a server and no account is needed. Three passwords are accepted (one per person); to remove or change one, ask Claude to rebuild the page.

Going online: drop the files of this folder on any static hosting (Cloudflare Pages "Upload assets", Netlify Drop, GitHub Pages, any web host). The address must be https (the default at these hosts): in-browser decryption requires it.

Files: `index.html` (application + login), `_headers` (security headers for Cloudflare Pages or Netlify), `robots.txt` (no indexing), `404.html`.

Saved packs: in each person's browser. To pass a composition on: Export Excel or Copy summary. "Remember on this device" keeps the key in the browser; do not tick it on a shared computer.

`configurateur.html`: the page "Ligno: configurator, where we stand" (demonstration of the engine and the generator, in 3D, French and English), protected by the same three passwords; its content key is sealed by the site key, so "Remember on this device" covers both pages. Address: the application's, followed by `configurateur.html`.

`avec-mes-pieces.html`: the page "Ligno: with my pieces" (path A of the configurator, internal version: pick packs or pieces, catalogue models you can build, step-by-step 3D assembly; catalogue only, no generation on demand), protected by the same three passwords, key sealed the same way. Address: the application's, followed by `avec-mes-pieces.html`.

Version v12 (20/11/2026): only models validated by the Ligno engine are shown. The v11 application stays encrypted as it was (block `P`); an encrypted patch (block `Q`, its own key sealed by the site key, like the other pages) is applied in the browser when the page opens: it removes the former builds (drawings composed by roles, inventory check only, 41 of 42 refused by the engine) and shows instead the models of the verified catalogue, with the step-by-step 3D build and generation on demand by the configurator server. If the patch does not apply, a red banner says so.

`modeles-verifies.txt`: the verified catalogue read by the Pack Builder (1,363 models validated by the engine on 20/11/2026), encrypted the same way; meshes and the server address are read from `avec-mes-pieces.html`. Sources and build tools: private repository `cat-apac/ligno-configurateur`, `moteur/tools/pack_builder_patch.py` and `moteur/tools/pack_builder_models.py`.
