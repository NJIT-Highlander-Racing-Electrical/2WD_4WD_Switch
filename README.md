# 2WD_4WD_Switch

## Switch Design Goals

* Have two voltage dividers that take 9V from switch press and converts to 5V signal (connected to DAQ)
* One turns on when the switch is pressed to the 4WD engagement state
* One turns on when the switch is pressed to the 4WD disengagement state
* Read both of these on the DAQ Arduino side and light up dashboard accordingly over CAN-Bus
  
* (MAYBE) capacitor on switch to make it so you just need to tap switch instead of holding
