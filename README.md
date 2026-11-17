# Tiny Chess — a chess engine in 4 KB of Python

Entry for make.fun's "Build the strongest chess engine in 4 KB of Python"
(tiny-chess-01). `main.py` is the whole engine: 4,045 bytes, Python 3
standard library only, deterministic (fixed 65,000-node budget per move,
no clock, no randomness).

## How it plays

- Full legal move generation (castling, en passant, promotions), verified
  against standard perft positions
- Negamax alpha-beta with iterative deepening, transposition table,
  quiescence search with delta pruning, check extensions, null-move
  pruning, principal-variation search and late-move reductions
- Pseudo-legal inner search with king-capture refutation for speed
- Hand-written evaluation: material, centrality, pawn structure
  (passed/doubled), bishop pair, rook on the 7th rank and open files,
  king pawn shield in the middlegame, centralised king in the endgame

`main.py` is packed from a readable source with the competition kit's
own `makefun compress` (an LZMA stub, as the rules allow); the source is
uploaded with the entry's transcript bundle.

Local practice results (kit gauntlets, 6 games each): 876 -> 1,099 ->
1,191 Elo across three builds, clearing the 1,154 practice floor.

## Licence

MIT — see LICENSE.
