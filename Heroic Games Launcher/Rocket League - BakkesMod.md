# Rocket League - BakkesMod

1. Download [BakkesMod](https://bakkesmod.com/download.php)
2. Open Rocket League settings on Heroic Games Launcher
3. Enable Esync or Fsync
4. Click on "Run EXE on prefix"
5. Select "BakkesModSetup.exe"
6. Proceed through the installation setup
   1. Do not check for desktop shortcut
   2. Check Run BakkesMod
7. If proposed, update BakkesMod. Else go to File > Check for updates
8. Close BakkesMod
9. Open Rocket League through Heroic Games Launcher
10. Once Rocket League is launched, open a terminal and execute this command :

    ```bash
    If Fsync is enable
    $ WINEFSYNC=1 WINEPREFIX=PATH/TO/ROCKET/LEAGUE/PREFIX/pfx /home/$USER/.steam/steam/steamapps/common/[PROTONVERSION]/dist/bin/wine c:/Program\ Files/BakkesMod/BakkesMod.exe

    If Esync is enable
    $ WINEESYNC=1 WINEPREFIX=PATH/TO/ROCKET/LEAGUE/PREFIX/pfx /home/$USER/.steam/steam/steamapps/common/[PROTONVERSION]/dist/bin/wine c:/Program\ Files/BakkesMod/BakkesMod.exe
    ```

11. If BakkesMod say it is out of date, uncheck safe mode in Settings > Enable save mode
12. After some time, BakkesMod should inject in Rocket League

[Source](https://gist.github.com/Allavaz/23bb92ec4a69fa74f01088cb846b3029)
