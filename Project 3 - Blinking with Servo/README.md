# Project 3 - Blinking with Servo
<p align="center">
	<img src="https://github.com/JonanthaW/Arduino-Projects/blob/main/Project%203%20-%20Blinking%20with%20Servo/working.jpg" width="50%" />
</p>

![Github](https://img.shields.io/badge/Difficulty-Easy-success)
![Github](https://img.shields.io/github/last-commit/JonanthaW/Arduino-Projects)

## :books: About it
In this project we connect a Micro Servo and a LED to the arduino. When the Micro servo moves, the LED lights up and vice versa.

## :floppy_disk: What will we use:
<ul>
		<li>1x Arduino UNO</li>
		<li>1x BreadBoard/ProtoBoard</li>
		<li>1x USB Cable</li>
		<li>1x LED(Generic)</li>
		<li>1x Resistor 220 ohm (Ω) /1k ohm (kΩ)</li>
		<li>1x Micro Servo</li>
		<li>Jumper wires(generic)</li>
</ul>

<div align="center">
	<img src="https://github.com/JonanthaW/Arduino-Projects/blob/main/Project%203%20-%20Blinking%20with%20Servo/sketch.jpg" width="90%"/>
</div>

### :bulb: Code:

<p>After you build the circuit plug your Arduino board into your computer, start the Arduino Software (IDE) and enter the code below. </p>

<p>Turn it on:</p>

```
#include <Servo.h>

#define LED 9  // The pin the LED is connected to
#define SERVO 2 // The digital port where Servo is connected

Servo s; // Var Servo
int pos; // Pos Servo


void setup() {
  s.attach(SERVO);
  s.write(0); // Servo pos initial 0
  pinMode(LED, OUTPUT); // Declare the LED as an output
}

void loop() {
    for(pos = 0; pos < 180; pos++)
  {
    s.write(pos); // Change the servo pos
    digitalWrite(LED, HIGH); // Turn the LED on
  	delay(15); // Wait 15 milisseconds
  }
  	digitalWrite(LED, LOW); // Turn the LED off
	delay(1000); // Wait 1 Second 
  for(pos = 180; pos >= 0; pos--)
  {
    s.write(pos); // Change the servo pos
    digitalWrite(LED, HIGH); // Turn the LED on
    delay(15); // Wait 15 milisseconds
  }
  	digitalWrite(LED, LOW); // Turn the LED off
	delay(1000); // Wait 1 Second
}
```
