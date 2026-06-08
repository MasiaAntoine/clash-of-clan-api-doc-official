# Rechercher des clans

| Propriété | Valeur |
|-----------|--------|
| **Méthode** | `GET` |
| **Chemin** | `/clans` |
| **Catégorie** | Clans |

## Description

Rechercher des clans par nom et/ou filtrer selon divers critères. Au moins un critère est requis. Le nom doit comporter au moins 3 caractères. L'ordre des résultats n'est pas garanti.

## Paramètres

| Nom | Type | Emplacement | Requis | Description |
|-----|------|-------------|:------:|-------------|
| `name` | `string` | query | Non | Recherche par nom (min. 3 caractères), joker autorisé. |
| `warFrequency` | `string` | query | Non | Filtrer par fréquence de guerres |
| `locationId` | `integer` | query | Non | Filtrer par localisation (voir `GET /locations`). |
| `minMembers` | `integer` | query | Non | Nombre minimum de membres |
| `maxMembers` | `integer` | query | Non | Nombre maximum de membres |
| `minClanPoints` | `integer` | query | Non | Points de clan minimum. |
| `minClanLevel` | `integer` | query | Non | Niveau de clan minimum. |
| `limit` | `integer` | query | Non | Limite du nombre d'éléments retournés. |
| `after` | `string` | query | Non | Éléments après ce marqueur (dans `paging`, champ `after`). `after` et `before` sont mutuellement exclusifs. |
| `before` | `string` | query | Non | Éléments avant ce marqueur (dans `paging`, champ `before`). `after` et `before` sont mutuellement exclusifs. |
| `labelIds` | `string` | query | Non | IDs de labels séparés par des virgules. |

## Réponses

### 200 — Succès

```
ClanList[Clan{...}]
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
