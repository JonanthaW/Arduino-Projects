# Project 10 -Seven Display ON or OFF Cathode
<p align="center">
	<img src="https://github.com/JonanthaW/Arduino-Projects/blob/main/Project 10 -Seven Display ON or OFF Cathode/working.jpg" width="50%" />
</p>

![Github](https://img.shields.io/badge/Difficulty-Easy-success)
![Github](https://img.shields.io/github/last-commit/JonanthaW/Arduino-Projects)

## :books: About it

In this project we connect a 7 Segment Display and control it with cathode common.

## :floppy_disk: What will we use:
<ul>
		<li>1x Arduino UNO</li>
		<li>1x BreadBoard/ProtoBoard</li>
		<li>1x USB Cable</li>
		<li>1x 7 Segment Display</li>
		<li>1x Resistor 220 ohm (Ω) /1k ohm (kΩ)</li>
		<li>Jumper wires(generic)</li>
</ul>

<div align="center">
	<img src="https://github.com/JonanthaW/Arduino-Projects/blob/main/Project 10 -Seven Display ON or OFF Cathode/sketch.gif" width="70%"/>
</div>

### :bulb: Code:

<p>After you build the circuit plug your Arduino board into your computer, start the Arduino Software (IDE) and enter the code below. </p>

<p>Code:</p>

```
void setup()
{
  for(int i=1; i<=8; i++) {
  	pinMode(i, OUTPUT);
  }
}

void loop() {
  for(int i=1; i<=8; i++) {
  	digitalWrite(i,HIGH);
  }
  delay(1000);
  for(int i=1; i<=8; i++) {
  	digitalWrite(i,LOW);
  }
  delay(1000);
}
```
