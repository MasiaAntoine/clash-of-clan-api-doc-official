# Obtenir les informations d'un joueur

| Propriété | Valeur |
|-----------|--------|
| **Méthode** | `GET` |
| **Chemin** | `/players/{playerTag}` |
| **Catégorie** | Joueurs |

## Description

Obtenir les informations d'un joueur via son tag. Les tags se trouvent en jeu ou dans les listes de membres. Encodez `#` en `%23` dans l'URL.

## Paramètres

| Nom | Type | Emplacement | Requis | Description |
|-----|------|-------------|:------:|-------------|
| `playerTag` | `string` | path | Oui | Tag du joueur. |

## Réponses

### 200 — Succès

```
Player{
clan PlayerClan{...}
league League{...}
leagueTier LeagueTier{...}
builderBaseLeague BuilderBaseLeague{...}
role stringEnum:
Array [ 5 ]
warPreference stringEnum:
Array [ 2 ]
attackWins integer
defenseWins integer
townHallLevel integer
townHallWeaponLevel integer
legendStatistics PlayerLegendStatistics{...}
troops PlayerItemLevelList[...]
heroes PlayerItemLevelList[...]
heroEquipment PlayerItemLevelList[...]
spells PlayerItemLevelList[...]
labels LabelList[...]
tag string
name string
expLevel integer
trophies integer
bestTrophies integer
donations integer
donationsReceived integer
builderHallLevel integer
builderBaseTrophies integer
bestBuilderBaseTrophies integer
warStars integer
achievements PlayerAchievementProgressList[...]
clanCapitalContributions integer
playerHouse PlayerHouse{...}
currentLeagueGroupTag string
currentLeagueSeasonId Long{...}
previousLeagueGroupTag string
previousLeagueSeasonId Long{...}
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
