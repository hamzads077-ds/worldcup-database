# ⚽ World Cup Database 

![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
![Bash Script](https://img.shields.io/badge/Bash_Script-121011?style=for-the-badge&logo=gnu-bash&logoColor=white)
![freeCodeCamp](https://img.shields.io/badge/freeCodeCamp-0A0A23?style=for-the-badge&logo=freecodecamp&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

---


A relational database and Bash scripting project built for the **freeCodeCamp Relational Database Certification**. It parses FIFA World Cup match records from `games.csv`, loads them into a normalized **PostgreSQL** database, and runs analytical SQL queries.

## ⚙️ How It Was Built

1. **Database (`worldcup.sql`):** Created a `worldcup` database in PostgreSQL with two normalized tables: `teams` (24 unique teams) and `games` (32 matches) linked via `winner_id` and `opponent_id` foreign keys.
2. **Data Insertion (`insert_data.sh`):** Built a Bash script that reads `games.csv` using `IFS=","`, dynamically inserts unique teams into `teams`, fetches their `team_id`, and populates all match rows into `games`.
3. **Data Analysis (`queries.sh`):** Wrote 12 SQL queries using `SUM`, `AVG`, `ROUND`, `MAX`, `COUNT`, and `INNER JOIN` to generate tournament statistics matching `expected_output.txt`.

## 🚀 Quick Run

```bash
psql -U postgres < worldcup.sql
chmod +x insert_data.sh queries.sh
./insert_data.sh
./queries.sh
```

---

## 📊 Repository Stats

[![Stars](https://img.shields.io/github/stars/hamzads077-ds/worldcup-database?style=for-the-badge&logo=github&color=yellow)](https://github.com/hamzads077-ds/worldcup-database/stargazers)
[![Forks](https://img.shields.io/github/forks/hamzads077-ds/worldcup-database?style=for-the-badge&logo=github&color=blue)](https://github.com/hamzads077-ds/worldcup-database/network/members)
[![Views](https://komarev.com/ghpvc/?username=hamzads077-ds-worldcup-database&style=for-the-badge&color=brightgreen&label=VIEWS)](https://github.com/hamzads077-ds/worldcup-database)
