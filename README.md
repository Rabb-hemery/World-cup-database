# World Cup Database

Project completed as part of the freeCodeCamp **Relational Databases** curriculum.

## Description

This project consists of creating, populating, and querying a PostgreSQL database containing the results of the last three rounds (round of 16, quarterfinals, semifinals, finals) of the World Cup since 2014.

## Structure

- `worldcup.sql` — full database dump (structure + data)
- `insert_data.sh` — script that reads `games.csv` and inserts the data into the `teams` and `games` tables
- `queries.sh` — script containing the requested SQL queries along with their outputs

## Database

Two tables:
- **teams**: `team_id` (primary key), `name` (unique)
- **games**: `game_id` (primary key), `year`, `round`, `winner_id`, `opponent_id`, `winner_goals`, `opponent_goals`

## Usage

```bash
psql -U postgres < worldcup.sql
bash insert_data.sh
bash queries.sh
```

## Technologies

- PostgreSQL
- Bash
