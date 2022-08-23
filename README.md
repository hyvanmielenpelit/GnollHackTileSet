# GnollHack Tile Set

This repository contains individual PNG files of the GnollHack tile set, from which you can build the sprite sheets using TileSetCompiler.

## Tile Map Build Instructions

1. Clone GnollHackTileSet repository to `C:\Repositories\hyvanmielenpelit\GnollHackTileSet`
2. Clone [TileSetCompiler](https://github.com/hyvanmielenpelit/TileSetCompiler) repository to `C:\Repositories\hyvanmielenpelit\TileSetCompiler`
3. Export **tile_definition.csv** from **GnollHack Windows executable** ([ASCII](https://github.com/hyvanmielenpelit/GnollHack/wiki/Build-Instructions-for-ASCII-Version-on-Windows) or [GUI](https://github.com/hyvanmielenpelit/GnollHack/wiki/Build-Instructions-for-Windows-GUI-Version-on-Windows)) in Wizard Mode using the **#wizsavetiledata** extended command. The file appears in the same directory as the executable. Copy it to the main directory of the GnollHackTileSet repository.
4. Open the [TileSetCompiler solution](https://github.com/hyvanmielenpelit/TileSetCompiler) with **Visual Studio 2022**.
5. Select the **TileSetCompiler** profile in the **green arrow drop down menu (Debug options)** in the menu bar. This determines that the program searches for assets in `C:\Repositories\hyvanmielenpelit\GnollHackTileSet`.
    - If you want to use another repository location for GnollHackTileSet, you can create your own launch profile in [launchSettings.json](https://github.com/hyvanmielenpelit/TileSetCompiler/blob/master/TileSetCompiler/Properties/launchSettings.json).
6. **Start Debugging** the TileSetCompiler project.
7. The tile map files will appear in the main directory of the GnollHackTileSet repository:
    - gnollhack_64x96_transparent_32bits.png
    - gnollhack_64x96_transparent_32bits-2.png
8. A log file will appear in the main directory of the GnollHackTileSet repository:
    - gnollhack_tilenames.txt

## Updating Repository

1. Open the GnollHackTileSet folder with **Visual Studio Code** *(File → Open Folder)*.
2. Copy new or updated files to the repository using  **File Explorer**.
3. Commit changes using **Visual Studio Code** and the **Source Control View**.
4. Push or sync changes to GitHub using **Visual Studio Code** and the **Source Control View**.
