# Designing-of-PCBs

PCBs I designed in EasyEDA during my ENTC course at Symbiosis Institute of Technology (2022).
Each folder is one board with its schematic, PCB layout, renders and parts list.

| Board | What it does | Layers | Size |
| --- | --- | --- | --- |
| [LED Board](LED%20Board) | Red, green and blue LED each with a 1k resistor | 1 | 30.6 x 21.5 mm |
| [5V Voltage Regulator](5V%20Voltage%20Regulator) | 12V AC in, bridge rectifier, 78L05, 5V DC out | 1 | 26.9 x 29.2 mm |
| [Dual 12V Power Supply](Dual%2012V%20Power%20Supply) | 15-0-15 AC in, 7812 and 7912, +12V / GND / -12V out | 2 | 61.5 x 43.9 mm |

## Folder contents

- `*.json` - EasyEDA Standard source files (schematic and PCB). Import them in EasyEDA to edit.
- `Schematic_*.png` / `.pdf` - schematic exports
- `PCB_*` - 2D and 3D views of the layout
- `BOM_*.csv` - bill of materials with LCSC part numbers
- `Gerber_*.zip` - fabrication files (only the dual supply has these so far)
- `Circuit Diagram.png` - the reference circuit the two regulator boards were based on

Each board folder has its own README with the parts list and a few notes on things to watch
when building it.

## Tools

- EasyEDA Standard 6.5.5 for schematic capture, layout and Gerber export
