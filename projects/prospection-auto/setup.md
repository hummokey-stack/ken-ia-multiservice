# Guide de configuration — Prospection Auto N8N

## Prérequis

- N8N installé sur ton VPS (accès via navigateur)
- Compte Twilio avec WhatsApp Business activé
- Compte Google (Gmail + Google Sheets + Google Places API)

---

## Étape 1 — Google Places API

1. Va sur [console.cloud.google.com](https://console.cloud.google.com)
2. Crée un projet "KEN Digital Prospection"
3. Active l'API **Places API (New)**
4. Génère une clé API dans "Identifiants"
5. Note ta clé : `AIza...`

---

## Étape 2 — Google Sheets (CRM)

1. Crée un Google Sheets nommé **KEN Digital CRM**
2. Crée les onglets suivants :
   - **Prospects** (colonnes ci-dessous)
   - **Pipeline** (prospects qui ont répondu)

### Colonnes de l'onglet Prospects (ligne 1)

```
Nom | Secteur | Ville | Pays | Flag | Téléphone | Téléphone WA | Email | Adresse | Note Google | Nb Avis | Statut | Canal | Date Ajout | Date Contact | Date Réponse | Notes
```

### Statuts possibles

| Statut | Signification |
|--------|--------------|
| NOUVEAU | Scrappé, pas encore contacté |
| CONTACTÉ | Premier message envoyé |
| RELANCÉ | Relance J+2 ou J+5 envoyée |
| RÉPONDU | A répondu (neutre) |
| INTERET | A répondu positivement |
| REFUS | A dit non / STOP |
| CLIENT | Contrat signé |
| ARCHIVÉ | Sans réponse après J+5 |

### Colonnes de l'onglet Pipeline

```
Nom | Ville | Secteur | Canal | Type Réponse | Premier Message | Date Entrée Pipeline | Statut Pipeline | Notes
```

3. Copie l'ID du fichier dans l'URL : `https://docs.google.com/spreadsheets/d/[ID_ICI]/edit`

---

## Étape 3 — Twilio WhatsApp

1. Va sur [console.twilio.com](https://console.twilio.com)
2. Récupère :
   - Account SID : `ACxxxxxxxx`
   - Auth Token : dans le dashboard
3. Active **WhatsApp Business** (sandbox ou numéro dédié)
4. Note ton numéro WhatsApp Twilio : `whatsapp:+1415xxxxxxx`

---

## Étape 4 — N8N : Variables d'environnement

Dans N8N, va dans **Settings > Variables** et crée :

| Nom | Valeur |
|-----|--------|
| `GOOGLE_PLACES_API_KEY` | Ta clé Google Places |
| `GOOGLE_SHEET_ID` | L'ID de ton Google Sheets CRM |
| `TWILIO_WHATSAPP_NUMBER` | `whatsapp:+1415xxxxxxx` |

---

## Étape 5 — N8N : Credentials

### Google Sheets + Gmail (OAuth2)

1. Dans N8N, va dans **Credentials > Add Credential**
2. Choisis **Google OAuth2**
3. Nomme-la exactement : `Gmail - KEN Digital`
4. Suis l'authentification Google
5. Répète pour Google Sheets avec le même OAuth2

### Twilio

1. **Add Credential > Twilio**
2. Nomme-la : `Twilio - KEN Digital`
3. Remplis Account SID et Auth Token

---

## Étape 6 — Importer les workflows

1. Dans N8N, va dans **Workflows > Import**
2. Importe dans cet ordre :
   - `workflows/01-radar.json`
   - `workflows/02-tirs.json`
   - `workflows/03-reponses.json`
   - `workflows/04-relances.json`

---

## Étape 7 — Configurer le webhook Twilio (pour 03-reponses)

1. Dans N8N, ouvre le workflow **03 - RÉPONSES**
2. Clique sur le noeud **"Webhook WhatsApp (Twilio)"**
3. Copie l'URL du webhook (ex: `https://ton-n8n.com/webhook/whatsapp-inbound`)
4. Dans Twilio > Messaging > Settings > WhatsApp Sandbox Settings
5. Colle l'URL dans **"When a message comes in"** avec méthode POST

---

## Étape 8 — Activer les workflows

Active dans cet ordre :
1. **01-radar** (s'exécute à 8h, lun-ven)
2. **02-tirs** (s'exécute à 10h, lun-sam)
3. **03-reponses** (actif en permanence, écoute les webhooks)
4. **04-relances** (s'exécute à 14h, lun-sam)

---

## Calendrier d'exécution

```
08h00  →  RADAR scrape 21 villes (lun-ven)
10h00  →  TIRS envoie WA + Email aux NOUVEAU (lun-sam)
14h00  →  RELANCES vérifie J+2 et J+5 (lun-sam)
H24    →  RÉPONSES capture les entrantes (webhook)
```

---

## Surveillance

Surveille ces métriques dans Google Sheets :
- Nombre de NOUVEAU ajoutés / jour
- Taux de réponse : RÉPONDU / CONTACTÉ
- Taux d'intérêt : INTERET / RÉPONDU
- Taux de conversion : CLIENT / INTERET

**Objectif avant le 31 mai 2026 : 20 clients signés**
