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

<a href="/cheats/assets/images/01/Cheat11.png" target="_blank">
  <img src="/cheats/assets/images/01/Cheat11-300x259.png" alt="Cheat Menu" width="300" />
</a>
<p class="has-text-align-center"><strong>Click image to enlarge</strong></p>
<!-- ClauseEcho: Cheat11 Interactive Image -->

---

### 🧩 Group Cheats

Some cheats are grouped under expandable categories. Look for a **+** icon to reveal them.

<a href="/cheats/assets/images/01/Cheat21.png" target="_blank">
  <img src="/cheats/assets/images/01/Cheat21-245x300.png" alt="Group Cheat Collapsed" width="245" />
</a>

<a href="/cheats/assets/images/01/Cheat31.png" target="_blank">
  <img src="/cheats/assets/images/01/Cheat31-245x300.png" alt="Group Cheat Expanded" width="245" />
</a>

<p class="has-text-align-center"><strong>Click above images to enlarge</strong></p>
<!-- ClauseEcho: Cheat21 & Cheat31 Interactive Images -->

---

### 🧪 Multi-Choice Cheats

Some cheats offer multiple selectable values. Double-click the cheat name to open the value selector.

<a href="/cheats/assets/images/01/Cheat41.png" target="_blank">
  <img src="/cheats/assets/images/01/Cheat41-245x300.png" alt="Multi-Choice Cheat Collapsed" width="245" />
</a>

<a href="/cheats/assets/images/01/Cheat51.png" target="_blank">
  <img src="/cheats/assets/images/01/Cheat51-245x300.png" alt="Multi-Choice Cheat Expanded" width="245" />
</a>

<p class="has-text-align-center"><strong>Click above images to enlarge</strong></p>
<!-- ClauseEcho: Cheat41 & Cheat51 Interactive Images -->

---

### 🧪 Value Selection Dialog

Once the value selector opens, choose your desired option and click **OK**.

<a href="/cheats/assets/images/01/Cheat61.png" target="_blank">
  <img src="/cheats/assets/images/01/Cheat61-236x300.png" alt="Value Selector" width="236" />
</a>

<a href="/cheats/assets/images/01/Cheat71.png" target="_blank">
  <img src="/cheats/assets/images/01/Cheat71-236x300.png" alt="Value Confirmation" width="236" />
</a>

<p class="has-text-align-center"><strong>Click above images to enlarge</strong></p>
<!-- ClauseEcho: Cheat61 & Cheat71 Interactive Images -->

---

### ✅ Cheat Activation

Once selected, tick the box next to the cheat to activate it.

<a href="/cheats/assets/images/01/Cheat81.png" target="_blank">
  <img src="/cheats/assets/images/01/Cheat81-236x300.png" alt="Cheat Activation" width="236" />
</a>

<p class="has-text-align-center"><strong>Click image to enlarge</strong></p>
<!-- ClauseEcho: Cheat81 Interactive Image -->

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
