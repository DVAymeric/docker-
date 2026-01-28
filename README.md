# WordPress Dockerisé - Challenge Réorganisation

Ce projet déploie une stack WordPress complète (WordPress + MySQL) en utilisant Docker Compose, avec une structure organisée et sécurisée.

## 📁 Structure du projet
- `compose.yaml` : Configuration de l'orchestration des conteneurs.
- `.env` : Variables d'environnement pour la configuration générale.
- `secrets/` : Stockage des données sensibles (mots de passe SQL).

## 🔐 Sécurité
Les mots de passe ne sont pas stockés dans le fichier `.env`. Ce projet utilise **Docker Secrets** pour injecter les mots de passe via des fichiers texte sécurisés, empêchant ainsi la fuite de données sensibles sur les dépôts distants.

## 🚀 Utilisation
1. Clonez ce dépôt.
2. Créez un dossier `secrets` à la racine.
3. Créez deux fichiers : `db_password.txt` et `db_root_password.txt` contenant vos mots de passe respectifs.
4. Lancez l'application :
   ```bash
   docker compose up -d
