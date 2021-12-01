# SH1106
This repository describes the detailed procedure to convert SPI compatible OLED display module to I2C and program to display Alphabetics and Graphics by intefacing OLED display with NodeMCU ESP8266 board.
OLED displays are widely used in different electronics gadgets with a special reference to IoT (**I**nternet **o**f **T**hings) applications. Obvious reasons are: Low power consumption, Tiny size, Wide view angle and high flexibility compared to its counterparts (LCD, Seven Segment). <br/>
Neverthless, these OLED displays have to be handled carefully. Every OLED display module comes with driver IC in its backplane, which can't be seen (encapsulated). The driver IC handles the pixels of the module, i.e., by programming the driver, individual pixel can be switched ON or OFF!
Broadly speaking, the OLEDs can be categorized as:
* Passive Matrix OLED (PMOLED)
* Active Matrix OLED (AMOLED)
* Transparent OLED
* Top Emitting OLED
* Foldable OLED and
* White OLED
