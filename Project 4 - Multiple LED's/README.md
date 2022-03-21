# Project 3 - Blinking with Servo
<p align="center">
	<img src="https://github.com/JonanthaW/Arduino-Projects/blob/main/Project%204%20-%20Multiple%20LED's%20/working.jpg" width="50%" />
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
		<li>3x LED(Generic)</li>
		<li>3x PushButtons</li>
		<li>3x Resistor 220 ohm (Ω) /1k ohm (kΩ)</li>
		<li>Jumper wires(generic)</li>
</ul>

<div align="center">
	<img src="https://github.com/JonanthaW/Arduino-Projects/blob/main/Project%204%20-%20Multiple%20LED's%20/sketch.gif" width="70%"/>
</div>

### :bulb: Code:

<p>After you build the circuit plug your Arduino board into your computer, start the Arduino Software (IDE) and enter the code below. </p>

<p>Turn it on:</p>

```
#define BUTTONGREEN 2
#define LEDGREEN 3
#define BUTTONRED 4
#define LEDRED 5
#define BUTTONYELLOW 6
#define LEDYELLOW 7

void setup()
{
  // Function GREEN LED/Button
  pinMode(BUTTONGREEN, INPUT_PULLUP);
  pinMode(LEDGREEN, OUTPUT);
  
  // Function RED LED/Button
  pinMode(BUTTONRED, INPUT_PULLUP);
  pinMode(LEDRED, OUTPUT);
    
  // Function YELLOW LED/Button
  pinMode(BUTTONYELLOW, INPUT_PULLUP);
  pinMode(LEDYELLOW, OUTPUT);
}

void loop()
{
  // GREEN Condition
 if(digitalRead(BUTTONGREEN) == LOW) {
  	digitalWrite(LEDGREEN, HIGH);
  }
 else {
  	digitalWrite(LEDGREEN, LOW);
  }
  
  // RED Condition
 if(digitalRead(BUTTONRED) == LOW) {
    digitalWrite(LEDRED, HIGH);
  }
 else {
    digitalWrite(LEDRED, LOW);
  }
    
  // YELLOW Condition
 if(digitalRead(BUTTONYELLOW) == LOW) {
    digitalWrite(LEDYELLOW, HIGH);
  }
 else {
    digitalWrite(LEDYELLOW, LOW);
  }
}
```
