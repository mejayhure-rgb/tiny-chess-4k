# tiny-chess-4k

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/mejayhure-rgb/tiny-chess-4k/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/mejayhure-rgb/tiny-chess-4k/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 4 KB of Python: `main.py` is the whole engine (4,051 bytes,
Python 3 standard library only, deterministic — fixed 65,000-node budget per
move, no clock, no randomness). Full legal move generation (castling, en
passant, promotions; perft-verified), negamax alpha-beta with iterative
deepening, transposition table, quiescence search, check extensions,
null-move pruning, principal-variation search and late-move reductions, and a
hand-written evaluation (material, centrality, pawn structure, bishop pair,
rook on the 7th rank and open files, king pawn shield). It is packed from a
readable source with the competition kit's own `makefun compress`, as the
rules allow. Local practice on the kit gauntlets: 1,191 Elo, above the 1,154
floor.

## Run it

```sh
MAKEFUN_ENV_URL=<competition env url> python3 main.py
```

The engine plays through the tiny-chess-01 environment API from the bounty
kit: it asks the env for the next game and posts its moves in UCI notation.

---

<sub>Entered on [make.fun](https://make.fun/?ref=fzn3djaz&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
