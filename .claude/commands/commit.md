# /commit

> Commande pour sauvegarder le workspace avec git.

---

## Mission

Quand je lance `/commit`, exécute la séquence suivante :

### Étape 1 : Vérifier l'état du dépôt

Lance `git status` pour voir les fichiers modifiés, ajoutés ou supprimés.

Si git n'est pas initialisé, lance `git init` puis configure le dépôt.

### Étape 2 : Afficher le résumé des changements

Présente-moi la liste des fichiers modifiés de manière lisible :

```
Voici ce qui sera sauvegardé :

Fichiers modifiés :
- [liste des fichiers]

Fichiers nouveaux :
- [liste des fichiers]

Fichiers supprimés :
- [liste des fichiers]
```

### Étape 3 : Proposer un message de commit

Génère automatiquement un message de commit clair en français qui résume les changements détectés.

Format : `[date] - [résumé des changements en une ligne`

Exemple : `2026-05-19 - Ajout livrables, gestion secrets et commande commit`

Demande-moi si je veux garder ce message ou le modifier.

### Étape 4 : Exécuter le commit

Lance les commandes dans cet ordre :

```bash
git add .
git commit -m "[message validé]"
```

### Étape 5 : Confirmer

Affiche un message de confirmation :

```
Sauvegarde effectuée. Commit : [message]
[nombre] fichiers sauvegardés.
```

---

## Règles importantes

- Ne jamais committer le fichier `.env` (il est dans `.gitignore`, mais reste vigilant)
- Si un remote (GitHub, GitLab) est configuré, demande-moi si je veux aussi pusher
- Si git n'est pas installé sur la machine, signale-le clairement et propose des alternatives
- Pas de tirets longs dans les réponses
- Répondre en français
