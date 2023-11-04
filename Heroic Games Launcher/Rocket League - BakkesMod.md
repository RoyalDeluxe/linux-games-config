# Rocket League - BakkesMod

## Installation

1. Download [BakkesMod](https://bakkesmod.com/download.php)
2. Open Rocket League settings on Heroic Games Launcher
3. Enable Esync or Fsync
4. Click on "Run EXE on prefix"
5. Select "BakkesModSetup.exe"
6. Proceed through the installation setup
   1. Do not check for desktop shortcut
   2. Check Run BakkesMod
7. If proposed, update BakkesMod. Else go to File > Check for updates
8. If BakkesMod say it is out of date, there is two options :
    - uncheck safe mode in Settings > Enable save mode
    - create some folders in the Rocket League prefix like this :

      ```text
      [Path to your rocket league prefix]/drive_c/ProgramData/Epic/EpicGamesLauncher/Data/Manifests
      ```

      If after that, BakkesMod continue to be "out of date" then you need to get the content of the Manifests folder from an installed Epic Games Launcher (I took it from the EGL installed on my Windows partition)

## Launch Rocket League with BakkesMod

1. Launch Rocket League through Heroic Games Launcher
2. Once you're in the main menu, Do one of those action :
      - execute this command in a terminal :

        ```bash
        If Fsync is enable
        $ WINEFSYNC=1 WINEPREFIX=PATH/TO/ROCKET/LEAGUE/PREFIX/pfx /home/$USER/.steam/steam/steamapps/common/[PROTONVERSION]/dist/bin/wine c:/Program\ Files/BakkesMod/BakkesMod.exe

        If Esync is enable
        $ WINEESYNC=1 WINEPREFIX=PATH/TO/ROCKET/LEAGUE/PREFIX/pfx /home/$USER/.steam/steam/steamapps/common/[PROTONVERSION]/dist/bin/wine c:/Program\ Files/BakkesMod/BakkesMod.exe
        ```

      - Put one of the commands above in a script file. You need to execute the command in a termial so you need to use a specific syntaxe of your terminal. e.g. with gnome-terminal

        ```bash
        If Fsync is enable
        gnome-terminal -- sh -c 'WINEFSYNC=1 WINEPREFIX=~/games/Heroic/Prefixes/Rocket\ League/pfx /home/redflaam/.steam/steam/steamapps/common/Proton\ 8.0/dist/bin/wine c:/Program\ Files/BakkesMod/BakkesMod.exe'

        If Esync is enable
        gnome-terminal -- sh -c 'WINEESYNC=1 WINEPREFIX=~/games/Heroic/Prefixes/Rocket\ League/pfx /home/redflaam/.steam/steam/steamapps/common/Proton\ 8.0/dist/bin/wine c:/Program\ Files/BakkesMod/BakkesMod.exe'
        ```

3. BakkesMod will open and after some time the game should be injected

## Sources

[Source of inspiration](https://gist.github.com/Allavaz/23bb92ec4a69fa74f01088cb846b3029)

[Source for the "out of date" issue](https://www.reddit.com/r/bakkesmod/comments/s0njrh/how_to_bakkesmod_on_linux_steam_and_epic_games/)
