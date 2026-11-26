# SNOWFALL 11.7 — maquette Mini App

## Contenu
- `index.html` : interface mobile autonome (HTML/CSS/JS).
- `Dockerfile` : hébergement statique via Nginx.
- `docker-compose.yml` : lancement local ou sur VPS.

## Aperçu
Ouvrir `index.html` dans un navigateur. Sur iPhone, le plus simple est de déployer le dossier sur un hébergement HTTPS puis d'ouvrir l'adresse dans Telegram.

## Docker
```bash
docker compose up -d --build
```
Puis ouvrir `http://localhost:8080`.

## Connexion Telegram
Pour devenir une vraie Telegram Mini App, il faut :
1. Créer le bot avec @BotFather et définir le domaine HTTPS avec `/setdomain`.
2. Héberger cette page en HTTPS.
3. Ajouter le bouton Web App au bot via un backend Telegram (token conservé uniquement côté serveur).
4. Ajouter une base de données et une authentification administrateur avant de stocker des commandes.

Ne placez jamais le token du bot dans `index.html`, dans le navigateur ou dans un dépôt public. La maquette ne réalise aucun paiement et les fiches/prix sont fictifs. Vérifiez la conformité réglementaire avant toute utilisation commerciale.
