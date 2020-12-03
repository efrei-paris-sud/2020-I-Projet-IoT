

# Exercise 7
In this exersise we play with a RGB LED. We want the LED color to change at least seven times to the colors of our choice.
We will use the analogWrite function to control the color of the LED.
## Schematic 


## Code
``` 

const int redPin = 11;
const int greenPin = 10;
const int bluePin = 9;

void setup() {
  Serial.begin(9600);

  pinMode(redPin, OUTPUT);
  pinMode(greenPin, OUTPUT);
  pinMode(bluePin, OUTPUT);
   
}

void loop() {


  setColor(150, 200, 0);
    delay(1000);  
  setColor(80, 150, 50);
    delay(1000);  
  setColor(90, 70, 100);
    delay(1000);  
  setColor(130, 160, 40);
    delay(1000);  
  setColor(70, 20, 0);
    delay(1000);  
  setColor(200, 200, 0);
    delay(1000);  
  setColor(50, 200, 200);
    delay(1000);  
  
}

void setColor (int red,int green, int blue) {
  analogWrite(redPin,red);
  analogWrite(greenPin,green);
  analogWrite(bluePin,blue);
}

``` 
## Board Image

## Issues
no issues
