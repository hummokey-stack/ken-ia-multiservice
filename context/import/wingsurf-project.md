# Projet : windsurfoil.shop — Contexte complet

> Fichier de sauvegarde du projet client windsurfoil.shop.
> Consulté automatiquement via la commande /wingsurf.
> Dernière mise à jour : 2026-05-21

---

## Identité du projet

- **Client :** propriétaire de windsurfoil.shop (client de Ken)
- **Site live :** https://windsurfoil.shop
- **Type :** e-commerce PHP/SQLite — sports de glisse (wingsurf, kitesurf, surf, SUP, foil...)
- **Fichiers locaux :** `C:\xampp\htdocs\glisse-shop\`
- **Hébergeur :** Hostinger (hébergement mutualisé du client, séparé du VPS de Ken)

---

## Accès et credentials

| Service | Valeur |
|---------|--------|
| FTP Hôte | `82.25.113.59` |
| FTP Utilisateur | `u307387390.windsurfoil.shop` |
| FTP Mot de passe | `Tomate2020@@` |
| FTP Port | `21` (avec TLS explicite + mode passif dans FileZilla) |
| Chemin serveur | `/home/u307387390/domains/windsurfoil.shop/public_html/` |

**Contraintes d'accès :**
- Le FTP curl fonctionne uniquement vers la racine (les sous-dossiers bloquent avec exit code 56)
- Le serveur a une protection bot (Hostinger CDN challenge JS) qui bloque les requêtes curl HTTP
- SSH port 22 : fermé sur ce serveur mutualisé
- API Hostinger : ne donne pas accès aux fichiers mutualisés
- La seule méthode de déploiement fiable est **FileZilla** (protocole FTP, TLS explicite, mode passif)

---

## Architecture technique

```
glisse-shop/
├── index.php               Page d'accueil
├── produit.php             Fiche produit
├── categorie.php           Page catégorie
├── panier.php              Panier (localStorage)
├── commande.php            Tunnel de commande + WhatsApp
├── occasion.php            Produits d'occasion
├── promotions.php          Promotions
├── blog.php / article.php  Blog
├── a-propos.php            À propos
├── contact.php             Contact
├── livraison.php           Livraison
├── admin/                  Back-office (gestion produits, commandes, settings)
├── assets/
│   ├── css/                Styles
│   ├── js/                 Scripts
│   └── images/             Médias
├── includes/
│   ├── header.php          En-tête commun
│   ├── footer.php          Pied de page commun
│   ├── db.php              Connexion SQLite + init base
│   ├── functions.php       Fonctions utilitaires
│   ├── auth.php            Authentification admin
│   └── product-card.php    Composant carte produit
└── data/
    └── shop.db             Base de données SQLite
```

**Stack :** PHP 8.2 + SQLite (pas MySQL), vanilla JS, CSS custom, Font Awesome, Google Fonts (Rajdhani)

---

## Base de données SQLite

Fichier : `data/shop.db`

**Tables :**
- `settings` — paramètres du site (nom, email, téléphone, whatsapp, réseaux sociaux...)
- `produits` — catalogue (nom, slug, catégorie, marque, prix, stock, images, variantes...)
- `categories` — arborescence catégories (11 catégories principales + sous-catégories)
- `commandes` — commandes clients (référence, client, articles JSON, total, statut)
- `admin` — login admin (login: `admin`, password SHA256 de `admin123`)
- `newsletter` — abonnés newsletter
- `blog` — articles de blog
- `produit_variations` — variantes de produits

---

## Modifications déjà effectuées (2026-05-21)

### 1. Bouton "Valider ma commande" → redirige vers WhatsApp
- **Fichier :** `commande.php`
- **Fonctionnement :** quand le client clique, WhatsApp s'ouvre avec le message pré-rempli contenant tous les détails de la commande (nom, adresse, articles, total)
- **Numéro WhatsApp configuré :** `+33 7 56 80 29 95` (numéro France du client)
- **Stockage :** colonne `whatsapp` dans la table `settings`, valeur `33756802995`
- **Déployé :** oui, `commande.php` uploadé sur le serveur live

### 2. Bug SQL corrigé — admin/produits.php
- **Erreur :** `SQLSTATE[HY000]: General error: 1 ambiguous column name: nom`
- **Cause :** requête avec JOIN entre `produits` et `categories` (deux colonnes `nom`) sans préfixe de table
- **Correction ligne 36 :** `(nom LIKE :q OR marque LIKE :q)` → `(p.nom LIKE :q OR p.marque LIKE :q)`
- **Fichier local corrigé :** oui (`C:\xampp\htdocs\glisse-shop\admin\produits.php`)
- **Déployé sur live :** NON — bloqué par les limitations FTP/bot protection
- **Action requise :** uploader `admin/produits.php` via FileZilla

---

## Ce qui reste à faire

- [ ] Déployer `admin/produits.php` corrigé via FileZilla (correction bug SQL ligne 36)
- [ ] Vérifier que le bouton WhatsApp fonctionne correctement sur le site live
- [ ] Tester le tunnel de commande complet sur https://windsurfoil.shop/commande.php

---

## Comportement de déploiement

Pour déployer un fichier modifié sur le live :

**Via FileZilla (méthode recommandée) :**
1. Hôte : `82.25.113.59`, User : `u307387390.windsurfoil.shop`, Pass : `Tomate2020@@`, Port : `21`
2. Protocole FTP, Chiffrement TLS explicite, Mode passif
3. Glisser-déposer le fichier local vers le chemin correspondant sur le serveur

**Via curl FTP (fonctionne uniquement pour la racine) :**
```bash
curl -T fichier.php "ftp://82.25.113.59/fichier.php" --user "u307387390.windsurfoil.shop:Tomate2020@@" --ftp-pasv
```

**Via script PHP temporaire (pour modifier la BDD) :**
- Uploader un script `.php` à la racine via curl FTP
- L'accéder via `curl -s -L https://windsurfoil.shop/script.php`
- Le script s'auto-supprime avec `unlink(__FILE__)`
