# Sushi by the Sea

A colourful seaside sushi restaurant for 1–4 friends, built in Unity for desktop browsers.

**[Play together](https://bjbaker93.github.io/sushi-by-the-sea/)**

## Invite friends

1. Open the game in a desktop browser and choose Create Room.
2. Send friends the play link and the room code shown in your lobby.
3. Friends choose Join Room and enter the code. Everyone readies up; the host starts the shift.
4. Prepare at your own pace, then ready the crew to open early. Serve the visible queue, see results, and continue to the next day.

Rooms support up to four players. Everyone must load the same current game version. The website is public; room codes let your group join the same restaurant. No downloads or accounts are needed to play. A stable internet connection is required.

## Controls

| Key | Action |
| --- | --- |
| WASD | Move |
| Shift | Short dash in the direction you face |
| E | Context interaction: take, add an ingredient, pick up a plate, serve, or deposit a dirty dish |
| Hold E at sink, hands empty | Wash the queued dishes, oldest first |
| Q | Drop the item in your hand |
| Arrow keys | Follow each fresh sashimi cutting sequence |
| Space | Stop beer / fishing timing |
| B | Recipe book |

## Make a plate

**Nigiri:** empty plate → rice → sashimi.

**Maki:** empty plate → nori → rice → sashimi.

Carry the plate to the rice/nori or carry ingredients to a plate on the island. Each plate holds one sushi. Once placed, ingredients stay on the plate; use the bin to discard a failed recipe while keeping the reusable plate. Pocketed toppings affect quality when sashimi completes the recipe.

A customer's thought bubble shows the requested type, minimum stars per plate, and beer if wanted. Later orders can ask for two or three plates; every plate must independently meet the type and star target. Several weaker plates do not add up to a stronger one.

After a guest leaves, collect their dirty plates and mug. Press E at the sink to leave them there; any chef can hold E with empty hands to wash the queue. Clean dishes automatically return to the stockpile.

## Build and hosting

This repository contains the playable Web distribution, not the Unity source project. Version 0.3.0; Unity 6000.6.0f1; Photon Fusion 2.1.2 Shared Mode. The original project and design package remain in the owner's local workspace.

GitHub Pages publishes `main` from the repository root. Unity gzip decompression fallback produces `.unityweb` payloads, so custom compression headers are unnecessary. Upload a complete matching set of the HTML, loader, data, framework and WebAssembly files when updating. Do not mix versions. `build-manifest.json` records the deployed file hashes.

## Playtest notes

This is an evolving vertical slice. Saves and the recipe book are local to the browser and site address. Moving from localhost to this site does not transfer those saves. The run owner can resume saved progress in a newly created room after a disconnect; progress since the latest save may be lost. Refresh all clients after an update. Desktop Chrome has been the primary test browser; touch/mobile support is outside this slice.

The bundled DejaVu Sans font retains its notice in `DejaVuSans-LICENSE.txt`.
