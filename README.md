# loadcell_intro

- https://learn.sparkfun.com/tutorials/load-cell-amplifier-hx711-breakout-hookup-guide/arduino-example

- https://www.hbm.com/en/7163/wheatstone-bridge-circuit/

- https://www.robotshop.com/community/forum/t/hx711-and-a-single-strain-gauge/48600/6

# Steps
- Download and install Arduino IDE
- Download and install driver package for CP1202 (UART to USB ) for windows
- Download and install board package for Espresif ESP32
- Select Board package in Arduino IDE for ESP32 Dev Kit (for XUIXIN ESP32 boards)

- Open Serial monitor on the correct COM port.

- Press "BOOT" button on the ESP32 board and press "Install" in the IDE, release after download is complete.
- Click "EN" button to start the program

# Calculation for direct analog connection to loadcell.

3.3V - 350 Ohms -> 350 Ohm Load cell -> Ground
                 +--> A0 pin of Arduino for analog read.
                 
Full scale is 4095 => 3300mV/4095 = 0.806mV per step
3.3*350/700 - 3.3*349/699 = 2.3605mV => approx 3 steps change.

Better to use bridge configuration with HX711

#
