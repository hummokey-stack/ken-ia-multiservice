# /ken

> Reprendre exactement là où on s'était arrêté sur le projet de prospection N8N.

---

## Ce que tu dois faire quand je lance `/ken`

### Étape 1 — Charger le contexte de session

Lis dans cet ordre :
1. `context/CONTEXT.md`
2. La mémoire projet : cherche dans ta mémoire le fichier `project-prospection-n8n`
3. Le fichier `projects/prospection-auto/setup.md`

### Étape 2 — Me résumer où on en est

Présente-moi ce résumé :

```
🔁 Reprise du projet Prospection N8N

**Ce qui est déjà fait :**
- 4 workflows N8N créés et sur GitHub (01-radar, 02-tirs, 03-reponses, 04-relances)
- Accès N8N vérifié : https://n8n.srv1113074.hstgr.cloud (100 workflows, API OK)
- .env rempli avec Twilio, VPS, N8N

**Ce qui reste à faire :**
1. Créer Google Sheets CRM "KEN Digital CRM" (onglets Prospects + Pipeline) → coller ID dans .env
2. Activer Google Places API → coller clé dans .env
3. Créer OAuth2 Google Cloud (Client ID + Secret) → coller dans .env
4. Configurer credentials Twilio + Gmail dans N8N (noms : "Twilio - KEN Digital", "Gmail - KEN Digital")
5. Ajouter variables dans N8N > Settings > Variables
6. Importer les 4 workflows JSON dans N8N
7. Configurer webhook Twilio → URL webhook workflow 03-reponses
8. Activer les 4 workflows dans l'ordre

Par où veux-tu commencer ?
```

### Étape 3 — Attendre mes instructions

Ne lance rien de toi-même. Attends que je choisisse par quelle étape reprendre.
