

# Exercise 3
we had to complete a portion of code to show temperature and humidity in the Serial Console.

## Schematic 

## Code
 ```#include<Wire.h>
#include <BMP280.h>   // include BMP280 sensor library
BMP280  bmp280;  // initialize  BMP280 library
void setup(){
    Serial.begin(9600);
    pinMode(0, OUTPUT);
  if( bmp280.begin(BMP280_I2C_ADDRESS) == 0 )// initialize the BMP280 sensor
  {  // connection error or device address wrong!
  //ToDo: Show error in LCD
  while(1);  // stay here
  }
}
void loop(){
  float temp     = bmp280.readTemperature();   // get temperature
  Serial.println(temp);
  if (temp > 25){
      digitalWrite(0, LOW);
  }
  else {
      digitalWrite(0, HIGH);
  }
  float pressure = bmp280.readPressure();      // get pressure
  float humidity = bmp280.readHumidity();      // get humidity
  Serial.println(humidity);
  float altitude= bmp.readAltitude(seaLevelPressure) // get Altitude. The generic seaLevelPressure is 1013.25. If you put the current pressure of your city, you can find the Altitude of your place!
  delay(1000);  // wait a second
}
```
  
## Board Image

## Issues
no issues.
