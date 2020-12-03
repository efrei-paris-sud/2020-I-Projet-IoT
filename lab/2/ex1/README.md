

# Exercise 1 
We had to develop an arduino program which can read a byte from serial and adjust the passive buzzer frequency with that

## Schematic 
![Test Image](photo.png?raw=true)

## Code
 ```void setup() {
  Serial.begin(9600); // initialize serial:
}

void loop() {
  // if there's any data available, read it:
  while (Serial.available() > 0) {

    int i  = Serial.parseInt();    // look for the next valid integer in the incoming serial stream:
    byte b = Serial.read();    // look for the next valid byte in the incoming serial stream:

    tone(5, b, 50000); 
    delay(1000);        
    noTone(b);     
    delay(1000); 
  }
}
```
  
## Board Image


To make a gif you can use [ezgif](https://ezgif.com/maker).
## Issues
no issues.
