# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/taigedi123/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/taigedi123/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in at most 4,096 bytes of Python (main.py is 4,080 bytes: an
LZMA-packed build of a readable source, packed with the kit's
`makefun compress`). Negamax search with alpha-beta and PVS, a
transposition table, quiescence over captures, promotions and check
evasions, null-move pruning, late-move reductions, a defended-capture
test in quiescence, and a tapered piece-square evaluation with passed
pawns and pawn-structure terms from bitboards. It searches to a fixed
node budget (60,000 nodes a move): no clock and no randomness anywhere
in move choice, so every trial replays byte for byte. It plays the
house gauntlet through the env at MAKEFUN_ENV_URL (POST /game, /move).

## Run it

```sh
MAKEFUN_ENV_URL=http://store:8080 python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=5xww654b&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
