# Industrial-Temperature-Controller
###### Designed and simulated an Industrial Temperature Controller using Arduino UNO in Tinkercad, integrating multiple temperature sensors for real-time monitoring and automatic control. The system displays live readings on a 16x2 LCD and uses LED indicators to signal safe, warning, and critical temperature levels. This project demonstrates practical applications of embedded systems in industrial automation, ensuring process stability, equipment protection, and operational efficiency.
---
## Here is the references...

Circuit Connections in TINKERCAD :-

<img src=https://github.com/lingeshkumarkamaraj/Industrial-Temperature-Controller/blob/main/1.png> 
<img src=https://github.com/lingeshkumarkamaraj/Industrial-Temperature-Controller/blob/main/2.png> 
<img src=https://github.com/lingeshkumarkamaraj/Industrial-Temperature-Controller/blob/main/3.png> 
<img src=https://github.com/lingeshkumarkamaraj/Industrial-Temperature-Controller/blob/main/4.png> 
<img src=https://github.com/lingeshkumarkamaraj/Industrial-Temperature-Controller/blob/main/5.png> 
<img src=https://github.com/lingeshkumarkamaraj/Industrial-Temperature-Controller/blob/main/6.png> 

Working :- 

[<img width="300" height="300" src="https://img.icons8.com/color/96/start.png" alt="video"/>](https://youtu.be/55fJPhewIIs)


---
Code :-
```

#include<LiquidCrystal.h>
LiquidCrystal lcd(10,9,7,6,5,4);
void setup()
{
  pinMode(13, OUTPUT);
  pinMode(12, OUTPUT);
  pinMode(11, OUTPUT);
  pinMode(A0, INPUT);
  pinMode(A1, INPUT);
  pinMode(A2, INPUT);
  lcd.begin(16,2);
  lcd.clear();
}

void loop()
{
  int a,b,c;
  a = analogRead(A0);
  b = analogRead(A1);
  c = analogRead(A2);
  
  lcd.clear();
  if(a>=150)
  {
    digitalWrite(13,LOW);
    
    lcd.print(" ");
    lcd.setCursor(0,0);
    lcd.print("   1-Temp LOW ");
    lcd.setCursor(0,1);
    lcd.print("   Exhaust OFF");
    lcd.print(" ");
    delay(1500);
  }
  else
  {
    digitalWrite(13,HIGH);
    
    lcd.print(" ");
    lcd.setCursor(0,0);
    lcd.print("   1-Temp High");
    lcd.setCursor(0,1);
    lcd.print("   Exhaust ON");
    lcd.print(" ");
    delay(1500);
  }
  
  if(b>=150)
  {
    digitalWrite(12,LOW);
    
    lcd.print(" ");
    lcd.setCursor(0,0);
    lcd.print("   2-Temp LOW ");
    lcd.setCursor(0,1);
    lcd.print("   Exhaust OFF");
    lcd.print(" ");
    delay(1500);
  }
  else
  {
    digitalWrite(12,HIGH);
    
    lcd.print(" ");
    lcd.setCursor(0,0);
    lcd.print("   2-Temp High");
    lcd.setCursor(0,1);
    lcd.print("   Exhaust ON");
    lcd.print(" ");
    delay(1500);
  }
  
  if(c>=150)
  {
    digitalWrite(11,LOW);
    
    lcd.print(" ");
    lcd.setCursor(0,0);
    lcd.print("   3-Temp LOW ");
    lcd.setCursor(0,1);
    lcd.print("   Exhaust OFF");
    lcd.print(" ");
    delay(1500);
  }
  else
  {
    digitalWrite(11,HIGH);
    
    lcd.print(" ");
    lcd.setCursor(0,0);
    lcd.print("   3-Temp High");
    lcd.setCursor(0,1);
    lcd.print("   Exhaust ON");
    lcd.print(" ");
    delay(1500);
  }
  lcd.clear();
}

```
---
[TINKERCAD LINK](https://www.tinkercad.com/things/l1dyAhNWw9D-brilliant-tumelo-fyyran?sharecode=CTTdvnqBQ6AR4y3v7g-YXnTUR5CllQ3wQt5452dm3aE)
---
