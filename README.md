# Chess Archive Parser

A Linux-based Python tool to download Chess.com monthly PGN archives for a given user, extract opponent usernames, and analyze public account data. Designed to detect and categorize closed accounts (including self-closed, fair play violations closures and abuse closures). Output CSV files can be used to create spreadsheets or SQL database tables.

---

## ✅ Features

- Downloads PGN archives via the Chess.com public API
- Extracts all unique opponent usernames
- Fetches public account info from Chess.com
- Classifies accounts by status: `closed`, `closed:fair_play_violations`, `closed:abuse`
- Exports:
  - CSV file with opponent data
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

