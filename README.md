# On-The-Fly Renaming

The concept of OTF Renaming is simple: enable the user to rename specific items without the use of an anvil. 

## Usage

While holding an applicable item, sneak to rename it. This will replace the item with a temporary book and quill. The player should open it and write the desired name within the book. Then, upon signing, the previous item is returned with the name.

![Normal item](https://i.imgur.com/F0q6cEQ.png)
![Rename book](https://i.imgur.com/pPWQPX8.png)
![Book instruction message](https://i.imgur.com/B45cqHh.png)
![Name written on second page](https://i.imgur.com/Q4gNW7F.png)
![Titled whatever, then signed](https://i.imgur.com/nZ331jY.png)
![Item successfully renamed](https://i.imgur.com/cwuwGpZ.png)

Returns item upon failure:
![Item rename failed upon deselecting](https://i.imgur.com/6G1yZiz.png)

Supports stacks:
![Supports stack renaming](https://i.imgur.com/vH5yu3t.png)

By default, Paper (used to label [Warp Pads](https://github.com/SmoochyPit/Warp-Pads-Rewrite)) and Name Tags have this functionality enabled.

*Note: Unlike an anvil, this project does not limit the size or contents of user input. Keep this in mind when choosing to install.*

## Installation
### Step 1 - Download

(If you are on a Unix-based operating system, run `wget $(curl -s https://api.github.com/repos/SmoochyPit/Renameable-Items/releases/latest | grep 'browser_' | cut -d\" -f4)` in the datapacks folder of your world)

1. Click [releases](https://github.com/SmoochyPit/Renameable-Items/releases)
2. Find the latest release
3. Under assets, click "otf-renaming-1.X.X.zip" to download the archived data pack. *This file **should not** be unzipped before installation*
4. Select one of the following methods for installing the data pack:

### Step 2 - Data pack menu (New singleplayer worlds) (Very Easy)

1. In the Singleplayer menu, click "Create New World"
2. Click "Data Packs"
3. Drag the downloaded file onto your Minecraft window (toggle fullscreen with F11)
4. Click "Yes"
5. Hover over OTF Renaming in the menu and click the right arrow to add it to the list of selected data packs
6. Click "Done" and change any other world options you want
7. Click "Create New World"

### Step 2 - Manual installation (Existing singleplayer or multiplayer worlds) (Easy)

1. Place the downloaded file into the `[worldname]\datapacks` folder on your server or singleplayer world (located at `C:\Users\[user]\AppData\Roaming\.minecraft\saves\[worldname]\datapacks` by default in Windows and `~/.minecraft/saves/[worldname]/datapacks` on Linux).
2. Reload the world.

At this point, OTF Renaming will now be installed in your Minecraft world.

### Step 3 - Updating

1. Follow step 1 to download the latest release
2. Backup your world!! `World Select > Edit > Make Backup`
3. Delete the previous installation (Refer to step 2 for locating this file)
4. Follow step 2 to install the new data pack manually
5. Run `/reload` to check for any errors

### Support

Tested to support Minecraft: Java Edition 1.18.1-1.20.4.

### Uninstalling

To uninstall, run `/function itemname:uninstall`. Then disable or remove the data pack from the world.

### Configuration

I designed this pack to be easily customizable, but you'll still need to compile the pack yourself to make changes. Setting up and using Trident-Lang takes a few steps outlined below:

1. You'll need [git](https://git-scm.com/) and [Java](https://www.java.com/en/) installed.
    * The git installer on Windows asks many questions. The recommended settings will work fine.
2. Create a "workspace" folder for datapack-related files.
3. In this folder, open a terminal (right click -> git bash or command prompt)
4. Run `git clone https://github.com/energyxxer/Minecraft-Definitions`
5. Run `git clone https://github.com/energyxxer/Trident-Language`
6. Create a "datapacks" folder for data pack source code
7. In this folder, run `git clone https://github.com/SmoochyPit/Renameable-Items`

Now you have everything you need. Open the downloaded Renameable-Items folder and navigate to `datapack/data/itemname/functions/config.tdn`. Edit, add or removes values as you see fit. If a value is invalid, compilation will fail in the next step:

In the root of the "Renameable-Items" folder, run the command `java -jar ../../Trident-Language/Trident-Lang.jar .`. If it is successful, your configured .zip will be located in the "out" folder ready to be used.

### Resource Packs

Resource Packs can define a custom texture or model for the rename book by using the Custom Model Data value `0290100`.

Known Resource Packs implementing these textures (for default recipes) will be linked below if/when available:

* Stay tuned...

## Credits

Created with http://energyxxer.com/trident/. (https://github.com/Energyxxer/Trident-UI)
