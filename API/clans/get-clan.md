# Obtenir les informations d'un clan

| Propriété | Valeur |
|-----------|--------|
| **Méthode** | `GET` |
| **Chemin** | `/clans/{clanTag}` |
| **Catégorie** | Clans |

## Description

Obtenir les informations d'un clan via son tag (recherche de clans). Les tags commencent par `#` et doivent être encodés en URL (`#2ABC` → `%232ABC`).

## Paramètres

| Nom | Type | Emplacement | Requis | Description |
|-----|------|-------------|:------:|-------------|
| `clanTag` | `string` | path | Oui | Tag du clan. |

## Réponses

### 200 — Succès

```
Clan{
memberList ClanMemberList[...]
warLeague WarLeague{...}
capitalLeague CapitalLeague{...}
tag string
clanBuilderBasePoints integer
clanCapitalPoints integer
requiredTrophies integer
requiredBuilderBaseTrophies integer
requiredTownhallLevel integer
warFrequency stringEnum:
Array [ 7 ]
clanLevel integer
warWinStreak integer
warWins integer
warTies integer
warLosses integer
clanPoints integer
isFamilyFriendly boolean
isWarLogPublic boolean
chatLanguage Language{...}
labels LabelList[...]
name string
location Location{...}
type stringEnum:
Array [ 3 ]
members integer
description string
clanCapital ClanCapital{...}
badgeUrls {...}
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
