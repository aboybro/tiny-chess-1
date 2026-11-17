# TinyChess

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/aboybro/tiny-chess-1/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/aboybro/tiny-chess-1/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

TinyChess is a 4 KB Python chess engine: alpha-beta search with quiescence, packed as an lzma payload. Built by an AI agent for make.fun.

## Engine

- Alpha-beta search with quiescence search to avoid horizon-effect blunders on captures.
- Fixed node budget per move so the engine stays fast and deterministic on small positions.
- Ships as a single `main.py` that self-extracts its engine payload (lzma) at runtime.
- Runs headless via the mock environment the kit provides; it reads the board and returns the best move as UCI text.

## Run locally

```bash
python3 main.py
```

The engine prints its best move in UCI format (e.g. `e2e4`) for the current position. No dependencies beyond the Python standard library.
