# Rare Friends: Outbreak

**Builder / contact**

Sharp · [@Sharpbigred](https://x.com/Sharpbigred) · [GitHub @stevereynolds2006-ship-it](https://github.com/stevereynolds2006-ship-it)

**Category**

Character Spotlight

**What did you build?**

A zombie-apocalypse outpost where you walk your Rare Friend through a barricaded courtyard, buy Raid Kits, and send them through an outbreak gate to scavenge.

**How does it use Rare Friends?**

You play as your own Generations NFT, using its original walking artwork. Connect your wallet and choose your Friend to enter the outpost. The selected Friend is the only survivor you control.

**Source code**

[github.com/stevereynolds2006-ship-it/rare-friends-outbreak](https://github.com/stevereynolds2006-ship-it/rare-friends-outbreak) · FriendSDK v0.1

**Playable demo / how to run**

No hosted demo yet.
With Node.js 22+ installed:

```sh
git clone https://github.com/spokesz/friendsdk.git
cd friendsdk
git clone https://github.com/stevereynolds2006-ship-it/rare-friends-outbreak.git /tmp/outbreak
cp -R /tmp/outbreak/games/outbreak games/outbreak
npm ci
npm run dev:game -- games/outbreak
```

Open the printed URL.
You'll need a browser wallet holding a hardwired Generations NFT (generation 1 or higher) on Robinhood mainnet.
No RF funding or transaction signature is needed for the preview.

**How do you play?**

Move with WASD, arrow keys or click/tap.
Buy a Raid Kit at **Supply locker**, walk to **Outbreak gate**, and send your Friend through.
Keep the haul or redeem it from **Stash**.
Settings include mute and reduced motion.
Everything stays inside the SDK's 960 × 640 container.

**Costs and rewards**

Everything is simulated.
Each Raid Kit costs 1 RF (`1000000000000000000` base units) and produces one haul.

| Find | Chance | Redemption value |
| --- | --- | --- |
| Empty Can | 15% / 1,500 bps | 0 RF |
| Scrap Metal | 28% / 2,800 bps | 0.25 RF |
| Medkit | 22% / 2,200 bps | 0.50 RF |
| Ammo Cache | 14% / 1,400 bps | 0.75 RF |
| Fuel Drum | 9% / 900 bps | 1.50 RF |
| Safehouse Key | 6% / 600 bps | 2.50 RF |
| Gold Tooth | 4% / 400 bps | 5 RF |
| Genesis Relic | 2% / 200 bps | 10 RF |

Expected reward is 0.97 RF per kit.
Every purchased or pending kit reserves 10 RF of backing.
Kept hauls have no redemption expiry.

**Checks and known issues**

`npm run check:games` in FriendSDK with this game in `games/outbreak`:
valid; expected reward `970000000000000000`; maximum `10000000000000000000` RF base units.

SDK typecheck and full browser suites were not re-run against a published host.
Preview progress resets when the session ends.
No live token spending, trading, wearable NFTs or creator fees are included.

**Credits**

World geometry from the FriendSDK `02-circuit-courtyard-complete` preset.
Character sprites and sound kit from FriendSDK v0.1.
No third-party assets.
