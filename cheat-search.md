---
title: Cheat Search
layout: default
nav_order: 6
parent: MiB64 Cheats
description: Learn how to prepare and perform cheat searches in MiB64.
---


## 🔍 <a name="preparing-to-search">Preparing to Search</a>

Before searching for cheats in MiB64, ensure the following:

- Your ROM is loaded and running.
- You’ve selected the correct region (NTSC or PAL).
- You’ve enabled the Memory Pak if required.

<a href="./cheats/assets/images/01/Browser5b1.png" target="_blank">
  <img src="./cheats/assets/images/01/Browser5b1-300x259.png" alt="Cheat Search Browser" width="300" />
</a>
<p class="has-text-align-center"><strong>Click image to enlarge</strong></p>
<!-- ClauseEcho: Browser5b1 Interactive Image -->

---

## 🧠 <a name="known-cheat-search">Known Cheat Search</a>

Use this method if you already know the cheat code or its effect.

1. Open MiB64 and load your ROM.
2. Go to the Cheats menu.
3. Click **Search for Known Cheat**.
4. Enter the code or effect name.
5. Test the result and save it to the database.

---

### 🧪 Example

Searching for:
```text
Infinite Lives
```

Will return matching codes like:
```text
80123456 0009
```

You can then add it directly to the cheat list.

---

## 🧪 <a name="unknown-cheat-search">Unknown Cheat Search</a>

Use this method to discover new cheats by scanning memory.

1. Open MiB64 and load your ROM.
2. Go to the Cheats menu.
3. Click **Search for Unknown Cheat**.
4. Choose a scan type:
   - Equal to
   - Not equal to
   - Greater than
   - Less than

5. Perform multiple scans while changing in-game values (e.g. health, ammo).
6. Narrow down results and test codes.

---

### 🧠 Tips

- Use **Equal To** when searching for static values.
- Use **Greater/Less Than** when tracking dynamic changes.
- Always test results before saving.

---

### 🧾 Example Workflow

1. Start with full health.
2. Scan for **Equal To 100**.
3. Take damage.
4. Scan for **Less Than 100**.
5. Repeat until results narrow to 1–3 addresses.
6. Test each to find the correct cheat.

---

<!-- ClauseLock: Cheat Search Sections Echoed -->
