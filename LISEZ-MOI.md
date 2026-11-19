# Ligno Pack Builder, version protégée par mot de passe (page autonome)

`index.html` contient l'application chiffrée (AES-256-GCM) et une page de connexion. Le mot de passe saisi déchiffre l'application dans le navigateur ; rien n'est envoyé à un serveur, aucun compte n'est nécessaire. Trois mots de passe sont acceptés (un par personne) ; pour en retirer un ou en changer, demander à Claude de reconstruire la page.

Mise en ligne : déposer les fichiers de ce dossier sur n'importe quel hébergement de pages statiques (Cloudflare Pages « Upload assets », Netlify Drop, GitHub Pages, OVH, o2switch...). L'adresse doit être en https (c'est le cas par défaut chez ces hébergeurs) : le chiffrement dans le navigateur l'exige.

Fichiers : `index.html` (application + connexion), `_headers` (en-têtes de sécurité pour Cloudflare Pages ou Netlify), `robots.txt` (pas d'indexation), `404.html`.

Packs enregistrés : dans le navigateur de chaque personne. Pour transmettre une composition : Exporter Excel ou Copier le résumé. « Se souvenir sur cet appareil » garde la clé dans le navigateur ; ne pas cocher sur un ordinateur partagé.

`configurateur.html` : page « Ligno : configurateur, où nous en sommes » (démonstration du moteur et du générateur, en 3D, français et anglais), protégée par les mêmes trois mots de passe ; sa clé de contenu est scellée par la clé du site, de sorte que « Se souvenir sur cet appareil » vaut pour les deux pages. Adresse : la même que l'application, suivie de `configurateur.html`.

`avec-mes-pieces.html` : page « Ligno : avec mes pièces » (parcours A du configurateur, version interne : choix des packs ou des pièces, modèles du catalogue réalisables, montage 3D pas à pas ; catalogue seul, sans génération à la demande), protégée par les mêmes trois mots de passe, clé scellée de la même façon. Adresse : la même que l'application, suivie de `avec-mes-pieces.html`.
