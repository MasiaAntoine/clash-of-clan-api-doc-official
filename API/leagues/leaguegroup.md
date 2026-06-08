# Obtenir un groupe de ligue classée

| Propriété | Valeur |
|-----------|--------|
| **Méthode** | `GET` |
| **Chemin** | `/leaguegroup/{leagueGroupTag}/{leagueSeasonId}` |
| **Catégorie** | Ligues |

## Description

Obtenir un groupe de ligue classée

## Paramètres

| Nom | Type | Emplacement | Requis | Description |
|-----|------|-------------|:------:|-------------|
| `leagueGroupTag` | `string` | path | Oui | Identifiant du groupe de ligue. |
| `leagueSeasonId` | `string` | path | Oui | Identifiant de la saison de ligue. |
| `playerTag` | `string` | query | Oui | Tag of the player |

## Réponses

### 200 — Succès

```
LeagueGroup{
members LeagueGroupMemberList[...]
attackLogs LeagueGroupBattleLogEntryList[...]
defenseLogs LeagueGroupBattleLogEntryList[...]
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
