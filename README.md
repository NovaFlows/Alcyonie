# Site Alcyonie

Site vitrine d’Alcyonie, Céline Delohen. Une seule page, sans base de données, sans cookie et sans outil de statistiques.

## Contenu du dossier

| Fichier | Rôle |
|---|---|
| `index.html` | Tout le site : textes, mise en page et animations |
| `assets/` | Logo, portrait, icônes et image de partage (réseaux sociaux) |
| `fonts/` | Polices Newsreader et Albert Sans, hébergées sur le site (aucun appel à Google) |
| `robots.txt`, `sitemap.xml` | Référencement (le sitemap apparaît une fois le domaine renseigné) |
| `_headers` | Réglages de sécurité et de cache pour Netlify ou Cloudflare Pages |
| `vercel.json` | Les mêmes réglages pour Vercel |
| `favicon.ico` | Icône de l’onglet du navigateur |

## Modifier le site

- **Téléphone, e-mail, Instagram, adresses des cabinets, SIRET** : en bas de `index.html`, dans l’objet `SITE`. Les liens d’appel, d’e-mail et d’itinéraire se mettent à jour tout seuls.
- **Textes** : chaque section commence par un repère du type `<!-- ============ POUR LES STRUCTURES ============ -->`. Il suffit de chercher ce repère.
- **Tarifs** : directement dans les cartes « Particuliers » (rubrique `rates`) et dans la question « Quels sont les tarifs ? ».
- **Photo** : remplacer `assets/celine-delohen.webp` par une image au même nom (format portrait 4:5, environ 800 × 1000 px).
- **Repères « À compléter »** : ils s’affichent en pointillés bordeaux sur le site et se cherchent avec le mot `todo`.

## Mise en ligne (GitHub + hébergeur)

1. **GitHub** : créer un compte au nom de Céline, puis un dépôt (par exemple `alcyonie-site`). Dans le dépôt, *Add file → Upload files*, glisser **le contenu** de ce dossier (pas le dossier lui-même), puis *Commit changes*.
2. **Hébergeur** : créer un compte en choisissant *Se connecter avec GitHub*, puis importer le dépôt.
   - Aucun réglage de construction : pas de commande de build, dossier de publication = racine du dépôt.
   - Le site est en ligne en une minute sur une adresse provisoire (`…netlify.app` ou `…vercel.app`).
3. **Domaine (OVH)** : dans l’hébergeur, ajouter le domaine (`domaine.fr` et `www.domaine.fr`). L’hébergeur affiche les enregistrements DNS à créer. Dans OVH, *Noms de domaine → Zone DNS* : remplacer l’enregistrement **A** du domaine et le **CNAME** `www` par ces valeurs, et supprimer les anciens qui pointent vers OVH. La prise en compte prend de quelques minutes à quelques heures. Le HTTPS s’active ensuite automatiquement.
4. **Après le domaine** : compléter les balises `canonical` et `og:` en tête de `index.html` (repère « À activer une fois le nom de domaine choisi ») et ajouter un `sitemap.xml`.

Chaque modification enregistrée sur GitHub est remise en ligne automatiquement en une minute environ.

## Avant l’ouverture au public

- **Mentions légales** (fenêtre en pied de page) : compléter l’adresse du siège et l’hébergeur (nom, adresse, téléphone).
- **Vercel** : l’offre gratuite (Hobby) est réservée à un usage personnel non commercial. Pour un site professionnel, il faut l’offre Pro. Netlify et Cloudflare Pages acceptent les sites professionnels dans leur offre gratuite.
