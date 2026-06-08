# Obtenir l'historique de ligue

| Propriété | Valeur |
|-----------|--------|
| **Méthode** | `GET` |
| **Chemin** | `/players/{playerTag}/leaguehistory` |
| **Catégorie** | Joueurs |

## Description

Historique de ligue du joueur pour les batailles classées.

## Paramètres

| Nom | Type | Emplacement | Requis | Description |
|-----|------|-------------|:------:|-------------|
| `playerTag` | `string` | path | Oui | Tag du joueur. |

## Réponses

### 200 — Succès

```
LeagueSeasonResultList[LeagueSeasonResult{...}]
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
