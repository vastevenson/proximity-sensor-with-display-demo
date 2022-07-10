### proximity-sensor-with-display-demo

#### Goal

Create an Arduino that can show the real-time distance between an object and a proximity sensor on a seven segment display to avoid requiring the Serial Monitor on a connected PC over the USB cable. 
* Demo of project: https://youtu.be/-R0MfcWrQ3U

#### Set up 
* Clone this repo and upload the `.ino` file to your Arduino. 
* Make sure to attach one 220 ohm resistor to each of the seven segments of your display - make note that this code assumes you're using a common cathode display, common wire(s) goes to GND and when a given segment sees a +5V difference to common, it will light up. 
** If you're using a common anode display, common should go to +5V side and modify the `display_dig()` function to change to `LOW`. You will also need to modify the `turn_off_all_segs()` and `turn_on_all_segs()` similarly as it's the opposite for common anode displays. 
* Make sure that each of the seven segments (`a` through `g` match up to the appropriate pins - the code assumes you're hooking them up to pins `4` through `10` respectively
* Connect the proximity sensor VCC pin to 5V and GND to GND (can be the same common GND as the seven segment display)
* Make sure to connect the Trig (trigger/transmitter) and Echo (receiver) pins to 3,2 respectively. 
