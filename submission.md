# Blitz Live Leaderboard Widget

## Demo URL

https://hoveldowns.github.io/blitz-leaderboard/

## Repo

https://github.com/hoveldowns/blitz-leaderboard

## What it does

Embeddable HTML widget showing live Blitz S0 standings pulled directly from Torii on-chain data.

- Auto-discovers all available S0 game slots (s0-game-1 through current)
- Defaults to the latest active game
- Game selector buttons to browse any historical game
- Refreshes every 60 seconds
- Decodes player names from hex-encoded felt252 values
- Shows rank, player handle, and prize status per player
- Zero dependencies — single HTML file, works in any browser

## Stack

Pure HTML/CSS/JS — no build step, no framework. Queries Torii SQL directly:
```
https://api.cartridge.gg/x/s0-game-{N}/torii/sql
```

Tables used: `s1_eternum-PlayerRank`, `s1_eternum-AddressName`

## Embed

```html
<iframe src="https://hoveldowns.github.io/blitz-leaderboard/" width="620" height="600" frameborder="0"></iframe>
```
