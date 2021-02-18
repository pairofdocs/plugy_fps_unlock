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

## FPS Unlock Would Work for D2 v1.13c or 1.13d Only

The offsets that are present in BH are for v1.13c and v1.13d.
Offsets for v1.14 are required for this to work with v1.14.

```cpp
struct Offsets {
	int _113c;
	int _113d;
};
```

When a new Patch is created only the 1.13c and 1.13d offsets `{ 0x44E51, 0x45EA1 }` are provided:
```cpp
Patch* fpsPatch = new Patch(NOP, D2CLIENT, { 0x44E51, 0x45EA1 }, 0, 8);
```
