# Project 7 - LED Dice
<p align="center">
	<img src="https://github.com/JonanthaW/Arduino-Projects/blob/main/Project 7 - LED Dice/working.jpg" width="50%" />
</p>

![Github](https://img.shields.io/badge/Difficulty-Easy-success)
![Github](https://img.shields.io/github/last-commit/JonanthaW/Arduino-Projects)

## :books: About it
In this project we will build a circuit that will generate a random number between 0 and 6 and show it using LED'S, while the PushButton is pressed.

## :floppy_disk: What will we use:
<ul>
		<li>1x Arduino UNO</li>
		<li>1x BreadBoard/ProtoBoard</li>
		<li>1x USB Cable</li>
		<li>6x LED(Generic)</li>
		<li>6x Resistor 220 ohm (Ω) /1k ohm (kΩ)</li>
		<li>1x PushButton</li>
		<li>Jumper wires(generic)</li>
</ul>

<div align="center">
	<img src="https://github.com/JonanthaW/Arduino-Projects/blob/main/Project 7 - LED Dice/sketch.gif" width="70%"/>
</div>

### :bulb: Code:

<p>After you build the circuit plug your Arduino board into your computer, start the Arduino Software (IDE) and enter the code below. </p>

<p>Code:</p>

```
#define control_button 8 // pin for the button switch
const int leds[] = {2, 3, 4, 5 , 6, 7}; // Leds and pins
boolean buttonFlag = false; // value to check state of button switch

void setup()
{
  randomSeed(analogRead(0)); //random seed by noise from analog pin 0
  for(int i=0; i<=5; i++) {
  		pinMode(leds[i], OUTPUT); //All leds set as OUTPUT
  }
  pinMode(control_button, INPUT_PULLUP); //Button Input
}

void loop()
{
  while(digitalRead(control_button) == LOW && buttonFlag == false) { // if button is being pressed
  	int diceSide = random(7); // Get random number and set to var
    for(int i=0; i<=diceSide-1; i++) {
  		digitalWrite(leds[i], HIGH); // light leds according to diceSide
  	}
    buttonFlag = true; // set buttonFlag
  };
  
  if(digitalRead(control_button) == HIGH) { // button isnt being pressed
  	for(int i=0; i<=6; i++) {
  		digitalWrite(leds[i], LOW); // Turn off all LEDS
      	delay(2); // wait 2 millisseconds
  	}
    buttonFlag = false; //set buttonFlag
  };
}
```
