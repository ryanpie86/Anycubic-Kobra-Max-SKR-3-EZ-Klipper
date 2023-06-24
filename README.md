# Anycubic-Kobra-Max-SKR-3-EZ-Klipper
Klipper configuration for Kobra Max and SKR 3 EZ

This board is advertised to come shipped with an STM32H743 CPU, however I have received two now that instead have an STM32H723. There are compiles for each (USB communication) in the /firmware directory.

If you are using the factory Kobra Max print head with strain gauge, you will also need to purchase or build a Logic Level Shifter for the probe. The probe outputs 5V to the GPIO, which are 3.3V on the SKR 3 (and really most mainboards). The shifter will convert this to 3.3V and make everything happy. 

https://www.sparkfun.com/products/12009

It is also recommended, but not required, to use a reverse polarity protection diode on the reset pin, allowing your 3.3V from the reset pin to only travel into the print head. I have on several occasions "caught" the strain gauge throwing 5V out of the reset pin and into my mainboard.
