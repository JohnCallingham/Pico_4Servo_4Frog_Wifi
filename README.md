# Pico_4Servo_4Frog_Wifi
This program provides;-
- A Pico W using Wifi to connect to an OpenLCB/LCC hub. You must provide local network credentials and then it searches for a hub using mDNS. JMRI has an OpenLCB/LCC hub available.
- Demonstrates using the native Servo driver that uses PIO processors. This is limited to 7 while using WiFi, but only 4 are used here.
- Each servo has 3 positions whose factory reset positions are;-
    - position 1 (Thrown) - 80 degrees
    - position 2 (Mid) - 90 degrees
    - position 3 (Closed) - 100 degrees
- This allows only the smallest of movements which can be adjusted when connected to a turnout.
- Each position has 1 consumed event and 2 produced events as below;-
    - a consumed event which starts the servo moving to that position.
    - a produced event which is sent when the servo reaches that position.
    - a produced event which is sent when the servo leaves that position.
- Outputs provide for frog switching. JMRI can be used to configure the frog switching outputs so that the frog is switched according to the servo position reached.
- The mid point can be used to centre the servo for installation.
- When the module starts it sends out the leaving event for all servo positions and sets all servos to
their mid position.
