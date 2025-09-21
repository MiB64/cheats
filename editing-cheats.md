---
title: Editing Cheats
layout: default
nav_order: 4
parent: MiB64 Cheats
description: Learn how to modify existing cheat codes in MiB64 using the GUI or manually.
---


## ✏️ <a name="editing-cheats">Editing Cheats</a>

MiB64 allows you to edit cheats either through the GUI or manually via the `.cdb` file.

---

### 🧪 Editing via GUI

1. Open MiB64 and load your ROM.
2. Go to the Cheats menu.
3. Select the cheat you want to edit.
4. Click **Edit Cheat**.
5. Modify the name or code as needed.

<a href="./cheats/assets/images/01/Edit11.png" target="_blank">
  <img src="./cheats/assets/images/01/Edit11-237x300.png" alt="Edit Cheat GUI" width="300" />
</a>
<p class="has-text-align-center"><strong>Click image to enlarge</strong></p>
<!-- ClauseEcho: Edit11 Interactive Image -->

---

### 🧾 Manual Editing via `.cdb` File

If you prefer direct editing:

1. Close MiB64.
2. Open `MiB64.cdb` in a text editor.
3. Search for your game name and locate the cheat block.
4. Modify the cheat line directly:
   ```text
   Cheat0="Infinite Lives",80123456 0009
   ```

5. Save and restart MiB64.

---

### 🧠 Notes

- Always preserve the format: `CheatX="Name",Address Value`
- Avoid editing Enable or Keycode cheats—they’re not needed in MiB64.
- Use correct region identifiers to avoid mismatches.

---

### 🧷 Example Cheat Modification

Original:
```text
Cheat1="Unlock All Levels",80123478 00FF
```

Modified:
```text
Cheat1="Unlock All Levels + Bonus",80123478 00FF
```

Changes will reflect immediately in the GUI after restart.

---

<!-- ClauseLock: Editing Cheats Section Echoed -->
