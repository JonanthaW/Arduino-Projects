# Project 16 - Solar Energy Controller
<p align="center">
	<img src="https://github.com/JonanthaW/Arduino-Projects/blob/main/Project 16 - Solar Energy Controller/working.jpg" width="50%" />
</p>

![Github](https://img.shields.io/badge/Difficulty-Easy-success)
![Github](https://img.shields.io/github/last-commit/JonanthaW/Arduino-Projects)

## :books: About it

In this project we connect a Photoresistor and a LED to the arduino. When some light has been projected, the Photoresistor will turn on the LED.

## :floppy_disk: What will we use:
<ul>
		<li>1x Arduino UNO</li>
		<li>1x BreadBoard/ProtoBoard</li>
		<li>1x USB Cable</li>
		<li>1x Photoresistor </li>
		<li>1x LED(Generic)</li>
		<li>1x Resistor 220 ohm (Ω) /1k ohm (kΩ)</li>
		<li>Jumper wires(generic)</li>
</ul>

<div align="center">
	<img src="https://github.com/JonanthaW/Arduino-Projects/blob/main/Project 16 - Solar Energy Controller/sketch.gif" width="70%"/>
</div>

### :bulb: Code:

<p>After you build the circuit plug your Arduino board into your computer, start the Arduino Software (IDE) and enter the code below. </p>

<p>Code:</p>

```
#define LED 2

void setup()
{
  pinMode(LED, OUTPUT);
}

void loop()
{
  if(analogRead(A0) >= 600) {
  	digitalWrite(LED, HIGH);
  }
  else {
  	digitalWrite(LED, LOW);
  };
}
```
