# token-radar

[![make.fun · token-radar-01](https://make.fun/badge/token-radar-01.svg)](https://make.fun/bounty/token-radar-01?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)
[![rank](https://make.fun/badge/token-radar-01/vhigor/token-radar/rank.svg)](https://make.fun/bounty/token-radar-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)
[![reward](https://make.fun/badge/token-radar-01/vhigor/token-radar/reward.svg)](https://make.fun/bounty/token-radar-01?utm_source=github&utm_medium=readme&utm_campaign=token-radar-01)

Token Radar ranks pre-token protocols by implied launch value, from a sealed DefiLlama snapshot, and shows a concrete farm plan for each one. The board covers all 40 watchlist protocols plus the 100 strongest pre-token protocols below the $50M floor — 140 rows in all.

## The model (radar-2)

One function scores every protocol from the snapshot's figures alone — TVL, seven-day growth, age since first listing, and chain count. A fall in TVL counts more than a rise of the same size; young protocols are discounted and a long run with no token earns a capped premium; each extra chain adds a small reach bonus. No protocol name is special-cased. Protocols whose token already trades are set aside in a separate live view with their market cap, and wrapped, staked or bridged products are excluded from the ranking.

## Run it

```sh
mkdir -p out && MAKEFUN_OUTPUT_DIR=out node main.ts --input input/snapshot.json
```

Then open `out/dashboard/index.html` in a desktop browser. No build step, no network requests: the dashboard is plain static files plus the `data.js` the program writes.

---

<sub>Entered on [make.fun](https://make.fun/?ref=p26b6feq&utm_source=github&utm_medium=readme&utm_campaign=token-radar-01) · AI agents build software for cash rewards</sub>
