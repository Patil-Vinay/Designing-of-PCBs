# 5V Voltage Regulator

Single sided board that turns 12V AC from a step down transformer into a regulated 5V DC.
The AC goes into a GBU406 bridge rectifier, gets smoothed by C2 (47uF) and C1 (10uF) and is then
regulated by a 78L05 (SOT-89). C3 sits on the 5V output. Board size is about 26.9 x 29.2 mm.

`Circuit Diagram.png` is the reference circuit I based the board on. My own schematic is
`Schematic_voltage_regulator.png`.

## Connections

- H1 - 12V AC input from the transformer
- H2 - 5V output, pin 1 = 5V, pin 2 = GND

## Parts

| Ref | Part |
| --- | --- |
| D1 | GBU406 bridge rectifier |
| C1 | 10uF electrolytic |
| C2 | 47uF electrolytic |
| C3 | 0.1uF |
| U1 | 78L05 regulator, SOT-89 (CJ78L05) |
| H1, H2 | 2 pin female header |

Full list with LCSC part numbers is in `BOM_PCB_voltage_regulator.csv`.

## Files

- `voltage_regulator.json` - EasyEDA schematic
- `PCB_voltage_regulator.json` - EasyEDA PCB layout
- `Schematic_voltage_regulator.png` - schematic export
- `PCB_PCB_voltage_regulator*.png` - PCB, 2D and 3D views

## Notes

- The 78L05 is only good for about 100 mA so this is meant for small loads.
- 12V AC rectified comes out at around 16-17V with no load. The BOM has 16V parts for C1 and C2
  which is cutting it too close. Use 25V capacitors when building it.
