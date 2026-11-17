# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/taigedi123/tiny-chess-01-silver-kestrel/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/taigedi123/tiny-chess-01-silver-kestrel/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in at most 4,096 bytes of Python (main.py is 4,015 bytes: an
LZMA-packed build of a readable source, packed with the kit's
`makefun compress`). Negamax search with alpha-beta and PVS, a
transposition table, quiescence over captures, promotions and check
evasions with static exchange evaluation, null-move pruning,
late-move reductions, check extensions, killer moves and in-search
repetition scoring, over a tapered piece-square evaluation (middlegame
and endgame tables for pawns, knights, bishops and the king). It
searches to a fixed node budget (60,000 nodes a move): no clock and no
randomness anywhere in move choice, so every trial replays byte for
byte. Local practice trials against the house gauntlet rate it around
Elo 1,400-1,550 (the house baseline is about 1,365). It plays through
the env at MAKEFUN_ENV_URL (POST /game, /move).

## Run it

```sh
MAKEFUN_ENV_URL=http://store:8080 python3 main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=5xww654b&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
