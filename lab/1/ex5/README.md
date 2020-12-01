

# Exercise 3
In this exersise we will use the fading principle. Thus we want the light to shine gradually more and more.
## Schematic 
![Test Image](photo.png?raw=true)

## Code
``` 

int i=5;   

void setup() {
pinMode(i,OUTPUT);
}

void loop() {
analogWrite(i,255);
delay(500);
analogWrite(i,150);
delay(500);
analogWrite(i,50);
delay(500);
analogWrite(i,10);
delay(500);
analogWrite(i,0);
delay(500);
}

``` 
## Board Image

## Issues
no issues
