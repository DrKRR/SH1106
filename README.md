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
<br/>
AMOLED modules are costly compared to PMOLED modules. Futher, PMOLED modules of the following sizes (inches indicate length of the module (not diagonal) x,y indiactes the number of pixels) are widely used and are also popular. <br/>
Dimension: 0.66", 0.91", 0.96", 1.3", 1.54" etc.; Pixel density: 128X32, 128X64 and 128X128 etc.
OLED modules support SPI or I2C Protocol. Certain modules support both protocols with a little modification of components at its backplane. One important point to note is that they use different drivers to work with. Popular drives used in 0.96" and 1.3" OLED modules are SSD1306 and SH1106, respectively. 
