# In-Game Texture Replacement Guide

## Notes
1. This guide only illustrates one of many approaches for replacing in-game textures for Captivity. The approach shown here isn't the only one.
2. This guide may also be helpful for replacing in-game assets other than textures (e.g. sounds), but no direct instructions are shown for replacing assets other than textures.
3. The procedures in this guide only apply to Windows & Linux as the tool used in this guide only runs natively on Windows & Linux, not macOS (Sorry \:p)


---

## Steps

### Part 1: Setup

1. Download the latest release of UABEA (Unity Asset Bundle Extractor Avalonia) from its [official repository](https://github.com/nesrak1/UABEA/releases). The eighth release was used and tested when this guide was written. Make sure to choose the correct file for download (it should be within the Assets tab, uabea-windows.zip for Windows, uabea-ubuntu.zip for Linux) (For Linux users only: despite the name uabea-ubuntu.zip, it works for Linux distros other than Ubuntu as well, like Arch Linux)

2. Unzip the downloaded instance of UABEA. UABEA can be run through UABEAvalonia.exe on Windows or UABEAvalonia on Linux.

3. Download a tool for editing 2D sprites. Examples include Microsoft Paint, Gimp, Pinta. Pinta was used and tested when this guide was written. (Skip this step if such a tool is already installed on your device)

### Part 2: Locate and Extract the Texture

4. Make backup(s) of the game assets file `Captivity_Data/sharedassets0.assets`.

5. Open UABEA, then select the game asset file through menu options `File -> Open`. (Note: `sharedassets0.assets.resS` found in the `Captivity_Data` directory must be located within the same directory as `sharedassets0.assets` in order for in-game textures to be extracted without error) If the game asset file is opened correctly, a table of assets should appear with the columns "Name, Container, Type, File ID, Path ID, Size, Modified".

6. Locate the texture to be modified within the table of assets. The table includes a variety of different types of assets, like Sprite, AudioClip, AnimationClip. Texture assets have the type `Texture2D`. Clicking on the `Name` column of the assets table would have the assets sorted alphabetically by name, which could make the search for texture file more convenient.

7. Search for your target texture. Use the keyboard shortcut `Ctrl + F` to search up the texture by name, or access it through the menu options `View -> Search by name`. When the texture name is unknown, make guesses. Texture names don't contain spaces. Keep search terms brief, try synonyms if no result is found, use wildcards. Take the texture `HairBrownPonyTail` for example, using wildcards (the wildcard is "\*" in this case) would make it easier to find it. Searching by "hair" wouldn't show the result, searching by "hair\*" or "\*hair\*" would show the result, however. Keeping the search term brief would help too. "\*hair\*" would show the result, while "\*brownhair\*" wouldn't. Using synonyms also helps. "\*brunette\*" or "\*chestnut\*" wouldn't show the result while "\*brown\*" would. When searching by name, if the case sensitive option is enabled, search results would be narrowed. Toggle the case sensitive option if needed. Searching by name only starts at the currently selected texture (a texture is selected when it's clicked in the table and highlighted), and skips any textures against the search direction (the search direction could be up or down the table depending on the direction option).

8. Export the texture. When the desired texture is found, select the texture by clicking on it. It should be highlighted after selection. Then use the menu options `Plugins -> Export texture` (Plugins is found in the right panel) to export the texture as a PNG file.

### Part 3: Modify and Reimport

9. Modify the texture with the sprite editor (e.g. Microsoft Paint, Gimp, Pinta). It's recommended to make a backup of the texture file (png file) before modification in case it's needed to revert modifications made to the texture.

10. Import the texture. Select the desired texture in the assets table in UABEA, use the menu options `Plugins -> Edit texture -> Load` (Load is found at the bottom of the window, besides the text `Texture`), then choose the modified texture file (png file). After that, select `Save` to save the texture modification. (This will not save the assets file however)

11. Save the assets file. This can be done with "Save" (accessible through menu options `File -> Save` or keyboard shortcut `Ctrl + S`) or "Save As..." (accessible through menu options `File -> Save as...` or keyboard shortcut `Ctrl + Shift + S`).

The resulting assets file (sharedassets0.assets) should contain the modified texture. Congratulations on updating the textures!

P.S. Consider sharing your changes with others in the server \:p
