# MIDI-sync-power-dev-board

The MIDI-sync-power-dev-board is a 4hp eurorack module created to be used either as an expander for other board or as a standalone module helping you developping electronic.
The module provides :
- an isolated 5V 400mA
- a 3.3V 200mA from LDO
- a Sync in from 3.5mm jack (use as sync, gate, trigger, ...)
	- 0-xV signal input transformed to TTL level (signal is inverted)
- a MIDI input or MIDI output configurable through soldering jumper
	- Can only use one configuration at a time!

The module has a 2x a 10 pins header on top and bottom that gives you access to eurorack +12V and -12V, the board 5V and 3.3V, the Sync signal, the MIDI in or MIDI out signal. 


| Signal names|   |
|----------|---------|
| +5V      | +3.3V   |
| +12V     | -12V    |
| GND      | GND     |
| MIDI OUT | GND     |
| Sync IN  | MIDI IN |

The idea behind this module came while developping my own synth that needed MIDI input. I had to make my own little MIDI In through optocoupler on breadboard or veroboard each time. 

Additonally, I created the [Canvas](https://github.com/lucblender/simple_canvas) synthesizer in collaboration with [Synthux Academy](https://www.synthux.academy). And the board did not have MIDI input or sync in making it hard to sync with any synthesizer setup. To not add complexity to the design, I prefered to create this little expander that I now use to power the Canvas and use Sync in and MIDI input.

## Schematic

![Schematic](pictures/schematic.png)

## PCB

|Top|Bottom|
|----|----|
|![top](pictures/circuit-board-top.png)|![bottom](pictures/circuit-board-bottom.png)|

### MIDI configuration

|MIDI in|MIDI out|
|----|----|
|On the bottom, you need to solder JP1 and JP2|On the top, you need to solder JP3, JP4 and JP5|

*Reminder*: You can only use one MIDI configuration at a time!

## Front panel

The MIDI-sync-power-dev-board has mutliple front panel since it can be use for various reason.
- midi-sync-module-front-panel-**a**: Dedicated to the Canvas
- midi-sync-module-front-panel-**b**: Generic Sync In, MIDI OUT
- midi-sync-module-front-panel-**c**: Generic Sync In, MIDI IN

All the front panel are double sided. On the Top you will find a the debug front panel with 10 pins header description. And on the Bottom you will find the custom design.

### Front Panel Example

| front-panel-**a**-top|front-panel-**a**-bottom|front-panel-**b**-top|front-panel-**b**-bottom|front-panel-**c**-top|front-panel-**c**-bottom|
|----|----|----|----|----|----|
|![a-top](pictures/front-panel-a-top.png)|TODO|![b-top](pictures/front-panel-b-top.png)|![b-bottom](pictures/front-panel-b-bottom.png)|![c-top](pictures/front-panel-c-top.png)|![c-bottom](pictures/front-panel-c-bottom.png)||