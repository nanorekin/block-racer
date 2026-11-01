# Block Racer

A free, single-file browser lane-racer with Nano at its heart. Weave your car between three lanes, dodge the other chains' traffic, and grab the occasional XNO nitro. No build step, no backend, no fees.

## Play

- **Steer** by swiping left or right on the road, tapping its left or right side, or using the arrow keys / A and D. Your car races forward on its own. A **Full screen** button is available if your browser supports it.
- **Traffic:** rival vehicles labelled BTC, ETH, USDT, DOGE, LTC and XRP drift down the other lanes — the tickers are just for flavour, they all behave the same. Switch lanes early; the road gets faster and busier the longer you last.
- **XNO nitro:** a glowing XNO coin drifts down a lane now and then — drive into it for a few seconds of invincibility that lets you plough straight through traffic, plus double score while it lasts.
- **Daily challenge:** the same traffic for everyone, new every day at 00:00 UTC. Dodge 60 vehicles without running out of lives to clear the day and keep your streak.
- **Quick 60:** 60 seconds, score as much as you can.
- **Survival:** endless — traffic gets faster and more frequent the longer you last.
- **Lives:** 3 to start (4 for supporters), with a brief shield after each hit.
- **Scoring:** points for distance covered plus a bonus for every vehicle dodged, which grows with your combo; a hit resets the combo.
- **Ranks** (by total vehicles dodged): Newbie, Hodler (150), Diamond Hands (500), Whale (1,500), Satoshi (4,000).

Everything is stored in the player's browser.

## Deploy on GitHub Pages

1. Create a new repository, for example `block-racer`.
2. Upload `index.html` and `README.md` to the root of the repository.
3. Open **Settings > Pages**, set the source to **Deploy from a branch**, choose `main` and `/ (root)`, then save.
4. After a minute the game is live at `https://<your-username>.github.io/block-racer/`.

## Donations

The tip card works the same way as in the other Feeless games:

- A `nano:` payment link with the chosen amount, shown as a QR code and an **Open in wallet** button.
- A **Copy address** button.
- An **I've sent it, check** button that asks public Nano nodes whether a matching payment arrived, and unlocks the supporter perks (Gold, Mint and Neon accent colours, and a 4th life) on that browser.

To use a different wallet, change `NANO_ADDRESS` near the top of the script in `index.html`. If the public RPC endpoints in `RPCS` ever block browser requests, point them at your own proxy.

The supporter unlock is stored in `localStorage`, so it is a thank-you perk, not secure access control. Vehicle tickers and colours are used for fun and are not endorsements.

Add `?selftest` to the URL to expose a small `window.__br` object for automated tests.
