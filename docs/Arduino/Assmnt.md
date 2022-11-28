<h3 style="font-size:5vw; text-align:left" > Arduino Projects</h3>

### Frist program 

 #### LCD control by Push button

> Project requirements

1- LCD Display  16*2 <br>
2- Arduino board Uno <br>
3- Female or Male Connection <br>
4- Push Button  <br>

``` Arduino
#include <LiquidCrystal.h>
const int rs = 12, en = 11, d4 = 5, d5 = 4, d6 = 3, d7 = 2;
LiquidCrystal lcd(rs, en, d4, d5, d6, d7);

void setup() 
{
  lcd.begin(16, 2);
  lcd.print("team-4,ZJU");
  lcd.setCursor(0,1);
  lcd.print("Mohammed22251414");
  delay(1000);
}

void loop() 
{
  for (int i=0;i<15;i++) 
  { 
    lcd.scrollDisplayLeft();
    delay(150);
  }
  
  for (int j=0;j<34;j++)
  {
    lcd.scrollDisplayRight();
    delay(150);
  }
  
  delay(1000);

} 

```
#### Output

### Second program 

```Arduino
#include <LiquidCrystal.h>
#define pb 7
#define gnd 8
const int rs = 12, en = 11, d4 = 5, d5 = 4, d6 = 3, d7 = 2;
LiquidCrystal lcd(rs, en, d4, d5, d6, d7);

void setup() 
{
  lcd.begin(16, 2);
  pinMode(pb,INPUT_PULLUP);
  pinMode(gnd,OUTPUT);
  digitalWrite(gnd,LOW);
  lcd.print("Push Button"); 
}

void loop() 
{
  if(digitalRead(pb)==LOW)
  {
    lcd.setCursor(0,1);
    lcd.print("OFF ");
  }else
  {
    lcd.setCursor(0,1);
    lcd.print("ON");
  }
}
```
#### Output

### Class Work
led controll by Push Button <br>

<div class="responsive">
  <div class="gallery">
    <a target="_blank" href="img/32.jpg">
     <video width="320" height="240" poster="img/download.png" controls>
   <source src="img/arduino.mp4" type="video/mp4">
   <source src="movie.ogg" type="video/ogg">
</video>
    </a>
    <div class="desc">Led </div>
  </div>
</div>
<div class="clearfix"></div>

<br>