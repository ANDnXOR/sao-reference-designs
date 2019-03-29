# AND!XOR SAO Reference Designs
This is where we will publically post our reference designs for SAOs. Some may just be schematics, some may include Kicad projects (depending on the SAO). 

## I2C Addresses ##

| Type 			| IC   		| 7-bit address	|
|:-:			|:-:	    |:-:	        |
| GPIO Expander	| MCP23017	| 0x20		  	|
| EEPROM		| AT24C32 	| 0x50		 	|
| REDACTED  	| REDACTED 	| TBD			|

## EEPROM ##
Simple I2C EEPROM SAO based on the AT24C32. All address pins are pulled to GND. Badges that detect the AT24C32 on the I2C bus should query for bytes at known addresses then perform actions.

AND!XOR has adopted the following format for data stored in the EEPROM, we hope that others from #badgelife do too.
| 0			| 1			| 2 			| 3...n		|
| :-:		| :-:		| :-:			| :-:		|
| DC Year	| Maker ID	| SAO Type ID 	| Data 		|

* DC Year: Use 0x1B for DC27
* Maker ID: Unique identifier for SAO maker, AND!XOR uses 0x49 (Middle 8bits of our registered Bluetooth ID) 
* SAO Type ID: Unique identifier assigned by the maker for the SAO
* Data: Arbitrary data parseable by anything recognizing DC, Maker, and SAO values

## GPIO Expander ##

Returning from DC26 we will be using MCP23017-based SAO(s). When the MCP23017 is detected on the bus, the badge will play special patterns. d
