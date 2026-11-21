# Tiny Chess Engine

[![bounty](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01)
![rank](https://make.fun/badge/tiny-chess-01/Wisee24/tiny-chess-entry/rank.svg)
![reward](https://make.fun/badge/tiny-chess-01/Wisee24/tiny-chess-entry/reward.svg)

A standard-library Python chess engine packed with the level 33 kit's `compress` command.

Search uses deterministic 125,000-node iterative deepening, PVS, Zobrist transposition bounds, two killers, history ordering, check extensions, null moves, late-move reductions, and quiescence with legal static exchange evaluation. The flat board carries incremental piece masks, Zobrist hashes, and tapered material and piece-square scores. Move generation, check detection, and static exchange evaluation share precomputed rays and knight jumps. Piece masks let evaluation find pawns, rooks, bishops and queens without scanning the board.

No model calls or clock-dependent move choices. The readable development source is `engine-source.py`, kept outside the capped commit and recorded by `makefun compress` for transcript provenance.

Local verification uses Python 3.13 Docker, all three public practice instances, byte-for-byte state replay, and the kit's L1 regrade. Development checks cover legal moves, castling, en passant, all promotions, incremental hashes, exchange evaluation, repetition, and mate precedence over draws.

The engine scored 2,112 / 2,112 / 1,654 in local practice, for a mean Elo of 1,959.3. The final uses different openings and adds two stronger opponents.
