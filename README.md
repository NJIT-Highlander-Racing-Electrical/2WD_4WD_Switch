# 2WD_4WD_Switch

## Switch Design Goals

* 2WD/4WD switch connects to front PTU as usual, being able to toggle between states
* It will have two methods of power:
  * Standard 12V vehicle power
  * 9V Battery auxiliary power for when the main power system is not active
  * The driver will be able to flip between these power sources using a SPDT toggle switch 
* It will send data about its status back to the DAQ via two wires, where there is an Op-Amp to lock the HIGH voltage to 3.3v instead of 9-12v
* We have a common ground with both the 12V and 9V power sources, so a third ground connection is not necessary
* The DAQ will receive the data from the two Op-Amps, toggle the state of 2WD/4WD engagement accordingly, and relay this data over CAN-Bus so the dashboard can display it

## Enclosure Design Requirements

* Split enclosure so internals can be accessed
* Snap fit hole for main polarity reversing switch
* Mounting holes for threaded inserts in bottom (that attach to a mounting plate on chassis)
* Clearance hole for MALE aviation plug connector (16mm)
* Clearance hole for SPDT ON-ON 9V/12V power switch (6mm)
* Slot for 9V battery and wires
   * Ideally, this pocket would have a 9V battery connector pigtail at the bottom of it so we can just press a 9V in

## Electrical Design/Soldering Plan

* We can solder directly to the switch pins, no connectors needed like last year!
* See schematic in this repository for wiring diagram

* +12V ON AVIATION PIN 1
* GND ON AVIATION PIN 2
* SIGNALS ON 3 and 4

