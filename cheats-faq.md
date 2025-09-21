---
title: Cheats FAQ
layout: default
nav_order: 7
parent: MiB64 Cheats
description: Frequently asked questions about cheat codes in MiB64.
---

## ❓ <a name="cheats-faq">MiB64 Cheats FAQ</a> — Written By Gent

This should help you with any questions that you might have about adding & editing codes in the Cheat Database. Maximise this window if you are having trouble viewing it.

---

### 🧠 The Do's & Don'ts of Adding & Editing Cheat Codes

**Q: Why don't the cheats work in MiB64?**  
I ticked what I wanted to use but it does nothing on all games I have tried. What can I do to make them work?

**A:** Make sure you have enabled your Memory Pak—otherwise some cheats will not work!  
Go to **Options → Configure Controller Plugin** to check.

---

**Q: Why can't I see any cheats in the menu? It's blank.**

**A:** This could be several reasons:

- The game you're playing has no cheat support yet. You can add cheats manually or wait for support.
- Make sure `MiB64.cdb` is in the root folder (same as the MiB64 executable).
- Opening too many ROMs in one session may cause memory hang. Restart MiB64 and reload your game.
- You may need to manually add a cheat to populate the menu.

---

### 🧪 Manual Cheat Entry

So just enter this example below:

```text
Name: Test
Code: 80123456 0001
```

Once added, close MiB64.  
Open the `MiB64.cdb` file in a text editor (e.g. Notepad).  
Search for your game name:

In this case:  
```text
Name=Super Mario 64
```

If nothing shows, try without gaps or verify the correct region.

---

### 🧾 Region Codes

Example region identifiers:

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

### 🧠 Persistent Cheats

**Q: Is there a way to make MiB64 remember cheats I left on after closing?**

**A:** Yes. Go to:  
**Options → Settings → Options → Remember Selected Cheats**

Cheats left on will auto-enable next time you load the game.  
Turn off any you don’t want before closing MiB64.

---

### 🧠 Finding Cheat Codes

**Q: Where do I find cheat codes to add myself?**  
**A:** Google “N64 Action Replay cheats” for PAL and “N64 Gameshark cheats” for NTSC.

---

### 🧪 Adding Cheats

**Q: How do I add cheat codes in MiB64?**  
**A:** Click the [Adding Cheats](cheats.html#adding-cheats) link for full instructions.

Note: You do not need to add Enable or Keycodes.  
These are only for real console cheat devices—MiB64 does not require them.

---

### 🔍 Searching for Cheats

**Q: Can I search for my own cheat codes in MiB64?**  
**A:** Yes. MiB64 allows you to search, test results, and add them to the database via the GUI.  
See [Preparing for Cheat Search](cheats.html#preparing-to-search) for more info.

---

### ✏️ GUI vs Text Editor

**Q: Can I add, edit & delete cheat codes without opening the cheat file?**  
**A:** Yes. MiB64 lets you do all of this through the GUI.  
See: [Adding](cheats.html#adding-cheats), [Editing](cheats.html#editing-cheats), [Deleting](cheats.html#deleting-cheats), and [Using Cheats](cheats.html#using-cheats)

---

**Q: Can I edit codes in the MiB64.cdb file directly?**  
**A:** Yes, but you don’t need to. If you prefer, open the file in WordPad and search for the game name and region.

Example:  
```text
Name=Super Mario 64
```

Look at how the cheats are written:

```text
Cheat0="Ostrich Mario",8033B3BC 0090  
Cheat1="Mario Runs Backwards",8033B3BE 0070
```

Codes are separated by a space:  
`XXXXXXXX XXXX` — not `XXXXXXXXXXXX`

---

### 🧪 Modify Codes and Options

Example:

```text
Cheat5="Open Level Character Modifier",8125508A 00??  
Cheat5_O=$01 Easy Level,$02 Easy & Normal Level,$03  
Cheat7="Play As Options",811653D2 00??  
Cheat7_O=$07 The Big Green One,$08 Vikki,$09 Plastro  
Cheat7_N=Here you can choose who you would like to play as. But do not use this with any other play-as option.
```

Make sure the option (`_O`) and note (`_N`) share the same cheat number.  
Also verify that the number of question marks `??` matches the number of values `$00`.

---

### 🧷 Grouping Cheats

You may have noticed the `\` in the modify code example.  
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

### 🧠 Equalizer Compatibility

**Q: I saw a message on PAL Action Replay sites saying “Cannot be used with Equalizer.” What is an Equalizer? Can I still use these codes in MiB64?**

**A:** The Equalizer is a smaller version of the Action Replay device.  
It functions similarly, and yes—you can use those codes in MiB64.

---

### 🎮 Using Cheats

**Q: How do I use cheat codes in MiB64?**

**A:** For a full visual explanation, click the [Using Cheats](cheats.html#using-cheats) link.

---

### 🧪 Serial Repeaters

**Q: You mentioned Serial Repeaters (patch codes). How do they work?**

**A:** Codes starting with `50` are Serial Repeaters.  
They compress hundreds of codes into a smaller patch version.

Example:
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

### 🧠 Understanding Hexadecimal

Hex counts go:
```
0–9, A–F, then 10–19, 1A–1F, and so on.
```

Decimal 0–255 = Hex 00–FF (8-bit)  
Decimal 256–65535 = Hex 100–FFFF (16-bit)  
So decimal 0–31 = Hex 00–1F

---

### 📊 Hexadecimal Reference Chart

**Numbers 0–255 (Dec) → 00–FF (Hex)**  
<a href="/cheats/assets/images/01/hex_1_0-255-1024x566.png" target="_blank">
  <img src="/cheats/assets/images/01/hex_1_0-255-1024x566.png" alt="Hex Chart 0–255" width="691" />
</a>

**Numbers 256–512 (Dec) → 100–200 (Hex)**  
<a href="/cheats/assets/images/01/hex_2_256-512-1024x566.png" target="_blank">
  <img src="/cheats/assets/images/01/hex_2_256-512-1024x566.png" alt="Hex Chart 256–512" width="691" />
</a>
<!-- ClauseEcho: Hexadecimal Reference Charts -->

---

### 🧪 Building a Patch

The 50 patch code works like this:

- You tell the patch how many codes there are.
- You specify how much each code changes.
- It compresses a long list of codes into a serial repeater.

The memory address is the 3rd–5th hex pair.  
The value is the last 4 digits (9th–12th).  
The prefix `80` means 8-bit, so values max out at `FF` (decimal 255).

---

### 🧾 Code Progression Example

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

### 🧪 Patch Construction

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

You can patch up a long line of codes that might look like 10 entries but represent hundreds of changes.  
You could also have as much as 500 codes in one patch.

---

### ⚠️ A Question of Regions

As always, we really cannot stress this enough:  
**Do not try to add NTSC (U), (JU), (J) Gameshark cheat codes to PAL (E), (A), (F), (G), (I), (S) games—and vice versa.**  
Mixing regions will cause cheats to fail or crash the game.

---

<!-- ClauseLock: Cheats FAQ Section Echoed -->