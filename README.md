# QC:Doom Edition Flatpak release

A gameplay mod bringing Quake Champions weapons and many different player classes (Champions) each with unique abilities, passive and actives, to be used in single player or multiplayer; along with monsters from Quake 1, Quake 2 and Quake 4, and Doom 2016 for you to chose what theme of monsters you want, or even mix them up.  
The mod was designed from the ground up to be played in single player, cooperative, and many types of PvP, like Deathmatch (Free for all), Team Deathmach, Duel, Capture the Flag, Last Man Standing, "Clan Arena".  
See the [QCDE Manual](https://qcde.net/files/public/QCDE_Manual.pdf) for more information.

## Installation

This Flatpak release of QC:DE combines Q-Zandronum, Doomseeker and the mod itself into a complete, pre-configured package for easy installation on Linux systems.

### Game data

* Pre-installed game data can be found under:
  * IWADs: `/app/share/games/doom` 
  * QCDE: `/app/share/games/qcde`
  * Location of `/app/` can be queried with the following command: `flatpak info --show-location net.qcde.QCDE`

* The default download location of Doomseeker is:
  * `~/.var/app/net.qcde.QCDE/data/doomseeker`

* Place your IWADs and other files to:
  * `~/.var/app/net.qcde.QCDE/.config/zandronum/` or
  * `~/.var/app/net.qcde.QCDE/data/doomseeker`
* Optionally, edit the Q-Zandronum settings file to load files additional directories:
  * `~/.var/app/net.qcde.QCDE/.config/zandronum/zandronum.ini`
  * Add new paths under the `[IWADSearch.Directories]` and `[FileSearch.Directories]` sections, **don't edit the default entries**.
  * Make sure to also add any new search paths to Doomseeker as well under `Settings -> File Paths`, otherwise the server browser will not see them.

## Run with custom wads

### UI
With Doomseeker, you can create a custom game. Then, under mode you can sellect 'Play offline' to start a singleplayer game.  
An example Deathmatch game is pre-configured out of the box.

### CLI
You can also start a custom game using the command line. If your files are located in the directories mentioned above, you can refer to them by just their filenames.  
For example, to run Plutonia II with QCDE and its OST, the command would be the following:

```
flatpak run --command="q-zandronum" net.qcde.QCDE -file PL2.WAD QCDEv3.1_beta_3.pk3 QCDEmus3.0.pk3
```

For more info, see:

* https://wiki.zandronum.com/Command_Line_Parameters

Additionally:

* https://zdoom.org/wiki/Command_line_parameters
* https://zdoom.org/wiki/Installation_and_execution_of_ZDoom

## Accessing files on unconventional spots ##
If you want to access wads in different locations, you might have to adjust the [Flatpak sandboxing permissions](http://docs.flatpak.org/en/latest/sandbox-permissions.html). You can easily do that like this:

```
flatpak override net.qcde.QCDE --filesystem=/OTHER/LOCATION/WITH/WADS --user
```
 
# Credits
This repository is based on the Flatpak release of Q-Zandronum [com.qzandronum.Q-Zandronum](https://github.com/flathub/com.qzandronum.Q-Zandronum), which in turn, was forked from [com.zandronum.Zandronum](https://github.com/flathub/com.zandronum.Zandronum).  
Credits go to every contributor of these repositories.

