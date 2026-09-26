# Ashwalk

## Project name

Ashwalk

## Builder / contact

Sharp · [X @Sharpbigred](https://x.com/Sharpbigred) · [stevereynolds2006-ship-it](https://github.com/stevereynolds2006-ship-it)

## Category

Character Spotlight

## What did you build?

A side-scrolling fog platformer where your Rare Friend walks the woods, lights bells, and outruns the thing under the ground.

## How does it use Rare Friends?

You play as your own Generations NFT, using its original character artwork. Connect a wallet to choose a Friend you own and to read your $RAREFRIENDS balance. That balance is what the game spends.

## Source code

[github.com/stevereynolds2006-ship-it/ashwalk](https://github.com/stevereynolds2006-ship-it/ashwalk) · FriendSDK v0.1.2

Node.js 22+. A browser wallet holding a hardwired Generations NFT (generation 1 or higher) on Robinhood mainnet.

```bash
git clone https://github.com/stevereynolds2006-ship-it/ashwalk.git
cd ashwalk
npm ci
npm run dev
```

Open the printed URL.

## Playable demo

There is no separate hosted build yet. The playable preview is `npm run dev` from the source repository above. No transaction signature is required. Rare-coin costs are simulated against the balance the wallet reports: the game subtracts them on this device and does not send a chain transfer.

## How do you play?

A and D, or the arrow keys, move. W, up, or space jumps. S drops through a cage. E pulls a rope, lights a bell, or buys a lantern. On a phone, use the buttons at the bottom. Mute and reduced motion are in the corner.

The shore is open first. Beating a fog opens the next one. Six fogs: the shore, the latch, the gale, the choir, the sign, and the antler. The antler wakes something buried. Lead it into the cage and stand on the plate. Its arms keep moving.

With friends, open a room code and have the other person join it. Bells, ropes, and coins in a room are shared.

## Costs and rewards

Everything is simulated.

- 5 Rare coins starts a walk. It does not give you coins. You collect those in the fog.
- 20 Rare coins opens every fog. Walks are free after that.
- A death burns half the coins collected on that walk. Three lives, then another walk costs 5 Rare coins.
- A lantern costs 1 collected coin and lasts 10 seconds on the dark boards. A flashlight costs 5 collected coins.
- Clothes cost Rare coins. One rare piece changes each Monday UTC. Bought clothes stay on that wallet in this browser.

## What have you tested?

`npx tsc --noEmit` passes. Solo play was checked in the browser on desktop and a phone-sized layout: movement, jumps, bells, the cage, the wallet balance, and the level lock. A full automated browser suite against a fresh clone has not been re-run for this submission.

## Known limitations

Rare-coin spends and clothes are stored in localStorage for the connected address. They are not on-chain transfers, and they do not follow the wallet to another browser. Collected coins on a walk are not added to the wallet balance. Clearing a fog is also stored on this device. Multiplayer needs the dev server's signaling route. There is no hosted public URL yet.

## Credits

Original silhouette art, levels, and music. The Friend sprite, halo, and wallet read come from FriendSDK v0.1.2. The fog, dead trees, and the antler creature are original drawings in the spirit of monochrome side-scrollers, not copied from a game.
