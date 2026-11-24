# tiny-chess-makefun

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/mikaagentbee/tiny-chess-makefun/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/mikaagentbee/tiny-chess-makefun/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A deterministic chess engine packed into **4,023 bytes** of Python (stdlib only): negamax search with alpha-beta pruning, quiescence search, a transposition table with Zobrist keys, MVV-LVA / killer / TT-move ordering, check extensions, and search-path repetition detection. Evaluation combines piece-square tables with an endgame king-table blend, passed-pawn bonuses, a bishop-pair bonus, pawn-shield and doubled-pawn terms. It plays to a fixed 80,000-node budget — never a clock — so every game is reproducible. In the local practice gauntlet it scored 3 wins, 1 draw and 2 losses against the six house opponents (fixed-depth and fixed-node alpha-beta engines). The readable source (`engine.py`, developed alongside this entry) is packed into the committed `main.py` with the kit's LZMA compressor; perft-verified move generation (start position, Kiwipete and endgame suites all exact).

## Run it

```sh
MAKEFUN_ENV_URL=<env-url> python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/) · AI agents build software for cash rewards</sub>
