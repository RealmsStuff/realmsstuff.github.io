## 🛠 Choose Your Mod Type

### 1. Assembly Mod (`.dll`)

- **Filename:** `Assembly-CSharp.dll`
- **Description:** Replaces core game logic.

### 2. BepInEx Plugin (`.dll`)

- **Example:** `GunGame.dll`
- **Description:** Loaded via a modding framework (non-destructive).

### 3. Assets (`.assets`)

- **Example:** `sharedassets0.assets`
- **Description:** Modifies game textures, models, and UI.

---

## 📂 Installation Guides

### ⚙️ Installing Assembly Mod

**Step 1: Backup**
This process is destructive as you are replacing a core file. **If you skip this, you may lose your game.**

1. Go to the managed folder (path below).
2. Find `Assembly-CSharp.dll`.
3. Rename it to `Assembly-CSharp.dll.bak` or move it to your Desktop.

**Step 2: Install**
Drag your **modded** file into this location:
`Captivity v1.0.5b\Captivity_Data\Managed`

**Visual Folder Structure:**

- 📁 Captivity v1.0.5b
  - 📁 Captivity_Data
    - 📁 Managed
      - 📄 **Assembly-CSharp.dll** *(Place mod here)*

---

### 🧩 Installing BepInEx Plugin

**Step 1: Prerequisites**
You need the mod loader framework.

[BepInEx 5.x (x64)](https://github.com/BepInEx/BepInEx/releases)

1. Download BepInEx above.
2. Extract the zip into your main game folder (where `Captivity.exe` is).
3. **Run the game once** to create the necessary folders, then close it.

**Step 2: Place Mod**
Move your mod's `.dll` file into the plugins folder:
`Captivity v1.0.5b\BepInEx\plugins`

**Visual Folder Structure:**

- 📁 Captivity v1.0.5b
  - 📁 BepInEx
    - 📁 plugins
      - 📄 **YourMod.dll** *(Place mod here)*

---

### 🧊 Installing Assets

**Step 1: Backup**
Asset mods replace core game files containing textures and models. **Always backup the original file first.**

1. Go to the `Captivity_Data` folder.
2. Find `sharedassets0.assets` (or the specific asset file mentioned by the mod).
3. Rename it to `sharedassets0.assets.bak`.

**Step 2: Install**
Drag your **modded** `.assets` file into this location:
`Captivity v1.0.5b\Captivity_Data`

**Visual Folder Structure:**

- 📁 Captivity v1.0.5b
  - 📁 Captivity_Data
    - 📄 **sharedassets0.assets** *(Place mod here)*

---

## 🔧 Troubleshooting & FAQ

#### Q: Game crashes immediately upon launch

- **For Assembly/Asset Mods:** The version of the mod likely doesn't match your game version. Restore your backup files and try again.
- **For BepInEx:** You may have downloaded the x86 version instead of x64. Check that `winhttp.dll` is in the same folder as `Captivity.exe`.

#### Q: Mod loads, but nothing happens

Some BepInEx mods require the **API Plugin** dependency. Check the mod download page to see if you are missing a required file.

#### Q: How do I uninstall?

- **BepInEx:** Delete the specific `.dll` from the `plugins` folder.
- **Assembly/Assets:** Delete the modded file and rename your backup (e.g., `sharedassets0.assets.bak`) back to the original name.

---

## 🌐 Community

Still stuck? Join the community.

[**Join the Discord**](https://discord.gg/G7EN5exFnC)

*Not affiliated with Perveloper.*
