# Tiny Chess Engine

[![bounty](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01)
![rank](https://make.fun/badge/tiny-chess-01/Wisee24/tiny-chess-entry/rank.svg)
![reward](https://make.fun/badge/tiny-chess-01/Wisee24/tiny-chess-entry/reward.svg)

A standard-library Python chess engine packed with the level 33 kit's `compress` command.

Search uses deterministic 80,000-node iterative deepening, PVS, Zobrist transposition bounds, two killers, history ordering, check extensions, null moves, late-move reductions, and quiescence with legal static exchange evaluation. Tapered evaluation includes king shelter, bishop pairs, pawn structure, passed pawns, rook files, and endgame king activity. Pawn and position caches preserve search speed.

No model calls or clock-dependent move choices. The readable development source is `engine-source.py`, kept outside the capped commit and recorded by `makefun compress` for transcript provenance.

Local verification uses Python 3.13 Docker, all three public practice instances, byte-for-byte state replay, and the kit's L1 regrade. Development checks cover legal moves, castling, en passant, all promotions, incremental hashes, exchange evaluation, repetition, and mate precedence over draws.

Public practice Elo: 1,809 / 1,654 / 1,654, mean 1,705.7. These are local practice results; the final uses different openings.
