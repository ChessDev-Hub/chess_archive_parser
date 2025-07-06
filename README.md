# Chess Archive Parser

A terminal based Python tool to download Chess.com monthly PGN archives for a prompted username. Extracts their opponent usernames, and analyzes public account data of all unique opponents of that player. Designed to detect and categorize closed accounts (including self-closed, fair play violations closures and abuse closures). Output CSV files can be used to create spreadsheets or SQL database tables.

---

## ✅ Features

- Prompts for chess.com username when program starts
- Downloads PGN archives via the Chess.com public API to a subdirectory named archives off the current working directory
- Extracts all unique opponent usernames
- Fetches public account info about those oponents from Chess.com
- Classifies accounts by status: `closed`, `closed:fair_play_violations`, `closed:abuse`
- Data fields created in CSV:
  - Player_id (as assigned by chess.com -- useful for tracking when a username is changed in the future)
  - API_URL (the public API URL from which the opponent data is extracted)
  - User_URL (opponent's profile URL)
  - Username of the opponent
  - Title of the opponent (if it exists/placeholder if not)
  - Followers (number of followers the opponent has)
  - Country (two letter country code for the flag the opponent has chosen)
  - Last_online (Unix epoch timestamp of the last time the opponent logged in)
  - Joined (Unix epoch timestamp of when the opponent joined chess.com)
  - Status (account status of the opponent -- examples are basic, premium, staff, closed, closed:abuse, closed:fair_play_violations)
  - League (which player league the opponent has achieved)
- Exports:
  - CSV files with opponent data
  - TXT files with usernames grouped by account status
- Timestamped output files for easy tracking
- Skips monthly archive PGNs already downloaded in the archive subdirectory

---

## ⚙️ Requirements

- Python 3.7 or higher
- Stockfish installed at `/usr/bin/stockfish` (adjust path if needed)

### Python Modules

Install required modules:

```bash
pip install requests python-chess

