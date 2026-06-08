# Obtenir une localisation

| Propriété | Valeur |
|-----------|--------|
| **Méthode** | `GET` |
| **Chemin** | `/locations/{locationId}` |
| **Catégorie** | Localisations |

## Description

Obtenir les informations d'une localisation spécifique.

## Paramètres

| Nom | Type | Emplacement | Requis | Description |
|-----|------|-------------|:------:|-------------|
| `locationId` | `string` | path | Oui | Identifiant de la localisation. |

## Réponses

### 200 — Succès

```
Location{
localizedName string
id integer
name string
isCountry boolean
countryCode string
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
