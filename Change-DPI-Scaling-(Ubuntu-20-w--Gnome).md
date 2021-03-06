# Ubuntu + Gnome Scaling
There is a fairly simple way to scale applications on Ubuntu 20 with Gnome

In these examples, RuneLite.AppImage is present in `/usr/local/bin` and has executable permissions (`chmod +x`)


# CLI Solution
There is a fairly simple way to run RuneLite individually scaled on hidpi screens

```
GDK_SCALE=2 GDK_DPI_SCALE=0.5 /usr/local/bin/RuneLite.AppImage
```


# .desktop Application solution

```
[Desktop Entry]
Name=RuneLite
Exec=env GDK_SCALE=2 GDK_DPI_SCALE=0.5 "/usr/local/bin/RuneLite.AppImage"
TryExec=/usr/local/bin/RuneLite.AppImage
StartupNotify=true
Terminal=false
Type=Application
Icon=/path/to/some/icon/i/made/runelite.svg
Comment=RuneLite ubuntu 20 with gnome scaled launcher
Categories=X-Runescape;Game;X-Scaled;X-GDK;RolePlaying;AdventureGame;
GenericName=RuneLite

```
# Screenshot

![](https://i.imgur.com/IdT1pKD.png)


# Known Issues

* GPU
    * AntiAliasing of any setting while scaled breaks graphics as of this writing