# Dual 12V Power Supply

Double sided board that gives +12V and -12V from a 15-0-15 center tapped transformer. The two
outer taps go to a GBU406 bridge rectifier and the center tap is ground. C1 and C2 (1000uF) smooth
the positive and negative rails, a 7812 regulates the +12V side and a 7912 the -12V side.
C3, C4 (10uF) and C5, C6 (1uF) are on the outputs. Board size is about 61.5 x 43.9 mm.

`Circuit Diagram.png` is the reference circuit I followed (from circuitspedia.com). My own schematic is
`Schematic_12V Regulated Power Supply.png` (also as PDF).

## Connections

- INPUT (H1) - the two 15V AC taps
- INPUT_GND - transformer center tap
- OUTPUT+12V, OUTPUT-12V, OUTPUT_GND - outputs

The silkscreen next to the input says INPUT_12V_AC but the schematic is drawn for 15V taps.
A 15-0-15 transformer is needed so the regulators have enough headroom.

## Parts

| Ref | Part |
| --- | --- |
| D1 | GBU406 bridge rectifier |
| 7812 | AS7812 +12V regulator, TO-252 |
| 7912 | LM7912 -12V regulator, TO-220 |
| C1, C2 | 1000uF electrolytic |
| C3, C4 | 10uF electrolytic |
| C5, C6 | 1uF |
| INPUT | 2 pin female header |
| INPUT_GND, outputs | 1 pin male header |

Full list with LCSC part numbers is in `BOM_PCB_12V Regulated Power Supply.csv` (EasyEDA export, UTF-16 tab separated).

## Files

- `Gerber_PCB_12V Regulated Power Supply.zip` - Gerber and drill files, ready to send to a PCB maker
- `BOM_PCB_12V Regulated Power Supply.csv` - bill of materials
- `Schematic_12V Regulated Power Supply.pdf` / `.png` - schematic
- `PCB_3D_2D_View.pdf` - routing, 3D and 2D views of the board

The rectified rails are around 20V so C1 and C2 should be rated 35V or more.
