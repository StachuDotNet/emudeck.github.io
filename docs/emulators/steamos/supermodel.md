# Supermodel is a Sega Model 3 Emulator.

!!! warning

    Supermodel does not have a GUI. If you try to launch Supermodel from its shortcut in either Desktop Mode or Game Mode, it will not launch. In order to launch and configure Supermodel, you will need to do so from the command line. To see a list of commands, in Desktop Mode, open a terminal, and enter: <br>
    `flatpak run com.supermodel3.Supermodel --help`

Website: [https://www.supermodel3.com/](https://www.supermodel3.com/)

GitHub: [https://github.com/trzy/Supermodel](https://github.com/trzy/Supermodel)

***

## Supermodel Table of Contents

1. [Getting Started with Supermodel](#getting-started-with-supermodel)
    - [Configuration](#supermodel-configuration)
    - [Supermodel Folder Locations](#supermodel-folder-locations)
    - [How to Update Supermodel](#how-to-update-supermodel)
    - [How to Launch Supermodel in Desktop Mode](#how-to-launch-supermodel-in-desktop-mode)
    - [How Supermodel ROMs Work](#how-supermodel-roms-work)
    - [Widescreen Hacks](#widescreen-hacks)
    - [File Formats](#supermodel-file-formats)
    - [Hotkeys](#supermodel-hotkeys) 
        - [Steam Deck Light Gun Controls](#steam-deck-light-gun-controls)
2. [Supermodel Tips and Tricks](#supermodel-tips-and-tricks)
    - [Which ROM Set Does Supermodel Use?](#which-rom-set-does-supermodel-use)
    - [How to Configure Light Gun Games](#how-to-configure-light-gun-games)

***

## Getting Started with Supermodel
[Back to the Top](#supermodel-table-of-contents)

Supermodel is a fairly straight-forward emulator to set up. Place your ROMs in `Emulation/roms/model3`. Read the [Configuration](#supermodel-configuration) section to learn more about Supermodel and its folder locations.

To launch your ROMs in game mode, use Steam ROM Manager and use one of the following parsers to play your Supermodel ROMs:

* `EmulationStation-DE`
* `Sega Model 3 - Supermodel`
* `Emulators`


***

### Supermodel Configuration
[Back to the Top](#supermodel-table-of-contents)

* Type of Emulator: Flatpak
* Config Location: `$HOME/.supermodel`
* ROM Location: `Emulation/roms/model3`
* Saves: N/A

**Note:** `~/.supermodel` is a hidden folder by default. In Dolphin (file manager), click the hamburger menu in the top right, click `Show Hidden Files` to see these folders.

***

### Supermodel Folder Locations
[Back to the Top](#supermodel-table-of-contents)

These file locations apply regardless of where you chose to install EmuDeck (to your internal SSD, to your SD Card, or elsewhere). Some emulator configuration files will be located on the internal SSD as listed below. 

`$HOME` refers to your home folder. If you are on a Steam Deck, this folder will be named `/home/deck` (you will likely not see `deck` in the file path when navigating using the file manager). 

Paths beginning with `Emulation/..` correspond to your EmuDeck install location. If you installed on an SD Card, your path may be `/run/media/mmcblk0p1/Emulation/roms/..`. If you installed on your internal SSD, your path may be `/home/deck/Emulation/roms/..`

**Note:** Folders with a `.` (`.var`, `.local`, `.config`, etc.) at the beginning are hidden by default. In Dolphin (file manager), click the hamburger menu in the top right, click `Show Hidden Files` to see these folders.

`$HOME/.supermodel`

```
.supermodel/
├── Analysis
├── Assets
│   ├── DIR.txt
│   ├── p1crosshair.bmp
│   └── p2crosshair.bmp
├── Config
│   ├── Games.xml
│   └── Supermodel.ini
├── Log
└── NVRAM
    ├── dayto2pe.nv
    ├── daytona2.nv
    ├── dirtdvls.nv
    ├── eca.nv
    ├── fvipers2.nv
    ├── getbassur.nv
    ├── harley.nv
    ├── lamachin.nv
    ├── lemans24.nv
    ├── lostwsga (Calibrated for 4x3 resolutions).nv
    ├── lostwsga.nv
    ├── magtruck.nv
    ├── mgtrkbad.nv
    ├── oceanhuna.nv
    ├── oceanhun.nv
    ├── scud.nv
    ├── scudplus.nv
    ├── skichamp.nv
    ├── spikeofe.nv
    ├── spikeout.nv
    ├── srally2dx.nv
    ├── srally2.nv
    ├── swtrilgy.nv
    ├── vf3.nv
    ├── vf3tb.nv
    ├── von2.nv
    ├── vs298.nv
    ├── vs2.nv
    └── vs2v991.nv
```


***

### How to Update Supermodel
[Back to the Top](#supermodel-table-of-contents)

* Update through `Discover` (Shopping bag icon)
* Through the `Update your Emulators & Tools` section on the `Manage Emulators` page in the `EmuDeck` application


***

### How to Launch Supermodel in Desktop Mode

!!! info

    Supermodel does not have a GUI. In order to launch and configure Supermodel, you will need to do so from the command line. 

* In Konsole, run `flatpak run com.supermodel3.Supermodel`
    * If you want to see a list of commands, run:
        * `flatpak run com.supermodel3.Supermodel --help`
* In `Emulation/tools/launchers`, right click anywhere, click `Open Terminal Here`, type `./supermodel.sh`
    * If you want to see a list of commands, run:
        * `./supermodel.sh --help`

***

### How Supermodel ROMs Work
[Back to the Top](#supermodel-table-of-contents)

Supermodel follows MAME ROM sets to keep its games up to date. MAME ROM sets are typically three digits and match the latest MAME version. As of March 11th, 2024, MAME is on version 0.263 meaning that the latest ROM set is 0.263. 

In order to use Supermodel, you will need a non-merged ROM set, typically the most recent ROM set will do the trick. But as of March 11th, 2024, ROM sets from between approximately 0.235 and 0.263 should also ideally work for Supermodel.

For Supermodel specifically, you will need a **non-merged** ROM set. **Merged** ROM sets will **not** work. 

To summarize: 

As of March 11th, 2024, the latest **non-merged** ROM set is 0.263. To use Supermodel, ideally use the latest **non-merged** (0.263) and keep your ROMs zipped. Unzipping your ROMs will **not** work for Supermodel. 

For more information, see the [Maintaining ROM Versions](../../emulators/steamos/mame.md#maintaining-rom-versions) on the MAME emulator page. 

***

### Widescreen Hacks
[Back to the Top](#supermodel-table-of-contents)

When possible, widescreen hacks are automatically applied. However, for some games, widescreen causes severe visual glitches and are disabled for the respective game. 

**Applied**

* daytona2
* dayto2pe
* dirtdvls
* getbassur
* eca
* fvipers2
* lemans24
* mgtrkbad
* scud
* scudplus
* srally2
* srally2dx
* swtrilgy
* vf3
* vf3tb
* von2

**Disabled**

* lamachin
* lostwsga
* magtruck
* oceanhun
* oceanhuna
* skichamp
* spikeofe
* spikeout
* vs2
* vs298
* vs2v991

***

### Supermodel File Formats
[Back to the Top](#supermodel-table-of-contents)

* .zip

***

### Supermodel Hotkeys
[Back to the Top](#supermodel-table-of-contents)

{{ read_csv('supermodel-hotkeys.csv') }}

#### Steam Deck Light Gun Controls

Supermodel also comes with a `EmuDeck - Steam Deck Light Gun Controls` profile intended to be used with light gun games. To use this profile, apply it manually. For instructions, see [How to Select a Steam Input Profile](../../controls-and-hotkeys/steamos/hotkeys.md#how-to-select-a-steam-input-profile).

{{ read_csv('emudeck-steam-deck-light-gun-controls.csv') }}

***

## Supermodel Tips and Tricks
[Back to the Top](#supermodel-table-of-contents)

***

### Which ROM Set Does Supermodel Use?
[Back to the Top](#supermodel-table-of-contents)

Supermodel uses a non-merged (ideally the latest) ROM set.

See [How Supermodel ROMs Work](#how-supermodel-roms-work) for more information.

***

### How to Configure Light Gun Games
[Back to the Top](#supermodel-table-of-contents)

1. In Game Mode, single click the game you would like to change the Steam Input Profile for, and click the `Controller Icon` on the right of the screen. Click the layout (whichever name it is currently set to) at the top
2. Click the `Templates` tab
3. Select the `EmuDeck - Steam Deck Light Gun Controls` profile
4. Light gun controls will now be configured for this game

{{ read_csv('emudeck-steam-deck-light-gun-controls.csv') }}

***