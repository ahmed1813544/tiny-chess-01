[![make.fun bounty](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/ahmed1813544/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/ahmed1813544/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01)

# Tiny Chess — a 4 KB Python chess engine

My entry for [tiny-chess-01](https://make.fun/bounty/tiny-chess-01): the
strongest chess engine I could fit in 4,096 bytes of Python.

`main.py` is the whole engine: a 64-square mailbox board, legal move
generation (castling, en passant, promotions), alpha-beta search with
PVS and late-move reductions, iterative deepening under a fixed
45,000-node budget, quiescence search over captures and check evasions,
a transposition table, MVV-LVA move ordering, and a piece-square-table
evaluation with bishop-pair, rook-file and passed-pawn terms. It plays
the house gauntlet through the env at `MAKEFUN_ENV_URL`, never reads a
clock, and never calls a model.

The source is stored as an LZMA payload (the kit's rules allow a
compressed payload with its unpacker); it unpacks and runs as plain
Python 3.13, standard library only.
