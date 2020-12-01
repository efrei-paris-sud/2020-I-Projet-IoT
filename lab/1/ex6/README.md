

# Exercise 3
In this exersise we use a buzzer. The purpose is turn it on with a duration and a frequency tone of our choice.
## Schematic 
![Test Image](photo.png?raw=true)

## Code
``` 

const int buzzer = 5; 


void setup(){
 
  pinMode(buzzer, OUTPUT); 

}

void loop(){
 
  tone(buzzer, 400, 2000); 
  delay(1000);        
  noTone(buzzer);     
  delay(1000);        
  
} 

``` 
## Board Image

## Issues
no issues
