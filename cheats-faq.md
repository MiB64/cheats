---
title: Cheats FAQ
layout: default
nav_order: 8
parent: MiB64 Cheats
description: Frequently asked questions about cheat codes in MiB64.
---

## <a name="cheats-faq">MiB64 Cheats FAQ</a> — Written By Gent

This should help you with any questions that you might have about adding & editing codes in the Cheat Database. Maximise this window if you are having trouble viewing it.

---

### The Do's & Don'ts of Adding & Editing Cheat Codes

**Q: Why don't the cheats work in MiB64?**  
I ticked what I wanted to use but it does nothing on all games I have tried. What can I do to make them work?

**A:** Make sure you have enabled your Memory Pak—otherwise some cheats will not work!  
Go to **Options → Configure Controller Plugin** to check.

---

**Q: Why can't I see any cheats in the menu? It's blank.**

**A:** This could be several reasons:

- The game you're playing has no cheat support yet. You can add cheats manually or wait for support.
- Make sure the `MiB64.cdb` file is in the root folder (same location as the MiB64 executable).
- There may be a memory hang caused by opening too many ROMs in one session. Restart MiB64 and reload your game.
- You may need to manually add a cheat to populate the menu.

---

### Manual Cheat Entry

Enter this example:

```text
Name: Test  
Code: 80123456 0001
```

Once added, close MiB64.  
Open the `MiB64.cdb` file in a text editor (e.g. Notepad).  
Search for your game's name.

Example:  
```text
Name=Super Mario 64
```

If nothing shows, try without spaces or verify the correct region.

---

### Region Codes

```text
(JU) = :41 (1080) — NTSC  
(J)  = :4A (Japan) — NTSC  
(U)  = :45 (USA) — NTSC  
(E)  = :50 (Europe) — PAL  
(A)  = :55 (Australia) — PAL  
(G)  = :44 (Germany) — PAL  
(F)  = :46 (France) — PAL  
(I)  = :49 (Italy) — PAL  
(S)  = :53 (Spain) — PAL
```

So for USA, you'd see:

```text
Name=Super Mario 64  
[635A2BFF-8B022326-C:45] <<<< Arrow points to the CRC  
Name=SUPER MARIO 64
```

Once found, copy the entire cheat entry for Super Mario 64 to the end `//----`  
Paste it below your test entry like this:

```text
[New-CRC-C:45]  
Name=SUPER MARIO 64 (Region)  
Cheat0="Test Cheat",80123456 0001
```

Now copy the test cheat CRC over the original one below it.  
Delete the old entry, save the file, and confirm overwrite.  
Happy cheating!

---

Once you have found it, copy the entire cheat entry for the game (e.g. //Super Mario 64 to the end //----) and paste it below the test cheat you added.

```text
[New-CRC-C:45]  
Name=SUPER MARIO 64 (Region)  
Cheat0="Test Cheat",80123456 0001
```

Now copy the test cheat CRC over the original one below it.  
Delete the one above, leaving only the new one added.  
Save the file, confirm overwrite, and close. Happy cheating!

---

### Persistent Cheats

**Q: Is there a way to make MiB64 remember cheats I left on in a game even after closing and reopening?**

**A:** Yes. On the MiB64 GUI, go to:  
**Options → Settings → Options → Remember Selected Cheats**

Any cheats left on when you closed MiB64 will be remembered and automatically enabled next time you load the game.  
Make sure to turn off any cheats you don’t want re-enabled before exiting.

---

### Finding Cheat Codes

**Q: Where do I find cheat codes to add myself into the cheat file?**

**A:** Just Google:

- “N64 Action Replay cheats” for PAL  
- “N64 Gameshark cheats” for NTSC

---

### Adding Cheats

**Q: How do I add cheat codes in MiB64?**

**A:** Click the [Adding Cheats](https://mib64.github.io/cheats/adding-cheats#adding-cheats) link for a full explanation.

Note: You do not need to add Enable or Keycode cheats.  
These are only used on real console cheat devices—MiB64 does not require them.

---

### Cheat Search

**Q: Can I search for my own cheat codes in MiB64?**

**A:** Yes. MiB64 allows you to search and test results, then add them to the database through the GUI.  
Go to [Preparing for Cheat Search](https://mib64.github.io/cheats/cheat-search#preparing-to-search) for more information.

---

### Cheat Management via GUI

**Q: Can I add, edit & delete cheat codes in MiB64 without opening the cheat file in a text editor?**

**A:** Yes. MiB64 allows you to manage cheats directly through the GUI.  
Click for more information on:  
[Adding](https://mib64.github.io/cheats/adding-cheats#adding-cheats),  
[Editing](https://mib64.github.io/cheats/editing-cheats#editing-cheats),  
[Deleting](https://mib64.github.io/cheats/deleting-cheats#deleting-cheats),  
and [Using Cheats](https://mib64.github.io/cheats/using-cheats#using-cheats)

---

### Editing Cheats via Text Editor

**Q: Can I add or edit codes in the MiB64.cdb file using a text editor?**

**A:** Yes, but you don’t need to—everything can be done via the GUI.  
If you still want to, open the cheat file in WordPad and search for the game name and region.

Example:  
```text
Name=Super Mario 64
```

Look at how the cheats are written:

```text
Cheat0="Ostrich Mario",8033B3BC 0090  
Cheat1="Mario Runs Backwards",8033B3BE 0070
```

Notice how the codes are separated by a space:  
`XXXXXXXX XXXX` — not `XXXXXXXXXXXX`

---

---

### Modify Codes and Options

Example:

```text
Cheat5="Open Level Character Modifier",8125508A 00??  
Cheat5_O=$01 Easy Level,$02 Easy & Normal Level,$03  
Cheat7="Play As Options",811653D2 00??  
Cheat7_O=$07 The Big Green One,$08 Vikki,$09 Plastro  
Cheat7_N=Here you can choose who you would like to play as. But do not use this with any other play-as option.
```

Make sure the `_O=` (Option) and `_N=` (Note) share the same cheat number.  
Also verify that the number of question marks `??` matches the number of values `$00`.

---

### Grouping Cheats

You may have noticed the `\` in the cheat name.  
This is used to group cheats together in the menu.

Example:
```text
Player1\Infinite Health  
Player1\Infinite Ammo
```

Grouped cheats appear with a **+** icon to expand.  
Useful for organizing player-specific or multiplayer options.

---

### ⚠️ Important Notice

Make sure that:

- The `_O=` (Option) and `_N=` (Note) share the same cheat number.
- The number of `??` matches the number of `$00` values.

---

### ✅ Supported Codes

**N64 CODE TYPES**

```text
80-XXXXXX 00YY — 8-Bit Constant Write  
81-XXXXXX YYYY — 16-Bit Constant Write  
50-00AABB CCCC — Serial Repeater  
88-XXXXXX 00YY — 8-Bit GS Button Write  
89-XXXXXX YYYY — 16-Bit GS Button Write  
D0-XXXXXX YYYY — 8-Bit If Equal To  
D1-XXXXXX YYYY — 16-Bit If Equal To  
D2-XXXXXX YYYY — 8-Bit If Not Equal To  
D3-XXXXXX YYYY — 16-Bit If Not Equal To  
A0-XXXXXX 00YY — 8-Bit Constant Write (Uncached)  
A1-XXXXXX YYYY — 16-Bit Constant Write (Uncached)  
F0-XXXXXX 00YY — 8-Bit Bootup Write Once (RDS Only)  
F1-XXXXXX YYYY — 16-Bit Bootup Write Once (RDS Only)
```

---

### ❌ Unsupported Codes

```text
CC-000000 0000 — Disable Expansion Pak  
DD-000000 0000 — Disable Expansion Pak  
EE-000000 0000 — Disable Expansion Pak  
DE-XXXXXX 0000 — Download & Execute  
FF-XXXXXX 0000 — Store Activated Cheat Codes
```

---

### Equalizer Compatibility

**Q: I saw a message on PAL Action Replay sites saying “Cannot be used with Equalizer.” What is an Equalizer? Can I still use these codes in MiB64?**

**A:** The Equalizer is a little sister of the Action Replay cheat device.  
It works the same way, and yes—you can use those codes in MiB64.

---

---

### Serial Repeater Example

```text
California Speed  
Cheat2="Have All\Cars",50001504 0000,800AAE5B 0001
```

The patch:
```text
50001504 0000,800AAE5B 0001
```
represents 21 codes, each changing by +4 hex in the last digit of the memory address. The second code is the starting point after the 50 patch.

---

### Understanding Hexadecimal

Hex counts go:
```
0–9, A–F, then 10–19, 1A–1F, and so on.
```

Decimal 0–255 = Hex 00–FF (8-bit)  
Decimal 256–65535 = Hex 100–FFFF (16-bit)  
So decimal 0–31 = Hex 00–1F

---

### Hexadecimal Reference Chart

**Numbers 0–255 (Dec) → 00–FF (Hex)**  
<a href="/cheats/assets/images/01/hex_1_0-255-1024x566.png" target="_blank">
  <img src="/cheats/assets/images/01/hex_1_0-255-1024x566.png" alt="Hex Chart 0–255" width="691" />
</a>

**Numbers 256–512 (Dec) → 100–200 (Hex)**  
<a href="/cheats/assets/images/01/hex_2_256-512-1024x566.png" target="_blank">
  <img src="/cheats/assets/images/01/hex_2_256-512-1024x566.png" alt="Hex Chart 256–512" width="691" />
</a>

And so on, up to:  
```text
Decimal: 65535  
Hex: FFFF
```

That should give you the idea of how the hex count works.

---

### Patch Construction

Start with:
```text
50000000 0000
```

Count: 21 codes  
→ Hex = `15`  
→ `50001500 0000`

Increment: +4  
→ `50001504 0000`

Final patch:
```text
50001504 0000,800AAE5B 0001
```

This compresses 21 codes into 2 lines.

---

### Code Progression Example

From:
```text
800AAE5B 0001
```
To:
```text
800AAEAB 0001
```

Full sequence:
```text
800AAE5B 0001  
800AAE5F 0001  
800AAE63 0001  
800AAE67 0001  
800AAE6B 0001  
800AAE6F 0001  
800AAE73 0001  
800AAE77 0001  
800AAE7B 0001  
800AAE7F 0001  
800AAE83 0001  
800AAE87 0001  
800AAE8B 0001  
800AAE8F 0001  
800AAE93 0001  
800AAE97 0001  
800AAE9B 0001  
800AAE9F 0001  
800AAEA3 0001  
800AAEA7 0001  
800AAEAB 0001
```

Each address increases by +4 hex.

---

You can also add a long line of patches that compress hundreds of codes into just a few lines.  
MiB64 supports up to 500 codes in one patch.

---

### ⚠️ A Question of Regions

As always, we really cannot stress this enough:  
**Do not try to add NTSC (U), (JU), (J) Gameshark cheat codes to PAL (E), (A), (F), (G), (I), (S) games—and vice versa.**  
Mixing regions will cause cheats to fail or crash the game.

---

<!-- ClauseEcho: Full Cheats FAQ Complete -->
<!-- ClauseLock: cheats-faq.md sealed -->
