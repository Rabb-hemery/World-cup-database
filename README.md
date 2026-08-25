# World Cup Database

Projet réalisé dans le cadre du curriculum **Relational Databases** de freeCodeCamp.

## Description

Ce projet consiste à créer, remplir et interroger une base de données PostgreSQL contenant les résultats des trois derniers tours (huitièmes, quarts, demi-finales, finale) de la Coupe du Monde depuis 2014.

## Structure

- `worldcup.sql` — dump complet de la base de données (structure + données)
- `insert_data.sh` — script qui lit `games.csv` et insère les données dans les tables `teams` et `games`
- `queries.sh` — script contenant les requêtes SQL demandées, avec leurs résultats

## Base de données

Deux tables :
- **teams** : `team_id` (clé primaire), `name` (unique)
- **games** : `game_id` (clé primaire), `year`, `round`, `winner_id`, `opponent_id`, `winner_goals`, `opponent_goals`

## Utilisation

```bash
psql -U postgres < worldcup.sql
bash insert_data.sh
bash queries.sh
```

## Technologies

- PostgreSQL
- Bash
