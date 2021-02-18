# Original code
[PlugY v14](http://plugy.free.fr/en/index.html)

# Feature addition
FPS unlock / mouse fix feature from [BH 1.9.9](https://github.com/planqi/slashdiablo-maphack)

`Add option to remove FPS limit in single player` From BH [release notes](https://github.com/planqi/slashdiablo-maphack#release-notes-for-198)

# Method
Hex edit the running process D2client.dll

relevant BH [code](https://github.com/planqi/slashdiablo-maphack/blob/master/BH/Modules/Maphack/Maphack.cpp#L24):
```cpp
Patch* fpsPatch = new Patch(NOP, D2CLIENT, { 0x44E51, 0x45EA1 }, 0, 8);
```
