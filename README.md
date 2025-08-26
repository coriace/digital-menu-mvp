
# Menu Digital – MVP (React + Node)

Un prototype minimal pour créer et afficher des menus digitaux avec QR code.

## Lancer en local

### 1) Backend
```bash
cd backend
npm install
npm run start
```
L'API tourne sur **http://localhost:3000**.

### 2) Frontend
Dans un autre terminal :
```bash
cd frontend
npm install
npm run dev
```
L’interface tourne sur **http://localhost:5173**.

> Astuce : Vous pouvez changer la destination du QR en définissant `FRONTEND_BASE` côté backend.

## Démo express
1. Ouvre http://localhost:5173 puis va sur **/admin**
2. Renseigne `Nom` et `Slug` (ex: `luigi-darbouazza`) et clique **Enregistrer**.
3. Ajoute quelques plats (nom, prix, catégorie…).
4. Clique "Voir le menu public" → ton menu est disponible sur `/menu/{slug}`.
5. Le bouton "Télécharger le QR" génère un QR pointant vers cette URL.

## Limites connues (MVP)
- Pas d’authentification (utilise un slug que toi seul connais pour tester).
- Persistance JSON (LowDB). Pour la prod, passer à PostgreSQL.
- Pas d’upload d’images (uniquement URL).
- Pas (encore) de commandes ni de paiements.

## Prochaines étapes possibles
- Authentification restaurateur (email/mot de passe + rôles).
- Multi-établissements, horaires, options de plat (tailles, suppléments), allergènes.
- Widgets d’embed, mode hors-ligne (PWA), analytics.
- Impression QR (PDF) et thèmes visuels (clair/sombre, branding).
