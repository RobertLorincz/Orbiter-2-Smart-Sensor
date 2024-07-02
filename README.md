# Orbiter-2-Smart-Sensor
Orbiter 2 Smart Sensor

![Uploading orbiter3.gif…]()


This is a brand-new sensor design, much improved compared to the previous sensor version.

First big change is the filament tangle detection functionality. Tangled filament is one of the common causes of print failures. When the filament is tangled on the spool, the force required to pull the filament into the extruder increases, this triggers the detection senor and consequently runs a Klipper macro to pause the printing and inform the user about the issue. The detection is activated when the pulling force is increased over two kilos of force for more than one second. Wear of PTFE tube can also trigger tangle detection due high friction force.

Second big change is signals filtering and plausibility check by onboard microcontroller. Klipper native filament sensor support is not the best to filter out all kind of fake detections and debouncing of the input signals. To improve this, this sensor is equipped with a small eight-bit microcontroller just for that job plus control the RGB input light based on the sensor state in a much nicer way than is possible by Klipper macros.

Last but not least, push-fit collet clip for a better PTFE tube locking with RGB illuminated
ring around, which indicates the filament sensor / extruder status:

Red - no filament detected

Green - filament present

Blue blinking - filament unload

Yellow blinking - filament tangle
