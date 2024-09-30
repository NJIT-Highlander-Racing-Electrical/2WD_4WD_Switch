# 2WD_4WD_Switch

## Design Features

* 2WD/4WD switch connects to front PTU as usual, being able to toggle between states
* It has two methods of power:
  * Standard 12V vehicle power
  * 9V Battery auxiliary power for when the main power system is not active
  * The driver will be able to flip between these power sources using a SPDT (ON-ON) toggle switch 
* It will send data about its status back to the DAQ via two wires, where there are transistors to lock the HIGH voltage to 3.3v instead of 9-12v
  * We have a common ground with both the 12V and 9V power sources, so a ground connection for the data is not necessary
* The DAQ will receive the data from the two transistors, toggle the state of 2WD/4WD engagement accordingly, and relay this data over CAN-Bus so the dashboard can display it

## Enclosure Design Requirements

* Split enclosure so internals can be accessed
* Snap fit hole for main polarity reversing switch
* Mounting holes for chassis tab
* Clearance hole for MALE aviation plug connector (16mm)
* Clearance hole for SPDT ON-ON 9V/12V power switch (6mm)
* Slot for 9V battery and wires
   * Ideally, this pocket would have a 9V battery connector pigtail at the bottom of it so we can just press a 9V in

## Electrical Design/Soldering Plan

### See schematic in this repository for wiring diagram

### Aviation Plug Connections:

  * +12V on PIN 1
  * GND on PIN 2
  * SIGNALS on PIN 3 & PIN 4

### When 4WD is pressed:
* White wire (Green at DAS): 12V
* Black wire (Orange at DAS): 0V

### When 2WD is pressed:
* White wire (Green at DAS): Initially goes to 0V then goes to 12V when complete
* Black wire (Orange at DAS): 12V


### Wires from Switch to Diff:

 * Aviation 1: Dark Blue on Diff (Yellow on connecting wire)
 * Aviation 2: Baby Blue (Red on connecting wire)
 * Aviation 3: Brown/White (Black on connecting wire)

