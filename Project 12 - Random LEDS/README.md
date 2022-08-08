# Project 12 - Random LEDS
<p align="center">
	<img src="https://github.com/JonanthaW/Arduino-Projects/blob/main/Project 12 - Random LEDS/sketch.jpg" width="50%" />
</p>

![Github](https://img.shields.io/badge/Difficulty-Easy-success)
![Github](https://img.shields.io/github/last-commit/JonanthaW/Arduino-Projects)

## :books: About it

In this project we connect 4 LEDS into the arduino and generate random sequence of colors (The piezo will sound differently for every LED).
We can control the number of generated sequences changing the value of "char SELECTED[random(0, 25)];" to any number we prefer.

## :floppy_disk: What will we use:
<ul>
		<li>1x Arduino UNO</li>
		<li>1x BreadBoard/ProtoBoard</li>
		<li>1x USB Cable</li>
		<li>1x Piezo </li>
		<li>4x LED(Generic)</li>
		<li>4x Resistor 220 ohm (Ω) /1k ohm (kΩ)</li>
		<li>Jumper wires(generic)</li>
</ul>

<div align="center">
	<img src="https://github.com/JonanthaW/Arduino-Projects/blob/main/Project 12 - Random LEDS/sketch.gif" width="70%"/>
</div>

### :bulb: Code:

<p>After you build the circuit plug your Arduino board into your computer, start the Arduino Software (IDE) and enter the code below. </p>

<p>Code:</p>

```
#define REDLED 2
#define GREENLED 3
#define YELLOWLED 4
#define BLUELED 5

#define PIEZO 13

void setup()
{
  pinMode(REDLED, OUTPUT);
  pinMode(YELLOWLED, OUTPUT);
  pinMode(BLUELED, OUTPUT);  
  pinMode(PIEZO, OUTPUT);
  
  randomSeed(analogRead(13));
  beginGame();
}

void loop()
{
  beginMatch();
}


void beginGame() {
  // Init game and play a music
  const int LED[4] = {2, 3, 4, 5};
  tone(PIEZO, 329);
  delay(300);
  tone(PIEZO, 493);
  for(int i=2; i<=6; i++) {
  	digitalWrite(i, HIGH);
  }
  delay(600);
  for(int i=2; i<=6; i++) {
    digitalWrite(i, LOW);
  }
  noTone(PIEZO);
  delay(1000);
}

void beginMatch() {
  // Generating sequence
  char COLORS[4] = {'R', 'G', 'Y', 'B'};
  char SELECTED[random(0, 25)];
  for(int k=0; k<sizeof(SELECTED); k++) {
  	SELECTED[k] = COLORS[random(0, sizeof(COLORS))];
  }
  
  // Showing it
  for(int j=0; j<sizeof(SELECTED); j++) {
    if(SELECTED[j] == 'R') {
    	digitalWrite(2, HIGH);
        delay(500);
      	tone(PIEZO, 293);
    	digitalWrite(2, LOW);
      	delay(250);
      	noTone(PIEZO);
    }
    else if(SELECTED[j] == 'G') {
    	digitalWrite(3, HIGH);
        delay(500);
      	tone(PIEZO, 329);
    	digitalWrite(3, LOW);
      	delay(250);
      	noTone(PIEZO);
    }
    else if(SELECTED[j] == 'Y') {
    	digitalWrite(4, HIGH);
        delay(500);
      	tone(PIEZO, 392);
    	digitalWrite(4, LOW);
      	delay(250);
      	noTone(PIEZO);
    }
    else if(SELECTED[j] == 'B') {
    	digitalWrite(5, HIGH);
        delay(500);
      	tone(PIEZO, 493);
    	digitalWrite(5, LOW);
      	delay(250);
      	noTone(PIEZO);
    }
  } 
   delay(1000);
}
```
