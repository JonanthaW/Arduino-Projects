# Project 2 - Buzzer and Button
<p align="center">
	<img src="https://github.com/JonanthaW/Arduino-Projects/blob/main/Project%202%20-%20Buzzer%20and%20Button/working.jpg" width="50%" />
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
		<li>1x Buzzer/Piezo</li>
		<li>Jumper wires(generic)</li>
		<li>1x PushButton</li>
</ul>

<div align="center">
	<img src="https://github.com/JonanthaW/Arduino-Projects/blob/main/Project%202%20-%20Buzzer%20and%20Button/sketch.jpg" width="90%"/>
</div>

### :bulb: Code:

<p>After you build the circuit plug your Arduino board into your computer, start the Arduino Software (IDE) and enter the code below. </p>

```
int pushButton = 2;
int frequency = 00;
int buzzer = 9;

void setup() {
 pinMode(buzzer,OUTPUT);
 pinMode(pushButton, INPUT_PULLUP);
}
 
void loop() {
 //buttonState = digitalRead(pushButton); 
  
 if(digitalRead(pushButton) == LOW) {
  	tone(buzzer,frequency);
   frequency+=10;
   delay(500);
  }
  else {
  	noTone(buzzer);
    frequency = 0;
  }
}
```
