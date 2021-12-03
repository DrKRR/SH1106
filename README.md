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
OLED modules support SPI or I2C Protocol. Certain modules support both protocols with a little modification of components at its backplane. One important point to note is that they use different drivers to work with. Popular drives used in 0.96" and 1.3" OLED modules are SSD1306 and SH1106, respectively. <br/> Here, I am going to explain the application of 0.96", 128X64 module in IoT (SSD1306 Driver, I2C Protocol) and the 1.3", 128X64 module working in SPI and I2C Protocols (SH1106 Driver). Hardware and software details are given. 

#### Application of 0.96" OLED(128X64) to display Temperature, Pressure and Altitude:
Following are the figures of front and rear views of 0.96"OLED with 4-Pin I2C with SSD1306 Driver. 
<br/>
<p align = "center"><img src="https://github.com/DrKRR/SH1106/blob/main/0.96-inch-oled-display-module-4-pin-800x800-1.jpg" width = "350" height = "150"></p>
As shown in the above figure, the I2C address can be chosen either 0x78 or 0x7A by connecting the 4k7 resistor appropriately. The selected address is used in the program to display the information on the OLED.<br/> In the present project, as an IoT example, I am going to explain the interfacing IC BMP280 and OLED with NodeMCU ESP8266 board. The program is developed in Arduino environment (Arduino IDE).<br/>
BMP280 is a temperature and barometric pressure sensor from Bosch Sensortech. It differs from BME280 that the later measures not only temperature and pressure but also humidity. Salient features of these sensors are: reasonably good accuracy (temp. :+/-1.0 degree celsius, barometric press. :+/-1.0 hPa, altitude:+/-1.0 meter), low energy consumption, very small in size and low-cost. Further, Adafruit library is readily available  supporting SPI/I2C protocol for interfacing (I2C address: 0x76 and 0x77). The following figure shows the tiny BMP280 board:
<br/>
<p align = "center"><img src="https://github.com/DrKRR/SH1106/blob/main/BMP280.jpg" width = "250" height = "200"> </p>The sensor works in the voltage range of 1.8 to 3.6V. As I am working at 3.3V, it is well suited. Usally,the board comes with connector not soldered. I have soldered a 6-pin berg connector. As I have mentioned earlier, I am using NodeMCU ESP8266 as controller for displaying temperature, barometric pressure and altitude on OLED display. The hardware connections to accomplish this task is shown in the following diagram:<br/>
<p align = "center"><img src="" width = "250" height = "200"> </p>
 
 
 
  
  
  
   
    
    
                                                                                  

    

    
   
  

   
 



