# Portfolio · Affissou EGBEBI

Portfolio personnel : développeur Full Stack (applications web métier, plateformes SaaS, API REST, intégration de paiements en ligne).

Site **100 % statique** (HTML + Tailwind CSS via CDN + Alpine.js). Aucune compilation, aucun `npm install` : les fichiers sont servis tels quels, donc parfaitement compatible avec GitHub Pages.

## Structure

| Fichier | Rôle |
|---|---|
| `index.html` | Accueil : hero, services, projets, à propos, témoignages, blog, contact |
| `projects.html` | Les 10 projets avec filtres par catégorie |
| `case-study.html` | Étude de cas détaillée : Stock Management |
| `blog.html` | Liste des articles |
| `blog-article.html` | Article : SaaS multi-entreprises avec Laravel |
| `blog-article-kkiapay.html` | Article : intégrer Kkiapay dans Laravel |
| `blog-article-architecture.html` | Article : Blade pour l'admin, API REST pour le public |
| `404.html` | Page d'erreur |
| `merci.html` | Page de confirmation après envoi du formulaire |
| `assets/` | Photo, avatars, visuels de couverture (SVG) et icônes |
| `favicon.ico` · `site.webmanifest` | Favicon (monogramme « AE ») et manifeste web |

## Prévisualiser en local

Ouvrir `index.html` dans un navigateur suffit. Pour un rendu plus fidèle (chemins relatifs) :

```bash
python -m http.server 8000
# puis http://localhost:8000
```

## Déployer sur GitHub Pages

1. Pousser le dépôt sur GitHub (branche `main`).
2. **Settings → Pages → Build and deployment → Source : GitHub Actions**.
3. Le workflow `.github/workflows/deploy.yml` publie le site à chaque push sur `main`.

Le site sera accessible sur `https://<votre-compte>.github.io/<nom-du-depot>/`.

## À personnaliser avant publication

- [ ] **Photo** : remplacer `assets/photo-placeholder.svg` par une vraie photo, et mettre à jour le `src` dans `index.html` (2 occurrences) et dans les 3 articles de blog.
- [x] **Réseaux sociaux** : LinkedIn, GitHub et Facebook pointent vers les vrais profils. WhatsApp n'est volontairement pas affiché ; pour l'ajouter, remettre un lien `https://wa.me/<indicatif><numéro>` dans le pied de page de `index.html`.
- [ ] **Témoignages** : les 3 citations de `index.html` sont des textes à remplacer par de vrais retours clients.
- [ ] **Captures d'écran** : les visuels de `assets/projets/` sont des couvertures génériques ; les remplacer par de vraies captures rendra le portfolio nettement plus convaincant.
- [ ] **Formulaire de contact** : il passe par [FormSubmit](https://formsubmit.co). Au premier envoi depuis le site en ligne, un mail de confirmation est envoyé à `affissouegbebi@gmail.com` ; il faut cliquer sur le lien pour activer l'adresse. Après envoi, le visiteur est redirigé vers `merci.html` (l'URL absolue exigée par FormSubmit est calculée automatiquement au chargement, rien à modifier après le déploiement).

## Crédits

Design basé sur le thème [Folio](https://themewagon.com/themes/folio-html/) de [Laurent Begey](https://lbegey78.gumroad.com/), distribué par [ThemeWagon](https://themewagon.com) sous licence MIT. Contenus, textes et adaptation : Affissou EGBEBI.
