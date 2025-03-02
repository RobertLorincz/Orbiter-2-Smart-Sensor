This beta firmware version is for use with the smart sensor with MMU unit.

The default firmware has a 1 second filter time on the filament detection signal; this is implemented to avoid multiple triggering of the sensor autoload features due to blobs on the filament tip. This filter time also causes a delay in the filament detection, which is not working well with MMU units with automatic filament change.

The O2SmartSensor_v2.4 firmware has this filter time reduced to about 100ms.

Firmware update procedure:

Be aware the procedure is for advanced users.
The sensor has an onboard ATtiny412 microcontroller.
Its firmware update requires a UPDI programmer for Microchip (Atmel) AVR microcontrollers. I use an ATMEL-ICE programmer.

1) Connect the sensor to a 5V power supply using the sensor connector power lines (pin3 -> +5V, pin4 -> GND).
2) Connect the UPDI signal to pin1 of the sensor connector, to the filament unload signal FU.
3) The FU signal has multiple functions and, by default, is configured as output. To put the sensor into programming mode, the unload button must be pressed for about 4 seconds. The sensor ring will start flashing with a white color, indicating the programming mode is activated.
4) Configure the fuse bits in the firmware programming interface with the values indicated in the SmartSensorFuses.png
5) Upload firmware; after uploading, the sensor should restart and enter into normal operating mode with the filament filter time set to 100ms.

