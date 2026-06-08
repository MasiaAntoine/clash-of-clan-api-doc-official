# Lister les ligues

| Propriété | Valeur |
|-----------|--------|
| **Méthode** | `GET` |
| **Chemin** | `/leagues` |
| **Catégorie** | Ligues |

## Description

Lister les ligues

## Paramètres

| Nom | Type | Emplacement | Requis | Description |
|-----|------|-------------|:------:|-------------|
| `limit` | `integer` | query | Non | Limite du nombre d'éléments retournés. |
| `after` | `string` | query | Non | Éléments après ce marqueur (dans `paging`, champ `after`). `after` et `before` sont mutuellement exclusifs. |
| `before` | `string` | query | Non | Éléments avant ce marqueur (dans `paging`, champ `before`). `after` et `before` sont mutuellement exclusifs. |

## Réponses

### 200 — Succès

```
LeagueList[League{...}]
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
