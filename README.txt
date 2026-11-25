AOL for 2 - The Adventure of 2 Links

TL;DR To enable Player 2, press 'select' on controller 2 while the spell screen is open (spell screen is opened by pressing 'start' on either controller). To save the game at any time, press Up+A on controller 1 while on the spell menu.

Notice:

If you notice any bugs, I would like to try to reproduce them and fix them. Please report them here: https://github.com/pharmville/Zelda2-nes-2player-patch/issues

My goal is a romhack that will work on real hardware, but I no longer have a NES or flashcart to test with. If you run into a problem on real hardware, please report it at the link above.

For the best experience, in your emulator (tested in MesenCE and FCE Ultra), enable the following (hardware-inaccurate) improvements:
-Remove sprite limit (removes sprite flickering)
-Overclocking: Additional scanlines before NMI - 262 (Eliminates lag)

Description:

AOL for 2 is a 2-Player romhack for Zelda II - The Adventure of Link. In this hack, Player 2 is not a "2nd-class citizen" but instead the goal is to allow Player 2 to perform any action that player 1 can! This includes fighting, casting spells, talking to townspeople, picking up items, transitioning the screen, flying around as fairy, and more. Additionally, bosses and enemies are aware of Player 2, and will target him too (when appropriate). Players share life, magic, and spellcasting effects. The shared Camera keeps both players on-screen at all times, and the camera dynamically centers exactly at the middle of their positions, until scrolling is no longer appropriate (due to reaching the edge of the screen). There is only one part of the game where player 2 is on the sidelines: The overworld map. Player 1 controls where the "Links" go.

Player 2 can join in (or leave) at any time by pressing 'select' on controller 2 while the spell screen is open. When player 2 is disabled, 'start' on controller 2 will still bring up the spell screen, so you don't even need player 1's help to join.

You can also customize your difficulty, and this difficulty will apply to both vanilla and coop modes. With the spell screen open, pressing 'select' on controller 1 will change the difficulty. Current difficulty is displayed on-screen in the upper right of the HUD. Pressing select will cycle between Normal, Hard, and Easy. Default for new saves is Normal. Difficulty is retained through .sav data whenever you save your game, but difficulty may also be changed at any time during play, by using this 'select' toggle.

Easy - Players take half damage
Normal - Vanilla Behavior
Hard - Players take 1.5x as much damage

Future plans:

This hack is feature-complete according to my tastes. Future improvments will probably be looking for ways to speed it up, so it isn't as laggy. Also fixing any remaining bugs as they are found.

Integreated patches:

Other romhacks that are integrated into AOL for 2 are listed below, along with their links and descriptions.

Zelda II Lag Reduction Patch (https://www.romhacking.net/hacks/8875/)

This patch optimizes several Z2 functions to significantly reduce CPU usage and thus the potential for lag. Changes that apply to the overworld reduce CPU usage by up to 7% and changes that apply to side-scrolling reduce CPU usage by up to 9%. These reductions have a very noticeable impact on the occurrence of lag, with some of the laggiest areas in the game being reduced to only mildly laggy.

The Adventure of Link: Refined (https://www.romhacking.net/hacks/9422/)

“The Adventure of Link: Refined” is a purist-friendly improvement patch that aims to create the ideal vanilla version of Link’s second adventure on the NES.

The guiding vision of this project is to refine (and in many cases fix) the original localization of “The Adventure of Link” without losing its unique charm or changing iconic lines beyond recognition.

This patch corrects the most distracting localization issues while keeping the original English wording intact wherever possible and respecting the original NES dialogue limitations. It also adds manual saving and includes a selection of small, unobtrusive improvements (faster text printing, smoother printing sound, and anti-seizure adjustments).

The patch features the following content:

Text Refinement

    Grammar, spelling, and punctuation errors have been corrected.
    Awkward or slightly mistranslated lines have been reworded.
    Text abbreviations have been avoided.
    Overly cryptic lines have been made clearer for new players.
    The full canonical terms “Magic Container” and “Heart Container” have been used in NPC hints.
    Text has been extended with relevant information.
    Redundant or nonessential information has been cut to make room for more relevant text.
    In extreme cases: nonsensical, misleading, or overly redundant dialogue has been replaced with alternatives.
    The limits of the original western release have been respected and preserved: four lines of text per dialogue, with a maximum of eleven characters per line, and only period, exclamation mark, and question mark as available punctuation.

Improvements

    Manual saving has been added (press Start to open the spell menu—or pause the game in the overworld—then press Up+A to open the save menu). (by ShadowOne333)
    The original typewriter-like text printing sound has been replaced with a smoother alternative. (by ShadowOne333)
    Anti-seizure measures (as seen in later revisions) have been implemented. (by ShadowOne333)
    Text printing speed has been increased. (by ShadowOne333 and Furo_19)

Special thanks to the creators of those romhacks! This romhack is much better than it would be without their efforts.

Rom info:

Zelda II - The Adventure of Link (U) [!].nes (headered rom)
SHA256: ad8c0fbcf092bf84b48e69fd3964eea4ed91bfe62abc352943d537979782680c
Once Patched SHA256: bc281ec0eeef14c0bcf837942be3df0680c3c7104c164fc14a532c6c0cd0ca97
Patch your rom using the online patcher here: https://www.romhacking.net/patch/

Special thanks to the creators of:

-Z22: The Adventure of Link and Lonk (zelda 2 coop - seems not quite finished)
-The Legend of Zelda: Z for 2 (zelda 1 coop - tons of fun, highly recommended)

Those romhacks were a blast! Z22 got me started, and helped me realize "what more" I wanted to improve upon. I started by fixing an issue with Z22 that would corrupt .sav ram thus making it impossible to get the water of life. But I didn't stop there, and eventually this romhack became the result of my much bigger plans. Also, playing through Z for 2 (zelda 1 coop) with my son helped me realize what a blast these older Zelda games can be when both players are equal partners. Now Zelda 2, the black sheep of the zelda games, gets to have similar treatment for multiplayer as Zelda 1! And yes, he and I have enjoyed playing through this completed romhack as well.

Also indispensable to the creation of this hack:

Disassembly - 99.99% of the work was done for me, here: https://github.com/FiendsOfTheElements/z2disassembly
Data Crystal - https://datacrystal.tcrf.net/wiki/Zelda_II:_The_Adventure_of_Link
ChatGPT - Absolutely amazing how quickly (and how accurately) it implements asm, works around space constraints, tracks down bugs, and more.
MesenCE - The debugger is incredible!
