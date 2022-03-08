# Project 1 - Simple LED Circuit
<p align="center">
	<img src="https://github.com/JonanthaW/Arduino-Projects/blob/main/Project%201%20-%20Simple%20LED%20Circuit/working.jpg" width="50%" />
</p>

![Github](https://img.shields.io/badge/Difficulty-Easy-success)
![Github](https://img.shields.io/github/last-commit/JonanthaW/Arduino-Projects)

## :books: About it
In this project we are going to connect an LED to our ARDUINO board and make it stay on and/or blink.

## :floppy_disk: What will we use:
<ul>
		<li>1x Arduino UNO</li>
		<li>1x BreadBoard/ProtoBoard</li>
		<li>1x USB Cable</li>
		<li>1x LED(Generic)</li>
		<li>1x Resistor 220 ohm (Ω) /1k ohm (kΩ)</li>
		<li>Jumper wires(generic)</li>
</ul>

<div align="center">
	<img src="https://github.com/JonanthaW/Arduino-Projects/blob/main/Project%201%20-%20Simple%20LED%20Circuit/sketch.jpg" width="90%"/>
</div>

### :bulb: Code:

<p>After you build the circuit plug your Arduino board into your computer, start the Arduino Software (IDE) and enter the code below. </p>

<p>Stay on</p>

```
#define LED 13  // The pin the LED is connected to
void setup() {
  pinMode(LED, OUTPUT); // Declare the LED as an output
}

void loop() {
  digitalWrite(LED, HIGH); // Turn the LED on
}
```
<p>Make it blink</p>

```
#define LED 13 // the pin the LED is connected to

void setup() {
  pinMode(LED, OUTPUT); // Declare the LED as an output
}

void loop() {
  digitalWrite(LED, HIGH); // Turn the LED on
  delay(1000); // Wait for 1000 milliseconds (1 second)
  digitalWrite(LED, LOW); // Turn the LED off
  delay(1000); // Wait for 1000 milliseconds (1 second)
}
```
