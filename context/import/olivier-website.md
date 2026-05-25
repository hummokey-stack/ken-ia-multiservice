# Projet : keniaagency.netlify.app — Site web KEN IA MULTISERVICE

> Fichier de sauvegarde du site web personnel de Ken.
> Consulté automatiquement via la commande /olivier.
> Dernière mise à jour : 2026-05-21

---

## Identité du projet

- **Site live :** https://keniaagency.netlify.app
- **Dépôt GitHub :** https://github.com/hummokey-stack/ken-ia-multiservice
- **Fichiers locaux :** `C:\Users\KEN MASTER\Desktop\jarvis-starter-kit\website\`
- **Hébergement :** Netlify (déploiement automatique depuis GitHub branche `main`)
- **Config Netlify :** `netlify.toml` à la racine — `publish = "website"`
- **Type :** Site vitrine one-page HTML/CSS/JS vanilla

---

## Déploiement

Tout push sur `main` déclenche un redéploiement Netlify automatique (1-2 min).

```bash
# Modifier en local → commit → push = live
git add website/
git commit -m "message"
git push origin main
```

---

## Structure des fichiers

```
website/
├── index.html          Page principale (tout le site)
├── assets/
│   ├── ken-logo.png         Logo principal (NE PAS convertir en WebP)
│   ├── ken-logo-full.png    Logo complet (NE PAS convertir en WebP)
│   └── ken-mark.png         Marque/icône (NE PAS convertir en WebP)
└── images/
    └── *.webp               Toutes les images converties en WebP
```

**Règle importante :** Les fichiers dans `assets/` sont des logos — ne jamais les convertir en WebP ni changer leur extension dans le HTML.

---

## Stack technique

- HTML5 / CSS3 custom (variables CSS oklch, responsive)
- JavaScript vanilla
- Fonts : Space Grotesk, Inter, JetBrains Mono (Google Fonts)
- Icônes : Font Awesome
- Pas de framework, pas de build tool

---

## Modifications effectuées (2026-05-21)

### 1. Slider d'images hero
- Slider full-width avec 5 images en en-tête
- Auto-play, swipe mobile, indicateurs dots, pause on hover

### 2. Intégration des images restantes
- Strip visuel 3 colonnes après le marquee
- Backgrounds sur les cartes de services (opacité 0.06-0.13)
- Section portfolio 4 colonnes avant le CTA

### 3. Contacts réels ajoutés
- Téléphones : +237 654 270 447 et +237 692 105 983
- Email : olivierkedinta@gmail.com
- Popup WhatsApp flottant (FAB vert, auto-ouverture 6s, lien wa.me/237654270447)

### 4. Optimisation images — WebP
- 20 images converties PNG/JPG → WebP
- Gain : 27.4 Mo → 2.5 Mo (-91%)
- Logos `assets/` conservés en PNG
- Références mises à jour dans index.html

### 5. OG Tags + SEO
- `og:title`, `og:description`, `og:image`, `og:url`, `og:type`, `og:locale`, `og:site_name`
- `twitter:card` summary_large_image
- `meta name="description"` pour Google
- Image OG : `images/Gemini_Generated_Image_7sgqob7sgqob7sgq.webp`

---

## Paramètres importants

| Variable | Valeur |
|----------|--------|
| URL live | https://keniaagency.netlify.app |
| WhatsApp contact | +237 654 270 447 |
| Email contact | olivierkedinta@gmail.com |
| Téléphone 2 | +237 692 105 983 |
| Image OG | images/Gemini_Generated_Image_7sgqob7sgqob7sgq.webp |

---

## Ce qui pourrait être fait ensuite

- Ajouter un favicon
- Ajouter un domaine personnalisé sur Netlify
- Ajouter Google Analytics / tracking
- Créer des pages séparées (services, portfolio, contact)
- Ajouter un formulaire de contact fonctionnel
