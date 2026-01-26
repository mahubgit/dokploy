# Déploiement Clawdbot via Dokploy

## 1️⃣ Prérequis

- Serveur Dokploy fonctionnel
- Docker & Docker Compose installés
- Accès à Ollama externe : http://localhost:11434

---

## 2️⃣ Déploiement

1. Pousse ce repo dans ton dépôt Git (Dokploy compatible)
2. Dans l'interface Dokploy :
   - Crée une **application Docker Compose**
   - Sélectionne ce repo
   - Déploie

Dokploy créera automatiquement les volumes Docker persistants :
- `clawdbot-config`
- `clawdbot-workspace`

---

## 3️⃣ Onboarding Clawdbot

1. Ouvre un terminal sur le service `clawdbot-cli` depuis Dokploy
2. Lance la commande :

```bash
docker compose run --rm clawdbot-cli onboard

