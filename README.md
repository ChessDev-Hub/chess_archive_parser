# Chess Archive Parser

A Linux-based Python tool to download Chess.com monthly PGN archives for a given user, extract opponent usernames, and analyze public account data. Designed to detect and categorize closed accounts (including fair play violations and abuse reports).

---

## ✅ Features

- Downloads PGN archives via the Chess.com public API
- Extracts all unique opponent usernames
- Fetches public account info from Chess.com
- Classifies accounts by status: `closed`, `closed:fair_play_violations`, `closed:abuse`
- Exports:
  - CSV file with all opponent data
  - TXT files with usernames grouped by account status
- Timestamped output files for easy tracking
- Skips PGNs already downloaded

---

## ⚙️ Requirements

- Python 3.7 or higher
- Stockfish installed at `/usr/bin/stockfish` (adjust path if needed)

### Python Modules

Install required modules:

```bash
pip install requests python-chess

