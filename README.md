# Sushi by the Sea

A colourful seaside sushi restaurant for 1–4 friends, built in Unity for desktop browsers.

**[Play together](https://bjbaker93.github.io/sushi-by-the-sea/)**

## Invite friends

1. Enter your name, choose **Human, Frog, Fish or Mouse**, and pick one of six outfit colours.
2. For a fresh run, select starting **round 1, 5 or 10**, then **Create Restaurant**. Each starting round provides matching funds and equipment. **Resume Saved Run** is a separate choice when a checkpoint exists.
3. Send friends the play link and room code. Friends choose **Have a Code? Join a Friend**, enter the code, then **Join Restaurant**.
4. Everyone selects **I'm Ready**; the creator selects **Enter Restaurant**. Explore and prepare at your own pace, then have every chef choose **Open Restaurant**. Serve the finite queue, review Results, and continue to the next round.

Rooms support up to four players. Everyone must load the same current game version. The website is public; room codes let your group join the same restaurant. No downloads or accounts are needed to play. A stable internet connection is required.

## Controls

| Key | Action |
| --- | --- |
| WASD or arrow keys | Move with short acceleration, deceleration and smooth turning |
| Shift | Short dash in the direction you face |
| Tap E | Pick up/place an item, combine ingredients, serve, or deposit a dirty dish |
| Hold E over a whole fish on a counter | Start a fresh cutting sequence |
| Arrow keys while cutting | Follow the cutting arrow shown above your chef |
| Hold E at sink, hands empty | Wash the queued dishes, oldest first |
| Q | Drop the item in your hand |
| E or Space | Stop beer / fishing timing |
| 1 / 2 | Select a topping pocket |
| B | Recipe book |
| Esc | Options / close |

During cutting, arrow keys control the sequence. Release them after the cut before using them to move again.

Walking is faster than the plate revision: 9.9 units/second with a short acceleration and stopping response. Leave room to turn around the solid kitchen island.

## Make sushi, then build a board

Take a fish from the walk-in cold room and place it on any free preparation tile. **Tap E picks the fish up; hold E starts cutting.** Every portion requires its own fresh arrow sequence. Mistakes or cancellation still consume the portion and reduce its value.

Combine **loose cut fish + rice = Nigiri**. Add **nori = Maki**. Ingredients work in any order: rice plus nori can wait for fish, fish plus nori can wait for rice, and loose Nigiri can still receive nori. Carry compatible ingredients together at a supply or bring one to another on a counter. Pocketed toppings improve sushi when it first completes; upgrading loose Nigiri preserves its quality and toppings.

Put **one to three completed sushi on a reusable wooden board**. The total stars float above the board, including the recipe-variety bonus. Once boarded, sushi cannot be removed or changed. Raw ingredients stay separate from boards. Use the bin for unwanted food; a used board remains a dirty reusable dish.

Every empty counter tile can hold one item. The central island is one continuous solid bench with six usable tiles, and side counters provide more workspace. Empty bar tiles can be used for preparation too; clear them so customers can sit there.

## Serve and wash

A customer's thought bubble shows the requested sushi type and **whole-board** star target, plus beer when wanted. Normal orders ask for one board and/or one beer. A nonempty wrong-type or low-value board is accepted as a failed order and applies its HYPE penalty once. Choose a board's contents and total carefully.

Preparation has no time limit. Service has a finite queue and shorter customer patience, with a **ROUND N** announcement when it opens. Beer requests begin in round 3 for around half the guests. Stop the filling mug in its ideal band above the chef, then serve it to support patience.

After guests leave, collect dirty boards and mugs. Tap E at the sink to deposit a dish and free your hand. Any chef can then hold E with empty hands to wash the queue oldest-first, continuing through consecutive dishes. Release to pause. Other chefs can deposit while washing continues; clean dishes automatically return to stock. Clearing the bar frees seats.

## Build and hosting

This repository contains the playable Web distribution, not the Unity source project. Version **0.4.1**, board kitchen revision **26**; Unity **6000.6.0f1**; Photon Fusion **2.1.2 Stable 2279**, Shared Mode. The network version is `astra-boards-4`. The original project and design package remain in the owner's local workspace.

GitHub Pages publishes `main` from the repository root. Unity gzip decompression fallback produces `.unityweb` payloads, so custom compression headers are unnecessary. Upload a complete matching set of the HTML, loader, data, framework and WebAssembly files when updating. Do not mix versions. `build-manifest.json` records the deployed file hashes.

## Playtest notes

This is an evolving vertical slice. Saves and the recipe book are local to the browser and site address. Moving from localhost to this site does not transfer those saves. The run owner can resume saved progress in a newly created room after a disconnect; progress since the latest save may be lost. Compatible checkpoints migrate, while unsupported checkpoints are preserved rather than silently discarding their contents. Refresh all clients after an update.

The editable handoff's `ASTRA_BUILD_REPORT.md` records tests actually executed and remaining limitations. These play instructions do not certify a browser or multiplayer test. Desktop Chrome has been the primary test browser; touch/mobile support is outside this slice.

The original temporary art and audio accompany the game. The bundled DejaVu Sans font retains its notice in `DejaVuSans-LICENSE.txt`.
