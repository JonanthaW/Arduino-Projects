# Project 5 - Traffic Light
<p align="center">
	<img src="https://github.com/JonanthaW/Arduino-Projects/blob/main/Project 5 - Traffic Light/working.jpg" width="50%" />
</p>

![Github](https://img.shields.io/badge/Difficulty-Easy-success)
![Github](https://img.shields.io/github/last-commit/JonanthaW/Arduino-Projects)

## :books: About it
In this project we replicate a real traffic light using some LED's. It uses code as an internal timer and continues to run until you cut the Arduino's power supply. 

## :floppy_disk: What will we use:
<ul>
		<li>1x Arduino UNO</li>
		<li>1x BreadBoard/ProtoBoard</li>
		<li>1x USB Cable</li>
		<li>3x LED(Generic)</li>
		<li>3x Resistor 220 ohm (Ω) /1k ohm (kΩ)</li>
		<li>Jumper wires(generic)</li>
</ul>

<div align="center">
	<img src="https://github.com/JonanthaW/Arduino-Projects/blob/main/Project 5 - Traffic Light/sketch.gif" width="70%"/>
</div>

### :bulb: Code:

<p>After you build the circuit plug your Arduino board into your computer, start the Arduino Software (IDE) and enter the code below. </p>

<p>Code:</p>

```
#define REDLED 2
#define YELLOWLED 3
#define GREENLED 4

void setup()
{
  pinMode(REDLED, OUTPUT);
  pinMode(YELLOWLED, OUTPUT);
  pinMode(GREENLED, OUTPUT);
}

void loop()
{
  // setting up initial with yellow
  digitalWrite(REDLED, LOW);
  digitalWrite(YELLOWLED, HIGH);
  digitalWrite(GREENLED, LOW);
 
  // waiting 2s in yellow
  delay(2000);
 
  // we turn off the yellow and turn on the red
  digitalWrite(YELLOWLED, LOW);
  digitalWrite(REDLED, HIGH);
 
  // waiting 5s w Red
  delay(5000);  
 
  // Green signal, let's go
  digitalWrite(GREENLED, HIGH);
  digitalWrite(REDLED, LOW);
 
  // waiting 5s w green
  delay(5000);
}
```
