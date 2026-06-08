# Récupérer la guerre de clan actuelle

| Propriété | Valeur |
|-----------|--------|
| **Méthode** | `GET` |
| **Chemin** | `/clans/{clanTag}/currentwar` |
| **Catégorie** | Clans |

## Description

Récupérer la guerre de clan actuelle

## Paramètres

| Nom | Type | Emplacement | Requis | Description |
|-----|------|-------------|:------:|-------------|
| `clanTag` | `string` | path | Oui | Tag du clan. |

## Réponses

### 200 — Succès

```
ClanWar{
clan WarClan{...}
teamSize integer
attacksPerMember integer
battleModifier stringEnum:
Array [ 2 ]
opponent WarClan{...}
startTime string
state stringEnum:
Array [ 10 ]
endTime string
preparationStartTime string
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
