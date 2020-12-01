

# Exercise 3
Using a potentiometer we want to change the blinking velocity of the LED by varying the value between 0 and 255.
## Schematic 
![Test Image](photo.png?raw=true)

## Code
``` 

const int buttonPin = 2;     // the number of the pushbutton pin
const int ledPin =  6;      // the number of the LED pin
const int analog_ip = A0;

// variables will change:
int inputVal = 0;         // variable for reading the pushbutton status

void setup() {
  Serial.begin(9600);
  // initialize the LED pin as an output:
  pinMode(ledPin, OUTPUT);

}
void loop() {
  
  inputVal = analogRead(analog_ip);
  
  digitalWrite(6, HIGH);
  
  delay(inputVal/4);
  //we turn off the led
  digitalWrite(6, LOW);
  //we wait 2s
  delay(inputVal/4);

``` 
## Board Image

## Issues
no issues
