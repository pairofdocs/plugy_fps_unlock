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

Install Plugy 14.01 from http://plugy.free.fr/en/index.html.
Copy PlugY.dll from this [release](https://github.com/pairofdocs/plugy_fps_unlock/releases/tag/v1.0.0) and place it into your `Diablo II/` folder.
