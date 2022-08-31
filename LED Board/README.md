# LED Board

Small single sided board with a red, a green and a blue 3 mm LED. Each LED has its own 1k resistor
and all three are fed from a 2 pin header (H1). Board size is about 30.6 x 21.5 mm.

## Parts

| Ref | Part |
| --- | --- |
| R1, R2, R3 | 1k axial resistor |
| RED | 3 mm red LED (Everlight 204-10SDRD) |
| GREEN | 3 mm green LED (Everlight 204-10SYGD) |
| BLUE | 3 mm blue LED (Everlight 204-10SUBC) |
| H1 | 2 pin female header, pin 1 = supply, pin 2 = GND |

Full list with LCSC part numbers is in `BOM_PCB_led_project.csv`.

## Files

- `led_project.json` - EasyEDA schematic
- `PCB_led_project.json` - EasyEDA PCB layout
- `Schematic_led_project.png` - schematic export
- `PCB_PCB_led_project*.png` - PCB, 2D and 3D views
- `OBJ_PCB_led_project.zip` - 3D model (.obj + .mtl) of the board

To open the design import the two .json files in EasyEDA (Standard edition).

## Note

The schematic labels the supply as 3V but that is too low for the blue LED. It drops around 3.3V
at normal current so at 3V it hardly lights and red and green only get about 1 mA through 1k.
Power the board from 5V instead. That gives roughly 3 mA for red and green and about 2 mA for blue.
