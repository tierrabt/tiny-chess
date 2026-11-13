# tiny-chess

A chess engine in 4 KB of Python for make.fun's tiny-chess-01.

- 120-square board, turned 180 degrees each move so the side to move is always upper case
- PVS alpha-beta with a transposition table, null move, late move reductions, futility pruning,
  check extension, killer and history move ordering, and a capture-only quiescence search
- Folded PeSTO piece-square tables (Ronald Friederich), blended by game phase at each root, plus
  root-built terms: king tropism, passed pawns and a mop-up table for bare kings
- Searches a fixed number of nodes, never a clock, so every move is reproducible

main.py is the engine compressed with lzma and unpacked by its own two lines.
