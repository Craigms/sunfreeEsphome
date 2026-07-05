Configuration yaml for esphome.
Works with Sunfree / senrui k200/u motor installed in Persilux blinds often purchased from aliexpress/alibaba

Provides live update of blind position and allows for up, down and stop control.  Also allows to move blind to specified position in %.
More controls could be added that would be used to set blind limits (admin mode) but I haven't bothered as you typically only do that once so can just use the remote.


Motor has RJ11 plug on flying lead with RS232 so no need to open case.  Cut off plug and wire directly into an ESP32.  Do not use ESP32-C3 supermini, they have a very bad PCB layout with the antenna located right next to the crystal oscillator.  
This causes very poor wifi reception and frequent drop outs.  ESP32-S3 supermini layout is all good, as are many other ESP32 PCBs.

Wire colours for soldering to PCB are:
Black: RX (wire into ESP32 TX)
Red: TX (wire into ESP32 RX)
Green: 0V
Yellow: 5V

There is protection on the datalines if you wire them incorrectly.  If you apply too much voltage to the datalines you may have to open motor and remove the protection diodes on the TX and RX lines as they will be damanged.

Based off published RS232 protocol provided here:
https://www.sunfreemotor.com/page106?_l=en&article_id=156


