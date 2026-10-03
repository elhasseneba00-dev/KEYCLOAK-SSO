# SSO Keycloak

Service d'authentification centralisé (Keycloak 26.7.5 + PostgreSQL + Caddy).

## Démarrage rapide (poste local)

    docker compose -f docker-compose.dev.yml up
    # Console : http://localhost:8080/admin  (admin / admin)
    # Realm d'exemple "sista" : mohmed / mohamed (admin), alassane / alassane

    

## Déploiement (VPS test puis prod)

    cp .env.example .env && nano .env && chmod 600 .env
    docker compose up -d

## Contenu

| Chemin | Rôle |
|---|---|
| docker-compose.yml, .env.example, Caddyfile | Production : Keycloak + PostgreSQL + HTTPS automatique |
| docker-compose.dev.yml, realm/entreprise-realm.json | Local : realm d'exemple importé au démarrage |

## État des tests

- Realm importé et login PKCE (web + mobile) vérifiés sur Keycloak 26.7.5
