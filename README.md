# Deity Zenith Dragonshard

A summoning, resource and captain levelling Cheat Engine table for **Dragonshard**, by Bener Kaya.

Deity Zenith lets you play god in **Dragonshard**. Pick something in the Cheat Engine table, point at the map with the mouse, press the summon key, and it appears there:

- **Units** of every faction, including heroes, monsters, neutral characters and wildlife
- **Buildings** of the three playable factions
- **Items**: potions, scrolls, rings, weapons and armour, champion artifacts and campaign quest items

You choose **whose side** the summons are on: **yourself**, the first enemy player, the **monster** player, the **wildlife** player, or any player slot. Items can be dropped on the ground or put straight into a player's inventory.

Deity Zenith can also **edit your Gold, Dragonshards and XP**, **level up your selected captains** to the level you pick, and **keep the game running** while you are in another window.

## Features

- **455 entries** with their in-game names: 252 units (including 19 heroes), 39 buildings and 164 items. Full list: `unit_list.txt`.
- **Picker**: **Faction** → **Category** (Unit, Building or Item) → **Summon**. Heroes are in the Unit list, marked **[Hero]**.
- **Count**: 1 to 25 per key press, spread in a small cluster.
- **Where**: at the mouse cursor, next to the selected unit or building, or (items only) straight into the owner's inventory.
- **Summon Key**: **Numpad0** by default; the middle mouse button, any other numpad key, or Off.
- **Resources**: edit or freeze your **Gold**, **Dragonshards** and **XP**.
- **Level Up**: raise your selected captains to the **Captain Level** you pick, with **one key** (**Numpad1** by default) or by ticking **Level Up Script**.
- **Run in Background**: the game and its sound keep running when you switch to another window (Alt+Tab) instead of pausing. On by default.

## What you need

- **Dragonshard**, GOG version **1.02.1.0** (Windows). Deity Zenith only works with that version's `Dragonshard.exe`; any other version or a modified exe is refused safely, and nothing is changed.
- **[Cheat Engine](https://www.cheatengine.org/) 7.5** or newer.
- Optional: **[dgVoodoo2](https://dege.freeweb.hu/dgVoodoo2/)**, to run the game in a window (or borderless fullscreen) so you can switch between the game and Cheat Engine easily.

## Install

Nothing to install, and nothing goes into the game folder. Put these files in any folder:

| File | What it is |
|---|---|
| `Deity Zenith Dragonshard.CT` | the Cheat Engine table |
| `unit_list.txt` | everything in the Summon lists, by faction and category, plus what was left out and why |
| `README.md` / `README.txt` | this guide |

The table works on its own: the lists are built into it. `unit_list.txt` is only there for reference.

### Optional: windowed or borderless with dgVoodoo2

dgVoodoo2 has no setting that stops the game pausing when you switch windows; use **Run in Background** for that. A window or dgVoodoo2's fake fullscreen makes switching between the game and other windows quick.


1. Copy the dgVoodoo2 DLLs for Direct3D 9 (`D3D9.dll` from its `MS\x86` folder) next to `Dragonshard.exe`, together with `dgVoodooCpl.exe`.
2. Run `dgVoodooCpl.exe` from the game folder. On the **General** tab, set the appearance to **Windowed** (or a borderless full-screen window), then **Apply**.
3. Start the game as usual. To undo, delete the files you copied.

## How to use it

1. Start **Dragonshard** and load a skirmish or campaign mission. Use a save you don't mind changing.
2. Start **Cheat Engine** and open **`Deity Zenith Dragonshard.CT`**.
3. Tick **Deity Zenith - Enable**. It connects to the game by itself (no need to pick the process), checks the game version, and the rows below it appear.
4. **Summon:** pick a **Faction**, a **Category** and an entry in **Summon**. Set **Count**, **Where** and **Owner**. Click back into the game, point at open ground (or select a unit or building first), and press **Numpad0** with **NumLock** on.
5. **Resources:** double-click the **Value** of **Gold**, **Dragonshards** or **XP** and type a number. Tick the box in front of one to freeze it; untick it to let it change again.
6. **Level up:** pick a **Captain Level**, select one or more of your captains in the game, and press **Numpad1** (or tick **Level Up Script**; the tick clears itself).
7. Untick **Deity Zenith - Enable** when you're done. That restores the original game code.

To change a setting, double-click its **Value** cell and pick from the list. Don't tick the setting rows themselves.

## The table

| Row | What it does |
|---|---|
| **Deity Zenith - Enable** | Connects to the game, checks the version, and turns everything on. Unticking it restores the original game code and unfreezes the resource rows. |
| **---Summon---** | |
| **Faction** | Order of the Flame, Lizardfolk, Umbragen, Monsters, Neutral NPCs, or Wildlife, cinematic and special. Ignored for items. |
| **Category** | **Unit**, **Building** or **Item**. Only the three playable factions have buildings. Items are the same under every faction. |
| **Summon** | The unit, building or item to summon. Default: Paladin (Order of the Flame). In the item list, normal items come first, then **[Artifact]** champion artifacts, then **[Quest]** campaign items. |
| **Count** | How many per key press, 1 to 25, spread in a small cluster. Each one is exactly what you picked: a captain comes alone, without soldiers. |
| **Where** | **At mouse cursor** (default): the ground under the pointer, on the layer you're looking at (surface or underground). **At selected unit or building**: next to the first unit or building you have selected; buildings are placed beside it, not on top. **Into owner's inventory** (items only): the item goes straight into the Owner's item slots. |
| **Owner** | **You (player)** (default). **First enemy player**: the first living player that isn't you or your ally. **Monsters (player 8)**: the game's monster player, hostile to everyone. **Wildlife / neutral (player 9)**: the ambient wildlife player. **Player slot 0** to **7**: that exact slot. Owners not in the current game are refused. Ground items belong to nobody, so Owner only matters for **Into owner's inventory** (player slots only). |
| **Summon Key** | **Numpad0** (default), **Middle mouse**, **Numpad1** to **Numpad9**, **Numpad \***, **Numpad +**, **Numpad -**, **Numpad .**, **Numpad /**, or **Off**. Keys the game also uses are marked, for example `Numpad8 (game: camera zoom in)`. |
| **---Resources---** | Your own resources in the current battle. |
| **Gold** | Your gold. Type a new amount, or tick the box to freeze it. |
| **Dragonshards** | Your dragonshards. Type a new amount, or tick the box to freeze it. |
| **XP** | Your experience (XP) pool. Type a new amount, or tick the box to freeze it. |
| **---Other---** | |
| **Captain Level** | The level **Level Up** raises captains to: 2 to 6. Default **5**, the highest level the game sells. **6** is a bonus level that exists in the game data but isn't sold in the game. |
| **Level Up Key** | The key that runs Level Up while you're in the game. Same key list as **Summon Key**; default **Numpad1**. If it's the same key as Summon Key, it's switched off until you pick a different one. |
| **Level Up Script** | A one-shot button: tick it and it unticks itself. Levels every captain of yours in your current selection to **Captain Level**, exactly like the Level Up Key. |
| **Run in Background** | **On** (default): the game keeps running, drawing and playing sound when you switch to another window. **Off**: the game pauses when it loses focus, as it normally does in single player. Works while **Deity Zenith - Enable** is ticked; unticking Enable puts the normal pause back. |
| **Status** | What happened on the last key press. |
| **Diagnostics** | Tick it to show the rows below it (untick to hide them; they keep updating). Last result, how many were summoned, spots skipped, owner player used, your player slot, free unit slots, network mode, the last Level Up (the first captain's level before and after, and its unit type), and live Run in Background readings: whether the game code and the sound setting are changed, the game's own active, frame loop and paused flags, a game tick counter that rises while the battle runs, the game screen state and the session type. |

## What you can summon

| Faction | Units | Buildings |
|---|---|---|
| Order of the Flame | 25 (4 heroes) | 11 |
| Lizardfolk | 26 (4 heroes) | 11 |
| Umbragen | 26 (5 heroes) | 17 |
| Monsters | 85 | 0 |
| Neutral NPCs | 39 (6 heroes) | 0 |
| Wildlife, cinematic and special | 51 | 0 |

**Items** (164, the same list under every faction): 76 normal items, 24 **[Artifact]** champion artifacts (each for one named hero, for example `[Artifact] Dagger of Frost (Kael)`) and 64 **[Quest]** campaign items. Most can go either on the ground or into an inventory; `unit_list.txt` marks the few that only work one way.

Left out on purpose (all listed at the end of `unit_list.txt`): unfinished units and items, the menu-only hero portraits, Nexus walls, gates and wall towers, town centres, Nexus monuments and expansion monoliths.

## Good to know

- **NumLock must be on** for the numpad keys. With NumLock off, Windows sends them as arrows, Home, End and so on.
- **Numpad keys the game also uses:** Numpad2 to Numpad6, Numpad8 and Numpad9 move the camera, and Numpad + and Numpad - change the volume. They're marked in the key lists. The defaults (Numpad0 and Numpad1) are free, as are Numpad7, Numpad \*, Numpad . and Numpad /.
- **Captain levels are per type.** Dragonshard levels a captain *type*, not a single unit. Levelling one Cleric levels all your Clerics, including ones you train later, just as buying the level in the game does. The levels count as bought.
- **Levels are only raised.** A captain already at or above the chosen level is left as it is.
- **Heroes are not levelled.** The game has no captain levels for heroes. Soldiers, juggernauts and units that aren't yours are skipped too.
- **Level 6** is a bonus level beyond what the game sells. It works, but the game may show no upgrade text for it.
- **Resources:** the game caps Gold and Dragonshards at 99,999 and XP at 99,000. Higher amounts are lowered the next time you gain that resource. Negative amounts are set to 0.
- **Quest items** can trigger or confuse mission scripts, for example a key that opens a gate early. **Champion artifacts** given to your inventory may unlock that hero's artifact for the rest of the campaign.
- **Extra heroes** and copies of campaign characters can confuse hero menus, mission scripts or objectives.
- **Buildings** are placed where you point, not snapped to your town grid. Another faction's building may behave oddly.
- **Cinematic and special units** are mostly for scripted scenes and may just stand there.
- Units pick up ground items the normal way, so an enemy can grab an item you drop near it.
- Deity Zenith always leaves room in the game's unit limit, so the game never runs out of space for its own units.
- **Single player only.** Dragonshard multiplayer keeps every PC's game in lockstep; a unit created on one PC only would break the game.
- Closing the game while Enable is ticked is safe: Deity Zenith notices and switches itself off.
- **Run in Background** only changes the game in memory, never the game files, and only while Enable is ticked.
  - The battle really goes on while you're away: enemies keep attacking and your resources keep growing.
  - Sound and music keep playing too, from the moment you tick Enable; no need to restart the game or reload a battle.
  - If you paused the game yourself before switching away, it stays paused.
  - Keys you type in other windows go to those windows, not to the game.
  - The mouse is let go when you switch away and locked to the game again when you come back.
  - The game keeps using your processor and graphics card while you are away.
  - It works best with the game in a window or in dgVoodoo2's fake fullscreen. In the game's own exclusive fullscreen, Windows may minimise the game when you switch away; the battle still runs, but you see it again only when you switch back.

## Troubleshooting

| What you see | What to do |
|---|---|
| "Start Dragonshard first" | Start the game, then tick Enable again. |
| "not the supported GOG 1.02.1.0 build" | Only that exact game version is supported. Nothing was changed. |
| "already changed by another tool" | Another trainer or table has changed the same game code. Close it and restart the game. |
| "An older Deity Zenith Dragonshard table is still switched on" | An older copy of this table is still on in this game. Untick Enable there (or restart the game), then tick it here. |
| The game still pauses when you switch windows | Tick **Deity Zenith - Enable** and set **Run in Background** to **On**. If you paused the game yourself, it stays paused. If it still stops, tick **Diagnostics**, switch away for a few seconds during a battle, switch back, and take a screenshot of the Diagnostics rows. |
| Status: "Run in Background is not available" | Another tool has changed the same game code. Close it and restart the game. |
| Status: "...but its sound could not be kept on" | Another program (for example an audio or overlay tool) has changed how the game's sound reacts to switching windows. The game still keeps running; close that tool and restart the game to get the sound back in other windows. |
| A numpad key does nothing | Turn **NumLock** on, and click into the game window first. |
| A numpad key also moves the camera or changes the volume | Pick a key that isn't marked "(game: ...)". |
| Status: "Summon Key and Level Up Key are the same key" | Pick a different **Level Up Key**. |
| Status: "Not in a battle yet" / "The game is not running a battle" | Load a skirmish or mission, return to the battle, and press the key again. |
| Status: "Multiplayer or a save being loaded" | Summoning is off in multiplayer. After loading a save, wait until the game runs. |
| Status: "The game is paused" | Unpause, then press the key again. |
| Status: "Mouse cursor is not over the ground" | Point at the map, not at the sky or the interface. |
| Status: "Nothing selected" | Select a unit or building first, or set **Where** to **At mouse cursor**. |
| Status: "That spot is outside the map" | Point closer to the middle of the map. |
| Status: "Unit limit almost reached" | The game is close to its unit limit. Remove some units first. |
| Status: "Inventory full" | Use some items, or drop the item on the ground instead. |
| Status about an item's ground object or inventory | Some items only work on the ground, others only in an inventory. Switch **Where**. |
| Status: "Level Up: nothing selected" | Select one or more of your captains first. |
| Status: "Level Up: nothing levelled" | The Status line says why: already at that level or higher, a hero, not a captain, or not yours. |
| Status: "Level Up ... waiting for the game" | Switch back to the running battle within 30 seconds. |
| **Gold**, **Dragonshards** or **XP** shows "(not in a battle)" or "(multiplayer: off)" | Load a single-player battle; the rows follow your player as soon as it runs. |
| A frozen resource stopped being frozen | Rows are unfrozen when a battle ends or a new one starts. Tick the box again. |
| Names look cut off | Drag the right edge of the **Value** column header to widen it. |

## Credits

Deity Zenith Dragonshard by **Bener Kaya**.
Dragonshard is a trademark of its respective owners. This is an unofficial fan-made table.
