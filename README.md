# Design-of-Automatic-Street-Light-System-using-LDR-Sensor-in-Tinkercad

**Aim:**

To measure the LDR Sensor using Photoresistor with Arduino UNO Board/ESP-32 using Tinker CAD. 
 
**Hardware / Software Tools required:**

- PC/ Laptop with Internet connection 
- Tinker CAD tool (Online) 
- Arduino UNO Board/ESP-32 
- Photoresistor 

**Circuit Diagram:**

<img width="1536" height="632" alt="Stunning Amberis" src="https://github.com/user-attachments/assets/c8ea2aca-6dfb-44f6-9c8a-0daef2e880ed" />

**Theory:**

The Arduino Uno is powered by the ATmega328P, an 8-bit microcontroller that runs at 16 MHz. It has 32 KB of flash memory, 2 KB of SRAM, and 1 KB of EEPROM. The board has 14 digital I/O pins (of which 6 can be used as PWM outputs) and 6 analog input pins. These pins allow the board to interface with various sensors, actuators, and other devices.The Arduino Uno can be powered via a USB connection or an external power supply. The board has a built in voltage regulator to manage power from 7 to 12 volts. The board is programmable using the Arduino IDE (Integrated Development Environment), which supports a simplified version of C/C++. The code, known as a "sketch," is uploaded to the board via a USB connection. The Uno has a USB-B port, which is used for communication with a computer. The USB connection also powers the board when connected. The board includes a reset button that restarts the microcontroller, useful during programming and troubleshooting. The In-Circuit Serial Programming (ICSP) header allows for low-level programming of the microcontroller or firmware updates. The Uno has a built-in LED on pin 13, commonly used for simple tests and debugging.

**Procedure**

1. Log in to Tinkercad, go to Circuits, and click Create New Circuit.

2. Add the Arduino Uno, an LDR (photoresistor), a small breadboard, a resistor (like 10kΩ), and jumper wires.

3. Connect one pin of the LDR to the Arduino 5V pin.

4. Connect the other LDR pin to one end of the resistor and also to the Arduino analog pin A1.

5. Connect the other end of the resistor to Arduino GND, forming a voltage divider.

6. Open the Code editor, switch to Text mode, and write the Arduino code for reading the LDR.

7. Start the simulation and check the serial monitor to see the LDR readings; adjust wiring or code if something is wrong.

8. Stop the simulation and save your circuit.


**Code:**
```
const int LEDPin=13; 
const int LDRPin=A0; 
void setup() 
{ 
  Serial.begin(9600); 
  pinMode(LEDPin,OUTPUT); 
  pinMode(LDRPin,INPUT); 
} 
void loop() 
{ 
  int LDRStatus=analogRead(LDRPin); 
  if(LDRStatus<=500) 
  { 
    digitalWrite(LEDPin,HIGH); 
    Serial.print("Current Light Intensity Value is -"); 
    Serial.println(LDRStatus); 
  } 
  else 
  { 
    digitalWrite(LEDPin, LOW); 
    Serial.print("Current Light Intensity Value is -"); 
    Serial.println(LDRStatus); 
  } 
}
```

**Output:**

<img width="1032" height="391" alt="Screenshot 2025-08-29 090950" src="https://github.com/user-attachments/assets/a88cdd81-67b3-48e7-8d2c-3aeec592059f" />

**Result:**

Thus measure the LDR Sensor using Photoresistor with Arduino UNO Board/ESP-32 using Tinker CAD has been Verified Successfully.
