https://travis-ci.com/pairofdocs/plugy_fps_unlock.svg?branch=master

# Original Code
[PlugY v14](http://plugy.free.fr/en/index.html)

# Feature Addition
FPS unlock / mouse fix feature from [BH 1.9.9](https://github.com/planqi/slashdiablo-maphack)

`Add option to remove FPS limit in single player` From BH [release notes](https://github.com/planqi/slashdiablo-maphack#release-notes-for-198)

# Method
Hex edit the running process D2client.dll

relevant BH [code](https://github.com/planqi/slashdiablo-maphack/blob/master/BH/Modules/Maphack/Maphack.cpp#L24):
```cpp
Patch* fpsPatch = new Patch(NOP, D2CLIENT, { 0x44E51, 0x45EA1 }, 0, 8);
```

# Notes

## FPS Unlock Works for D2 v1.13c and 1.13d Only

The offsets that are present in BH are for v1.13c and v1.13d.
BH has not yet added this feature for v1.14+.


# Install

Install Plugy v14.02 from http://plugy.free.fr/en/index.html.
Copy PlugY.dll from this [release](https://github.com/pairofdocs/plugy_fps_unlock/releases/tag/v1.0.1) and place it into your `Diablo II/` folder.

If you already have older versions of Plugy v14.01 or v11.02, use the respective Plugy.dll from this [release](https://github.com/pairofdocs/plugy_fps_unlock/releases/tag/v1.0.0).

# Credits and Discussion
A D2Mods.info / Phrozen Keep thread about this feature and implementations is [here](https://d2mods.info/forum/viewtopic.php?f=8&t=65239&p=501210#p501210).
Credit goes out to devurandom, Necrolis, fearedbliss.

@fearedbliss also implemented this FPS unlock feature for [Cactus](https://github.com/fearedbliss/Cactus).
See the [notes](https://github.com/fearedbliss/Cactus/blob/master/README-SINGLING.md#notes).
