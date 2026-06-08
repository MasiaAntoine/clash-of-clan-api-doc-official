# Documentation API Clash of Clans

Documentation officielle de l'API Clash of Clans, traduite et structurée en français.

## Présentation

L'API Clash of Clans expose les données du jeu au format **JSON** : clans, joueurs,
ligues, localisations, classements, passe d'or et labels.

- [Introduction et authentification](API/introduction.md)
- [Modèles de données](MODELES/README.md)

## Authentification

Chaque requête nécessite un jeton JWT dans l'en-tête HTTP :

```http
Authorization: Bearer VOTRE_JETON_API
```

Créez votre jeton sur la page **Mon compte** du [portail développeur Supercell](https://developer.clashofclans.com).

## URL de base

```
https://api.clashofclans.com/v1
```

> Les tags (`#2ABC`) doivent être encodés en URL (`%232ABC`).

## Routes

### Clans

Accéder aux informations spécifiques aux clans.

- [GET `/clans/{clanTag}/currentwar/leaguegroup`](API/clans/currentwar-leaguegroup.md) — Récupérer le groupe de guerre de ligue actuel du clan
- [GET `/clans/{clanTag}/warlog`](API/clans/warlog.md) — Récupérer le journal de guerre de clan
- [GET `/clans`](API/clans/search.md) — Rechercher des clans
- [GET `/clans/{clanTag}/currentwar`](API/clans/currentwar.md) — Récupérer la guerre de clan actuelle
- [GET `/clans/{clanTag}`](API/clans/get-clan.md) — Obtenir les informations d'un clan
- [GET `/clans/{clanTag}/members`](API/clans/members.md) — Lister les membres du clan
- [GET `/clans/{clanTag}/capitalraidseasons`](API/clans/capitalraidseasons.md) — Récupérer les saisons de raid de capitale

### Guerres de ligue

Routes liées aux guerres de ligue de clan.

- [GET `/clanwarleagues/wars/{warTag}`](API/clanwarleagues/wars.md) — Récupérer une guerre de ligue de clan

### Joueurs

Accéder aux informations spécifiques aux joueurs.

- [GET `/players/{playerTag}`](API/players/get-player.md) — Obtenir les informations d'un joueur
- [GET `/players/{playerTag}/battlelog`](API/players/battlelog.md) — Obtenir le journal de bataille
- [POST `/players/{playerTag}/verifytoken`](API/players/verifytoken.md) — Vérifier le jeton API joueur
- [GET `/players/{playerTag}/leaguehistory`](API/players/leaguehistory.md) — Obtenir l'historique de ligue

### Ligues

Accéder aux informations sur les ligues.

- [GET `/leaguetiers/{leagueTierId}`](API/leagues/leaguetier.md) — Obtenir un palier de ligue
- [GET `/capitalleagues`](API/leagues/capitalleagues.md) — Lister les ligues de capitale
- [GET `/leaguetiers`](API/leagues/leaguetiers.md) — Lister les paliers de ligue
- [GET `/leagues`](API/leagues/list.md) — Lister les ligues
- [GET `/leagues/{leagueId}/seasons/{seasonId}`](API/leagues/season.md) — Obtenir le classement d'une saison de ligue
- [GET `/capitalleagues/{leagueId}`](API/leagues/capitalleague.md) — Obtenir une ligue de capitale
- [GET `/builderbaseleagues/{leagueId}`](API/leagues/builderbaseleague.md) — Obtenir une ligue de base du bâtisseur
- [GET `/builderbaseleagues`](API/leagues/builderbaseleagues.md) — Lister les ligues de base du bâtisseur
- [GET `/leagues/{leagueId}`](API/leagues/league.md) — Obtenir une ligue
- [GET `/leaguegroup/{leagueGroupTag}/{leagueSeasonId}`](API/leagues/leaguegroup.md) — Obtenir un groupe de ligue classée
- [GET `/leagues/{leagueId}/seasons`](API/leagues/seasons.md) — Lister les saisons d'une ligue
- [GET `/warleagues/{leagueId}`](API/leagues/warleague.md) — Obtenir une ligue de guerre
- [GET `/warleagues`](API/leagues/warleagues.md) — Lister les ligues de guerre

### Localisations

Accéder aux classements globaux et locaux.

- [GET `/locations/{locationId}/rankings/clans`](API/locations/rankings-clans.md) — Classement des clans par localisation
- [GET `/locations/{locationId}/rankings/players`](API/locations/rankings-players.md) — Classement des joueurs par localisation
- [GET `/locations/{locationId}/rankings/players-builder-base`](API/locations/rankings-players-builder-base.md) — Classement joueurs (base du bâtisseur)
- [GET `/locations/{locationId}/rankings/clans-builder-base`](API/locations/rankings-clans-builder-base.md) — Classement clans (base du bâtisseur)
- [GET `/locations`](API/locations/list.md) — Lister les localisations
- [GET `/locations/{locationId}/rankings/capitals`](API/locations/rankings-capitals.md) — Classement des capitales par localisation
- [GET `/locations/{locationId}`](API/locations/get-location.md) — Obtenir une localisation

### Passe d'or

Informations sur le passe d'or.

- [GET `/goldpass/seasons/current`](API/goldpass/seasons-current.md) — Obtenir la saison actuelle du passe d'or

### Labels

Lister les labels de clans et de joueurs.

- [GET `/labels/players`](API/labels/players.md) — Lister les labels de joueurs
- [GET `/labels/clans`](API/labels/clans.md) — Lister les labels de clans

## Pagination

Les listes acceptent `limit`, `after` et `before`. Les marqueurs de pagination se trouvent dans `paging`.
Utilisez `after` **ou** `before`, jamais les deux.

## Conditions d'utilisation

Soumis aux [conditions Supercell](https://developer.clashofclans.com).

---

## Soutenir le projet

Si cette documentation vous est utile, offrez-moi un café — ça aide à maintenir le dépôt à jour.

[![Buy me a coffee](https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExYnJrd2ExdWRqN2UyZXJtdHhnamRkNG8xcWVmd3J6dGR3cTJzNG8ybSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/GNBCVMv6XobnMUMYJG/giphy.gif)](https://buymeacoffee.com/thorkild)
