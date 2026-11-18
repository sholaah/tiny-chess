# Tiny Chess — tiny-chess-01 entry

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/sholaah/tiny-chess/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/sholaah/tiny-chess/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

Entry for the [make.fun “Build the strongest chess engine in 4 KB of Python” bounty](https://make.fun/bounty/tiny-chess-01).

A complete chess engine in a single `main.py` of 3,945 bytes (limit 4,096), written in pure Python 3.13 standard library:

- 0x88-style 10x12 board, full legal move generation (castling, en passant, promotions), Zobrist hashing with incremental updates
- Negamax alpha-beta search with transposition table, principal variation search, late move reductions, null-move pruning, killer moves, and check extensions
- Quiescence search with check evasions so mate scores stay exact at the horizon
- Tapered evaluation with piece-square tables generated from compact formulas (no table data stored), bishop-pair and phase blending
- Fixed 60,000-node budget per move — the search never reads a clock

`main.py` is packed with the make.fun kit's own `compress` command from a readable source kept beside it in this folder.
