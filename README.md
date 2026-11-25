# AOL for 2 - The Adventure of 2 Links

> [!TIP]
> **TL;DR:** To enable Player 2, press **Select** on Controller 2 while the spell screen is open (open the spell screen by pressing **Start** on either controller). To save the game at any time, press **Up + A** on Controller 1 while the spell menu is open.

## Notice

If you notice any bugs, I would like to try to reproduce and fix them. Please report them on the [GitHub Issues page](https://github.com/pharmville/Zelda2-nes-2player-patch/issues).

My goal is a ROM hack that will work on real hardware, but I no longer have a NES or flashcart to test with. If you run into a problem on real hardware, please report it at the link above.

For the best experience in your emulator (tested in **MesenCE** and **FCE Ultra**), enable the following (hardware-inaccurate) improvements:
* **Remove sprite limit:** Removes sprite flickering
* **Overclocking (Additional scanlines before NMI - 262):** Eliminates lag

## Description

**AOL for 2** is a 2-player ROM hack for *Zelda II: The Adventure of Link*. In this hack, Player 2 is not a "2nd-class citizen" —the goal is to allow Player 2 to perform any action that Player 1 can! This includes:
* Fighting
* Casting spells
* Talking to townspeople
* Picking up items
* Transitioning screens
* Flying around as a fairy
* Placing palace crystals
* Probably more I am forgetting

Additionally, bosses and enemies are aware of Player 2 and will target him when appropriate. Both players share life, magic, and spellcasting effects. The shared camera keeps both players on-screen at all times, dynamically centering exactly at the midpoint of their positions until scrolling is no longer appropriate (such as reaching the edge of the screen). The only part of the game where Player 2 is on the sidelines is the overworld map, where Player 1 controls where the "Links" go.

### Drop-In / Drop-Out Co-op
Player 2 can join or leave at any time by pressing **Select** on Controller 2 while the spell screen is open. When Player 2 is disabled, pressing **Start** on Controller 2 will still bring up the spell screen, so you don't even need Player 1's help to join.

### Difficulty Settings
You can customize your difficulty, which applies to both vanilla and co-op modes. With the spell screen open, pressing **Select** on Controller 1 cycles between **Normal**, **Hard**, and **Easy** (default for new saves is Normal). The current difficulty is displayed in the upper right of the HUD and is saved to `.sav` data, though it can be toggled at any time during play:

| Difficulty | Effect |
| :--- | :--- |
| **Easy** | Players take half damage |
| **Normal** | Vanilla behavior |
| **Hard** | Players take 1.5x as much damage |

## Future Plans

This hack is feature-complete according to my tastes. Future improvements will focus on optimizing performance to reduce lag, as well as fixing any remaining bugs as they are found.

## ROM Info & Patching

Apply the patch to a clean, headered US ROM matching the checksums below:

* **Base ROM:** `Zelda II - The Adventure of Link (U) [!].nes` (Headered)
* **Base SHA-256:** `ad8c0fbcf092bf84b48e69fd3964eea4ed91bfe62abc352943d537979782680c`
* **Patched SHA-256:** `bc281ec0eeef14c0bcf837942be3df0680c3c7104c164fc14a532c6c0cd0ca97`

Use any ips patcher of your choosing. Here is an option: [romhacking.net online patcher] (https://www.romhacking.net/patch/).

## Integrated Patches

Other ROM hacks integrated into **AOL for 2** are listed below, along with their links and descriptions. Special thanks to the creators of these projects! This romhack is significantly better thanks to their efforts.

### [Zelda II Lag Reduction Patch](https://www.romhacking.net/hacks/8875/)
This patch optimizes several Z2 functions to significantly reduce CPU usage and the potential for lag. Changes to the overworld reduce CPU usage by up to 7%, and changes to side-scrolling reduce CPU usage by up to 9%. 

### [The Adventure of Link: Refined](https://www.romhacking.net/hacks/9422/)
*The Adventure of Link: Refined* is a purist-friendly improvement patch that aims to create the ideal vanilla version of Link’s second adventure on the NES. It corrects the most distracting localization issues while keeping the original English wording intact wherever possible and respecting original NES dialogue limitations, alongside small, unobtrusive quality-of-life improvements.

* **Text Refinement:**
  * Grammar, spelling, and punctuation errors have been corrected.
  * Awkward or slightly mistranslated lines have been reworded, and text abbreviations have been avoided.
  * Overly cryptic lines have been made clearer for new players, using the full canonical terms "Magic Container" and "Heart Container" in NPC hints.
  * Text has been extended with relevant information while cutting redundant text, replacing nonsensical or misleading dialogue where necessary.
  * Original western release limits are preserved (four lines per dialogue box, max 11 characters per line, using only periods, exclamation marks, and question marks).
* **Improvements:**
  * **Manual Saving:** Press **Start** to open the spell menu (or pause in the overworld), then press **Up + A** to open the save menu *(by ShadowOne333)*.
  * **Audio:** The original typewriter-like text printing sound has been replaced with a smoother alternative *(by ShadowOne333)*.
  * **Accessibility:** Anti-seizure measures (as seen in later revisions) have been implemented *(by ShadowOne333)*.
  * **Pacing:** Text printing speed has been increased *(by ShadowOne333 and Furo_19)*.

## Special Thanks & Credits

Special thanks to the creators of:
* **[Z22: The Adventure of Link and Lonk](https://www.romhacking.net/hacks/5243/)** *(Zelda 2 co-op)*
* **[The Legend of Zelda: Z for 2](https://www.romhacking.net/hacks/9882/)** *(Zelda 1 co-op — tons of fun, highly recommended)*

Those ROM hacks were a blast! *Z22* got me started and helped me realize what more I wanted to improve upon. I started by fixing an issue with *Z22* that corrupted `.sav` RAM and made it impossible to get the Water of Life, which eventually grew into this much larger project. Playing through *Z for 2* with my son also showed me how much fun these older Zelda games are when both players are equal partners. Now *Zelda II*, the black sheep of the Zelda series, gets similar multiplayer treatment — and my son and I have had a great time playing through this completed romack as well.

### Tools & Resources
Also indispensable to the creation of this hack:
* **[z2disassembly](https://github.com/FiendsOfTheElements/z2disassembly)** — 99.99% of the disassembly work was done for me here.
* **[Data Crystal](https://datacrystal.tcrf.net/wiki/Zelda_II:_The_Adventure_of_Link)** — Invaluable ROM and RAM documentation.
* **[ChatGPT](https://www.chatgpt.com)** — Amazing how quickly and accurately it implements ASM, works around space constraints, tracks down bugs, and more.
* **[MesenCE](https://github.com/nesdev-org/MesenCE)** — The debugger is incredible!
