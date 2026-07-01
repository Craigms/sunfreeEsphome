Configuration yaml for esphome.
Work with Sunfree motor installed in Persilux blinds off aliexpress/alibaba

Motor has RJ11 plug on flying lead with RS232 so no need to open case.  Cut off plug and wire directly into an ESP32.  Do not use ESP32-C3 supermini, they have a very bad PCB layout with the antenna located right next to the crystal oscillator.  
This causes very poor wifi receptino and frequent drop outs.  ESP32-S3 supermini layout is all good, as are many other ESP32 PCBs.

Wire colours for soldering to PCB are:
Black: RX (wire into ESP32 TX)
Red: TX (wire into ESP32 RX)
Green: 0V
Yellow: 5V

There is protection on the datalines if you wire them incorrectly.  If you apply too much voltage to the datalines you may have to open motor and remove the protection diodes on the TX and RX lines as they will be damanged.


