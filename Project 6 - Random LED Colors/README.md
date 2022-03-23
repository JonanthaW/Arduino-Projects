# Project 6 - Random LED Colors
<p align="center">
	<img src="https://github.com/JonanthaW/Arduino-Projects/blob/main/Project 6 - Random LED Colors/working.jpg" width="50%" />
</p>

![Github](https://img.shields.io/badge/Difficulty-Easy-success)
![Github](https://img.shields.io/github/last-commit/JonanthaW/Arduino-Projects)

## :books: About it
In this project we will put an RGB LED to show random colors. Simple and Easy.

## :floppy_disk: What will we use:
<ul>
		<li>1x Arduino UNO</li>
		<li>1x BreadBoard/ProtoBoard</li>
		<li>1x USB Cable</li>
		<li>1x LED RGB</li>
		<li>1x Resistor 220 ohm (Ω) /1k ohm (kΩ)</li>
		<li>Jumper wires(generic)</li>
</ul>

<div align="center">
	<img src="https://github.com/JonanthaW/Arduino-Projects/blob/main/Project 6 - Random LED Colors/sketch.gif" width="70%"/>
</div>

### :bulb: Code:

<p>After you build the circuit plug your Arduino board into your computer, start the Arduino Software (IDE) and enter the code below. </p>

<p>Code:</p>

```
#define red_led 2
#define blue_led 3
#define green_led 4

void setup()
{
  pinMode(red_led, OUTPUT);
  pinMode(blue_led, OUTPUT);
  pinMode(green_led, OUTPUT);
}

void loop()
{
	rgb_value(); // Calling the function and sending it to arduino
  	delay(50); // waiting 50 milisseconds
}

void rgb_value() { // Function to get random colors
	return analogWrite(red_led, random(256)), analogWrite(blue_led, random(256)), analogWrite(green_led, random(256));
}
```
