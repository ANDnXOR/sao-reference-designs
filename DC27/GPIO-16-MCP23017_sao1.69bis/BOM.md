# GPIO 16 (MCP23017) reference design #

Simple design, GPIO is driven high or low as output or can be used as input over I2C. For this design we drive all GPIO as output. See [https://github.com/ANDnXOR/ANDnXOR_DC26_Badge/blob/master/Firmware/components/drivers/addons.c] for an example driver. 

## BOM ##
* 1 x MCP23017-E/SS - SSOP-20
* 16 x LED
* 16 x 1k ohm resistors
* 1 x 0.1uF capacitor
* 1 x 2x3 male pin header (keyed / shrouded preferred AKA IDC on Ebay)
