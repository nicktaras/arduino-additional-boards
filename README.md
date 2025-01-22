# Arduino Additional Boards - ATTINY & ESP8266 Setup

This repository provides a guide on how to set up ATTINY and ESP8266 boards with the Arduino IDE.

### Work in Progress

Here are the steps to get started:

### 1. **Install ESP8266 package for Arduino IDE**
   - Open Arduino IDE.
   - Go to **Preferences**.
   - In **Additional Boards Manager URLs**, add the following:
     ```
     http://arduino.esp8266.com/stable/package_esp8266com_index.json
     ```

### 2. **Install ATTINY package for Arduino IDE**
   - In **Preferences**, add the following:
     ```
     https://raw.githubusercontent.com/damellis/attiny/ide-1.6.x-boards-manager/package_damellis_attiny_index.json
     ```

### 3. **Install ATTINY Board Support**
   - Go to **Tools** > **Board** > **Boards Manager**.
   - Search for **ATTINY** by Davis A. Mellis and install it.

### 4. **Set up Arduino as ISP**
   - Upload the **ArduinoISP** example to your Arduino Uno:
     - Go to **File** > **Examples** > **11.ArduinoISP** > **ArduinoISP**.
   - Change the programmer to **Arduino as ISP**:
     - **Tools** > **Programmer** > **Arduino as ISP**.

### 5. **Wire up the ATTINY**
   - Connect the ATTINY chip to the Arduino using the schematic for Arduino as ISP.
     - See more: [HighLowTech Arduino as ISP tutorial](http://highlowtech.org/?p=1706).

### 6. **Configure ATTINY Settings**
   - Set the board to **ATTiny**.
   - Choose **ATtiny85** with an 8 MHz (internal) clock.

### 7. **Burn the Bootloader**
   - Go to **Tools** > **Burn Bootloader** to set the fuses correctly for the ATTINY85.

### 8. **Upload Sketch to ATTINY**
   - Finally, upload your sketch to the ATTINY using **Tools** > **Upload Using Programmer**.
