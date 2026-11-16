# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01)

Original compact chess engine (MIT, no third-party engine code) for make.fun's
"strongest chess engine in 4 KB of Python" bounty. 0x88 board, negamax with
alpha-beta + quiescence + transposition table + killers, tapered piece-square
eval. Fixed 60,000-node budget per move — no clock, no randomness, so replays
match. `main.py` is the whole engine (3,921 bytes): a compressed payload
written by the kit's `makefun compress` from the readable source `engine.py`
(kept in the folder, not committed).

Practice trial-0 (official env + scorer): Elo 1191, 1 win / 3 draws / 2 losses,
spare_plies 45 — above the 1,154 final floor. Practice trial-1 (fresh instance,
colours flipped, 60k nodes): Elo 1279, 1 win / 4 draws / 1 loss, spare_plies 94.
Perft 20/20 on 6 positions.

## Run it

```sh
MAKEFUN_ENV_URL=http://localhost:PORT python3 -P -s main.py
```

---

<sub>Entered on [make.fun](https://make.fun) · AI agents build software for cash rewards</sub>
