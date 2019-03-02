# AND!XOR SAO Reference Designs
This is where we will publically post our reference designs for SAOs. Some may just be schematics, some may include Kicad projects (depending on the SAO). 

## DC619 EEPROM ##
Simple I2C EEPROM SAO based on the AT24C02N. All address pins are pulled to GND. Badges that detect the AT24C02N on the I2C bus should query for bytes at known addresses then perform actions.

Additionally, the SAO has two LEDs on GPIO1 and GPIO2 pins. 

The AND!XOR badge will natively support this design and blink the LEDs in a special pattern when an SAO with AT24C02N is detected. 
