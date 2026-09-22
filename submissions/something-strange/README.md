# Something Strange

**Builder / contact**

Sharp · [@Sharpbigred](https://x.com/Sharpbigred) · [stevereynolds2006-ship-it](https://github.com/stevereynolds2006-ship-it)

**Category**

Character Spotlight

**SDK:** FriendSDK v0.1.2

## What did you build?

A walkable outpost game where your Rare Friend buys a tuning fork, strikes it at a dish that should not be answering, and keeps whatever strange object replies.

## How does it use Rare Friends?

You play as your own Generations NFT. The FriendSDK runtime connects the wallet, verifies a hardwired Friend (generation ≥ 1) on Robinhood mainnet, and draws that Friend with its original character artwork. Simulated $RAREFRIENDS pays for forks and redeems answers.

## Source code

[github.com/stevereynolds2006-ship-it/something-strange](https://github.com/stevereynolds2006-ship-it/something-strange) · FriendSDK v0.1.2 · React 19 · TypeScript

Game component: `game/index.tsx`, `game/game.json`, `game/style.css`

## Playable demo / how to run

**Instant preview (no wallet):** [htmlpreview demo](https://htmlpreview.github.io/?https://github.com/stevereynolds2006-ship-it/something-strange/blob/main/demo/index.html)

The instant preview uses the same rules and copy. It is labeled simulated and does not replace the SDK ownership gate.

**FriendSDK preview** (wallet + hardwired Generations NFT, generation ≥ 1, Robinhood mainnet chain 4663):

```sh
git clone https://github.com/spokesz/friendsdk.git
cd friendsdk
npm ci
npm run build
git clone https://github.com/stevereynolds2006-ship-it/something-strange.git /tmp/something-strange
mkdir -p games/something-strange
cp /tmp/something-strange/game/* games/something-strange/
npm run dev:game -- games/something-strange
```

Open the printed URL (normally `http://localhost:4173`). Connect wallet, select your Friend. Preview play is simulated: no RF spend and no transaction signature.

## How do you play?

Move with WASD, arrow keys, or tap/click. Walk to **Listening post**, buy a simulated tuning fork (1 RF), walk to **Strike a fork**, and keep or redeem the answer from **Cabinet**. Settings include mute and reduced motion. Reloading resets preview state.

## Costs and rewards

Everything is simulated. Expected reward is 0.84 RF per fork. One fork produces exactly one answer. Each purchased or pending fork reserves 6 RF. Kept objects have no redemption expiry.

| Answer | Chance | Redemption |
| --- | ---: | ---: |
| A door that opens onto itself | 30% | 0.25 RF |
| A second shadow | 25% | 0.40 RF |
| A clock that counts sideways | 18% | 0.75 RF |
| A room that remembers you | 12% | 1.00 RF |
| A Friend-shaped hole | 8% | 1.75 RF |
| Static that knows your name | 5% | 3.00 RF |
| The other Friend | 2% | 6.00 RF |

World artwork: FriendSDK Orbital Array preset. Character art: canonical Rare Friends Generations sprites. See FriendSDK NOTICE.

## Checks and known issues

- `npm run check:games` in the FriendSDK checkout reports `games/something-strange: valid; expected reward 840000000000000000; maximum 6000000000000000000 RF base units`.
- Instant demo does not perform wallet or NFT ownership checks. Official play requires FriendSDK + an eligible Friend.
- No live contracts. No persistence across reloads. No hosted GitHub Pages SDK build yet (wallet-gated preview still runs locally).
- HUD buttons sit near the runtime toolbar on small screens; touch targets remain usable.
