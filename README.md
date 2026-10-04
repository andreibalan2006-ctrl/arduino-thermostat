# Arduino Smart Thermostat & Cooling System

## Description
A basic smart thermostat project built with an Arduino Uno. This system monitors the ambient temperature using a TMP36 sensor, displays the real-time data on an LCD screen, and automatically turns on a DC motor (acting as a cooling fan) when the temperature exceeds a certain threshold.

## Features
* **Real-time Monitoring:** Reads and calculates the temperature in Celsius.
* **LCD Output:** Displays the current temperature clearly on a 16x2 LCD screen.
* **Automatic Cooling:** Activates a 9V-powered DC motor fan using an NPN transistor when the environment gets too hot.

## Hardware Components
* 1x Arduino Uno
* 1x Breadboard
* 1x 16x2 LCD Display (with potentiometer for contrast)
* 1x TMP36 Temperature Sensor
* 1x DC Motor (Fan)
* 1x NPN Transistor (for motor control)
* 1x Resistor
* 1x 9V Battery (to power the motor)
* Jumper wires

## Wiring & Circuit
* **Power:** The Arduino provides 5V and GND to the breadboard logic. The 9V battery powers the motor, sharing a common GND with the Arduino.
* **Display:** The LCD is wired using 4-bit mode to Arduino digital pins (12, 11, 5, 4, 3, 2).
* **Sensor:** The TMP36 output pin is connected to Arduino analog pin `A0`.
* **Motor Control:** Arduino digital pin `6` triggers the base of the NPN transistor through a resistor. When triggered, the transistor closes the circuit, allowing the 9V battery to spin the motor.

## How to Use
1. Assemble the circuit according to the components list.
2. Clone this repository or download the `.ino` sketch file.
3. Open the sketch in the Arduino IDE.
4. Upload the code to your Arduino Uno.
5. The LCD will start displaying the temperature. If you warm up the sensor, the fan will automatically start!
