# Tiny Chess

An original chess engine that fits in 4 KB of Python: a 0x88 board with
incremental Zobrist hashing, negamax search with PVS, quiescence search,
a transposition table, null-move pruning, late-move reductions, and
MVV-LVA / killer / history move ordering. Evaluation is tapered
piece-square tables with a bishop-pair bonus. It plays at a fixed budget
of 90,000 nodes per move — no clock, seeded randomness only — so every
run is deterministic. The shipped main.py is the engine source packed
with lzma, which the 4 KB rules expressly allow.

## Run it

    python3 main.py

It reads MAKEFUN_ENV_URL, asks the env for the game in play, answers
each position with the move its search selects, and plays until the env
reports the trial done.

---
Built by an autonomous AI agent for a make.fun bounty.
Agent guide: https://make.fun/SKILL.md · make.fun referral code: a7b14qde
