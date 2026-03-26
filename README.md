# TP 13 : Intégration OAuth2 (Google / Keycloak)
---
## Objectif

---
Déléguer l'authentification d'une application Spring Boot à un fournisseur externe (Google ou Keycloak) en utilisant OAuth2 et OpenID Connect (OIDC). L'utilisateur s'authentifie auprès d'un service d'identité tiers au lieu de l'application elle-même.

---


## Architecture du TP
---
<img width="556" height="536" alt="image" src="https://github.com/user-attachments/assets/7e06e696-91a1-441b-bef6-41cfca4d707a" />

---
## Configuration avec Google
---
Prérequis dans la console Google Cloud :

Créer un projet

Activer l'API "Google Identity"

Créer des identifiants OAuth 2.0

Configurer l'URL de redirection : http://localhost:8082/login/oauth2/code/google

Éléments à configurer dans l'application :

Client ID et Client Secret fournis par Google

Scopes requis : openid, profile, email

Issuer URI : https://accounts.google.com

---
## Sécurité et bonnes pratiques
---
Utiliser HTTPS en production pour sécuriser les échanges

---
## Video demo
---
https://github.com/user-attachments/assets/975d6042-c3c3-4500-9184-bc0bd6e542d5

## Résumé
---
Ce TP met en œuvre une authentification déléguée conforme aux standards modernes. L'application ne gère plus localement les identifiants mais s'appuie sur un tiers de confiance. Cette approche est essentielle pour :

Le Single Sign-On (SSO) entre plusieurs applications

La sécurisation des APIs dans les architectures distribuées

---
## Auteur
---AIT LECHGUEUR BASMA

La réduction de la surface d'attaque (pas de stockage de mots de passe)

