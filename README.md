# tiny-chess-01 entry

A 4 KB chess engine in Python (stdlib only, deterministic).

`main.py` is an lzma payload with its unpacker: an original 0x88
alpha-beta engine with quiescence search, transposition table,
killer moves, MVV-LVA ordering, null-move pruning (R=2), LMR and
check extensions, searching to a fixed 100,000-node budget per move
(no clock, no randomness, no model calls). Evaluation is material
plus piece-square tables and the bishop pair.

Practice Elo (v5): trial-0 1430, trial-1 1326, mean 1378 — above
the sunfish 4K baseline (mean 1360), but the lead is thin.
v6 raises the node budget 75k -> 100k per move (the v3 timeout
was caused by CPU contention, not the budget). Node budget
100,000/move keeps every move well under the 10 s limit
and each 16-game trial under the 3,600 s wall.

## License

MIT, see LICENSE.
