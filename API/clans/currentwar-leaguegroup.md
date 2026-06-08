# Récupérer le groupe de guerre de ligue actuel du clan

| Propriété | Valeur |
|-----------|--------|
| **Méthode** | `GET` |
| **Chemin** | `/clans/{clanTag}/currentwar/leaguegroup` |
| **Catégorie** | Clans |

## Description

Récupérer le groupe de guerre de ligue actuel du clan

## Paramètres

| Nom | Type | Emplacement | Requis | Description |
|-----|------|-------------|:------:|-------------|
| `clanTag` | `string` | path | Oui | Tag du clan. |

## Réponses

### 200 — Succès

```
ClanWarLeagueGroup{
tag string
state stringEnum:
Array [ 5 ]
season string
clans ClanWarLeagueClanList[...]
rounds ClanWarLeagueRoundList[...]
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
