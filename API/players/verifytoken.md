# Vérifier le jeton API joueur

| Propriété | Valeur |
|-----------|--------|
| **Méthode** | `POST` |
| **Chemin** | `/players/{playerTag}/verifytoken` |
| **Catégorie** | Joueurs |

## Description

Vérifier le jeton API à usage unique présent dans les paramètres du jeu pour confirmer la propriété du compte.

## Paramètres

| Nom | Type | Emplacement | Requis | Description |
|-----|------|-------------|:------:|-------------|
| `playerTag` | `string` | path | Oui | Tag du joueur. |
| `body` | `object` | body | Oui | Corps de la requête JSON. |

## Corps de la requête

```json
{
"token": "string"
}
```

## Réponses

### 200 — Succès

```
VerifyTokenResponse{
tag string
token string
status string
}
```

### Erreurs standard

| Code | Description |
|------|-------------|
| `400` | Le client a fourni des paramètres incorrects pour la requête. |
| `403` | Accès refusé : identifiants manquants/incorrects ou jeton API sans droits sur la ressource. |
| `404` | Ressource introuvable. |
| `429` | Requête limitée (throttling) : trop de requêtes pour le jeton API utilisé. |
| `500` | Erreur inconnue lors du traitement de la requête. |
| `503` | Service temporairement indisponible (maintenance). |

Format d'erreur :

```json
{
  "reason": "string",
  "message": "string",
  "type": "string",
  "detail": {}
}
```

[← Retour à l'index](../../README.md)
