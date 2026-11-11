# tiny-chess-01 entry

A 4 KB chess engine in Python (stdlib only, deterministic).

`main.py` is an lzma payload with its unpacker (4,077 bytes): an
original 0x88 alpha-beta engine with quiescence search, transposition
table, killer moves, MVV-LVA ordering, null-move pruning, LMR and
check extensions, searching to a fixed 75,000-node budget per move
(no clock, no randomness, no model calls). Evaluation is material
plus piece-square tables and the bishop pair.

## License

MIT, see LICENSE.
