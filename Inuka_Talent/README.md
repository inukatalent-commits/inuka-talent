# Inuka Talent — site officiel

Site statique (HTML/CSS/JS, sans build) du concours Inuka Talent, Goma, RDC.

## Structure
- `index.html` accueil · `apropos.html` · `artistes.html` · `contact.html` · `404.html`
- `assets/` logos et photos · `hero/` visuels du carrousel · `art/` images des artistes
- `netlify.toml` configuration Netlify (cache, en-têtes de sécurité)
- `robots.txt`

## Mettre en ligne avec GitHub + Netlify
1. Crée un dépôt sur github.com (ex. `inuka-talent`), puis envoie-y **le contenu** de ce dossier (pas le dossier lui-même) : *Add file → Upload files*, ou en ligne de commande :
   ```
   git init && git add . && git commit -m "Site Inuka Talent"
   git branch -M main
   git remote add origin https://github.com/TON-COMPTE/inuka-talent.git
   git push -u origin main
   ```
2. Sur netlify.com : *Add new site → Import an existing project → GitHub*, choisis le dépôt.
3. Réglages de build : **Build command** vide, **Publish directory** `.` (déjà dans `netlify.toml`). Clique *Deploy*.
4. (Option) *Domain management* pour ajouter ton nom de domaine ; le HTTPS est automatique.

Alternative rapide sans GitHub : glisse-dépose le dossier sur https://app.netlify.com/drop

## Modifier le site
- Nombre de candidats inscrits : dans `index.html`, cherche `INSCRITS=0,MAX=300` et change `INSCRITS`.
- Chaque modification poussée sur GitHub redéploie automatiquement le site.

## À faire une fois le domaine connu
- Ajouter `<link rel="canonical">` et une image `og:image` (URL absolue), puis un `sitemap.xml`.
- Formulaire de contact : il ouvre actuellement le client mail du visiteur (`mailto:`).
