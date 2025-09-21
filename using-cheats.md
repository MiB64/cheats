---
title: Using Cheats
layout: default
nav_order: 2
parent: MiB64 Cheats
description: Learn how to activate and manage cheat codes in MiB64.
---



## 🕹️ <a name="using-cheats">Using Cheats</a>

To use cheats in MiB64, follow these steps:

1. Open MiB64 and load your ROM.
2. Navigate to the Cheats menu.
3. Tick the cheats you want to enable.
4. Start your game and enjoy the effects.

<a href="./cheats/assets/images/01/Cheat11.png" target="_blank">
  <img src="./cheats/assets/images/01/Cheat11-300x259.png" alt="Cheat Menu" width="300" />
</a>
<p class="has-text-align-center"><strong>Click image to enlarge</strong></p>
<!-- ClauseEcho: Using Cheats Image -->

---

### 🧠 Notes

- Some cheats require a Memory Pak to function.  
  Go to **Options → Configure Controller Plugin** to ensure it's enabled.

- Cheats will only appear if the game is supported.  
  If the menu is blank, check the following:
  - Is `MiB64.cdb` in the root folder?
  - Have you opened too many ROMs in one session? Restart MiB64.
  - You may need to manually add cheats for unsupported games.

---

### 🧪 Example Manual Entry

```text
Name: Test
Code: 80123456 0001
```

After adding the cheat:
1. Close MiB64.
2. Open `MiB64.cdb` in a text editor.
3. Search for your game name (e.g. `Name=Super Mario 64`).
4. Copy the full cheat block and paste it below your test entry.

```text
[New-CRC-C:45]
Name=SUPER MARIO 64 (Region)
Cheat0="Test Cheat",80123456 0001
```

Delete the old entry, save the file, and restart MiB64.

---

### 🧷 Persistent Cheats

To make MiB64 remember cheats between sessions:

- Go to **Options → Settings → Options → Remember Selected Cheats**
- Cheats left on will auto-enable next time you load the game
- Turn off any you don’t want before closing MiB64

---

<!-- ClauseLock: Using Cheats Section Echoed -->
