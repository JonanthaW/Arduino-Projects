# Arduino-Projects
<p align="center">
	<img src="https://github.com/JonanthaW/Arduino-Projects/blob/main/Project%201%20-%20Simple%20LED%20Circuit/2-ligada.jpeg" width="50%" />
</p>

Arduino is an open source physical computing platform based on simple I/O
board and a development environment that implements the Processing/Wiring
tongue. Arduino can be used to develop standalone interactive objects or
can be connected to software on your computer (eg Flash, Processing and MaxMSP).
The plates can be assembled manually or purchased pre-assembled; the open source
IDE can be downloaded for free from [https://arduino.cc](https://www.arduino.cc/en/Main/Software).

![Github](https://img.shields.io/github/v/release/arduino/Arduino)

## :books: About it
In this project we are going to connect an LED to our ARDUINO board and make it stay on and/or blink.

## :floppy_disk: What will we use:

<h3>Need:</h3>
	<ul>
		<li>1x Arduino UNO</li>
		<li>1x Protoboard</li>
		<li>1x USB Cable</li>
		<li>1x LED(Generic)</li>
		<li>Jumper wires(generic)</li>
		<li>Resistor 220 ohm/1k ohm</li>
</ul>

<div align="center">
	<img src="https://github.com/JonanthaW/Arduino-Projects/blob/main/assets/kit-1.jpeg" width="90%"/>
</div>

### :bulb: Code:

<p>Copy and paste this code into your Arduino IDE or Web Editor. </p>

<h2>To stay on</h2>

```
#define LED 13  // The pin the LED is connected to
void setup() {
  pinMode(LED, OUTPUT); // Declare the LED as an output
}

void loop() {
  digitalWrite(LED, HIGH); // Turn the LED on
}
```
<h2>Make it blink</h2>
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
