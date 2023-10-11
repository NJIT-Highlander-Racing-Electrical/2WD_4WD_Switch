# 2WD_4WD_Switch

## Switch Design Goals

* Two outputs (5V out)
* Each 5V line latches when its respective Engaged/Disengaged 9V output to the front PTU is pressed
* Sends this data to dashboard, which can forward over CAN-Bus to DAQ system if necessary

* (MAYBE) capacitor on switch to make it so you just need to tap switch instead of holding
