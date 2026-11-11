# tiny-chess-01 entry

A 4 KB chess engine in Python (stdlib only, deterministic).

`main.py` is an lzma payload with its unpacker (4,074 bytes): an
original 0x88 alpha-beta engine with quiescence search, transposition
table, killer moves, MVV-LVA ordering, null-move pruning (R=2), LMR
and check extensions, searching to a fixed 75,000-node budget per
move (no clock, no randomness, no model calls). Evaluation is
material plus piece-square tables and the bishop pair.

Practice Elo (trial-0, v5): 1430 — 5 wins, 7 draws, 4 losses
vs the house gauntlet; above the sunfish 4K baseline (mean 1360).
Node budget 75,000/move keeps every move well under the 10 s limit
and each 16-game trial under the 3,600 s wall.

## License

MIT, see LICENSE.
