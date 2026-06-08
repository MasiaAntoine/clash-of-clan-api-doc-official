# Introduction et authentification

## Démarrage rapide

1. Créez un compte sur le [portail développeur](https://developer.clashofclans.com).
2. Générez un jeton API (**Mon compte**).
3. Ajoutez-le à chaque requête :

```http
GET /v1/players/%232ABC HTTP/1.1
Host: api.clashofclans.com
Authorization: Bearer VOTRE_JETON
Accept: application/json
```

## Encodage des tags

| En jeu | En URL |
|--------|--------|
| `#2ABC` | `%232ABC` |
| `#9G9QGJ2C` | `%239G9QGJ2C` |

## Limites et erreurs

- **429** : trop de requêtes pour votre jeton.
- **403** : jeton invalide ou accès refusé à la ressource.
- Réponses au format `application/json`.

## Pagination

```json
{
  "items": [],
  "paging": {
    "after": "marqueur_apres",
    "before": "marqueur_avant"
  }
}
```

[← Retour à l'index](../README.md)
