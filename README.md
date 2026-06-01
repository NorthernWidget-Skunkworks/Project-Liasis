[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.20171210.svg)](https://doi.org/10.5281/zenodo.20171210)

# Project-Liasis

A small-scale, low-cost longwave pyrgeometer for measuring terrestrial thermal infrared (longwave) radiation. It uses a ZTP-135SR thermopile sensor (~8–14 µm) and is designed for deployment in environmental monitoring networks.

Named after *Liasis*, a genus of Australian pythons that sense thermal infrared through labial pit organs.

## Millable components

* [Pipe mount](https://easel.inventables.com/projects/cAirZefIUws53oghGYYopw) — accepts 1.25"–3.25" ID U-bolts (¼" bolt diameter); typical US sizes 1.25", 1.5", 1.75", 2"
* [Drilling jig](https://easel.inventables.com/projects/s-fOn9DWTmkeizO0vO8MGw) for Liasis enclosure

## NW-Device-Specification — Schema 1, Page 0

Implements [NW-Device-Specification](https://github.com/NorthernWidget/NW-Device-Specification) Schema 1. The 32-byte identity block (Page 0) is stored at the top of EEPROM:

```
Block 0:  Schema=0x01, Name='L','i','a','s','i','s',0x00
Block 1:  HW major=[mfr], HW minor=[mfr], FW patch=[mfr], 0x00,0x00,0x00, Reserved
Block 2:  Board type=0x6C01 ('l'=0x6C, rev 1), Group ID=[mfr], Unique ID=[mfr], FirmwareID=0x0000
Block 3:  Reserved, Magic=0x00, CRC=[computed], I2C address=TBD
```

Note: `0x6C00` is reserved (legacy Apis). Legacy deployed units carry board types `0x2400`/`0x2401` (formerly Dyson LW, Monarch LW).

## License

Hardware designs are licensed under the [Creative Commons Attribution-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-sa/4.0/).

<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a>

Software (where present) is licensed under the [GNU General Public License v3](LICENSE_for_code).
