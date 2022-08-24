# GnollHack Tile Set

This repository contains individual PNG files of the GnollHack tile set, from which you can build the sprite sheets using TileSetCompiler.

## Tile Map Build Instructions

These build instructions are for Windows. You need  [Visual Studio 2022](https://visualstudio.microsoft.com/vs/) to follow these instructions.

1. Clone GnollHackTileSet repository to `C:\Repositories\hyvanmielenpelit\GnollHackTileSet`
2. Clone [TileSetCompiler](https://github.com/hyvanmielenpelit/TileSetCompiler) repository to `C:\Repositories\hyvanmielenpelit\TileSetCompiler`
3. Build the ASCII Version of [GnollHack](https://github.com/hyvanmielenpelit/GnollHack) for Windows.
    - [ASCII Version Build Instructions](https://github.com/hyvanmielenpelit/GnollHack/wiki/Build-Instructions-for-ASCII-Version-on-Windows)
4. Create **tile_definition.csv**:
    1. Start the **GnollHack Windows executable**  in Wizard Mode by using `-D -u wizard` command line parameters. *(You can create a shortcut for this.)*
    2. Use the **#wizsavetiledata** extended command within the game.
    3. **tile_definition.csv** file appears in the same directory as the executable.
    4. Copy the file to the main directory of the GnollHackTileSet repository.
5. Open the [TileSetCompiler solution](https://github.com/hyvanmielenpelit/TileSetCompiler) with **Visual Studio 2022**.
6. Select the **TileSetCompiler** profile in the **green arrow drop down menu (Debug options)** in the menu bar. This determines that the program searches for assets in `C:\Repositories\hyvanmielenpelit\GnollHackTileSet`.
    - If you want to use another repository location for GnollHackTileSet, you can create your own launch profile in [launchSettings.json](https://github.com/hyvanmielenpelit/TileSetCompiler/blob/master/TileSetCompiler/Properties/launchSettings.json).
7. **Start Debugging** the TileSetCompiler project.
8. The **tile map files** will appear in the main directory of the GnollHackTileSet repository:
    - gnollhack_64x96_transparent_32bits.png
    - gnollhack_64x96_transparent_32bits-2.png
9. A **log file** will appear in the main directory of the GnollHackTileSet repository:
    - gnollhack_tilenames.txt

## Updating Repository

Updating the repository is done using [Visual Studio Code](https://code.visualstudio.com/).

1. Open the GnollHackTileSet folder with **Visual Studio Code** *(File → Open Folder)*.
2. Copy new or updated files to the repository using  **File Explorer**.
3. Commit changes using **Visual Studio Code** and the **Source Control View**.
4. Push or sync changes to GitHub using **Visual Studio Code** and the **Source Control View**.
