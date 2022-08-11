# Project 11 - Servo with Button
<p align="center">
	<img src="https://github.com/JonanthaW/Arduino-Projects/blob/main/Project 11 - Servo with Button/working.jpg" width="50%" />
</p>

![Github](https://img.shields.io/badge/Difficulty-Easy-success)
![Github](https://img.shields.io/github/last-commit/JonanthaW/Arduino-Projects)

## :books: About it

In this project we connect a Micro Servo into the arduino and control it using a pushButton.
When we press the button, the Micro Servo will rotate to a certain position and return back to the original position after.

## :floppy_disk: What will we use:
<ul>
		<li>1x Arduino UNO</li>
		<li>1x BreadBoard/ProtoBoard</li>
		<li>1x USB Cable</li>
		<li>1x Micro Servo</li>
		<li>1x PushButton</li>
		<li>Jumper wires(generic)</li>
</ul>

<div align="center">
	<img src="https://github.com/JonanthaW/Arduino-Projects/blob/main/Project 11 - Servo with Button/sketch.gif" width="70%"/>
</div>

### :bulb: Code:

<p>After you build the circuit plug your Arduino board into your computer, start the Arduino Software (IDE) and enter the code below. </p>

<p>Code:</p>

```
#include <Servo.h>
#define SERVO 2 // The digital port where Servo is connected
#define pushButton 3
Servo s; // Var Servo
int pos; // Pos Servo


void setup() {
  pinMode(pushButton, INPUT_PULLUP);
  s.attach(SERVO);
  s.write(0); // Servo pos initial 0
}

void loop() {
  if(digitalRead(pushButton) == LOW) {
    for(pos = 0; pos < 180; pos++)
  {
    s.write(pos); // Change the servo pos
  	//delay(15); // Wait 15 milisseconds
  }
	delay(1000); // Wait 1 Second 
  for(pos = 180; pos >= 0; pos--)
  {
    s.write(pos); // Change the servo pos
    //delay(15); // Wait 15 milisseconds
  }
	delay(1000); // Wait 1 Second
  }
}
```
