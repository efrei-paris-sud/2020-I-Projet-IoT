

# Exercise 3
We had to turn on a LED using a button. Therefore it lights when we push the button and it stops when we release.
## Schematic 
![Test Image](photo.png?raw=true)

## Code
``` 

// set pin numbers:
const int buttonPin = 2;     // the number of the pushbutton pin
const int ledPin =  6;      // the number of the LED pin
// variables will change:
int buttonState = 0;         // variable for reading the pushbutton status
void setup() {
  Serial.begin(9600);
  // initialize the LED pin as an output:
  pinMode(ledPin, OUTPUT);
  // initialize the pushbutton pin as an input:
  pinMode(buttonPin, INPUT);
}
void loop() {
  // read the state of the pushbutton value:
  buttonState = digitalRead(buttonPin);
  // Show the state of pushbutton on serial monitor
  Serial.println(buttonState);
  // check if the pushbutton is pressed.
  // if it is, the buttonState is HIGH:
  if (buttonState == HIGH) {
    // turn LED on:
    digitalWrite(ledPin, HIGH);
  } else {
    // turn LED off:
    digitalWrite(ledPin, LOW);
  }
  // Added the delay so that we can see the output of button
  delay(100);
}
``` 
## Board Image

## Issues
no issues
