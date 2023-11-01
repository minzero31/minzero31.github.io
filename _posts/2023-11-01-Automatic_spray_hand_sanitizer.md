---
layout: single
title: "자동분사 손소독제 개발 프로젝트"
---

[사용 언어]
- 아두이노

[하드웨어]

사용 부품

- 아두이노 우노보드
- 3D 모델링 부품 (fusion 360) 사용
- 초음파 센서 (HC-SR04)
- 서보모터 (Tower Pro MG995)
  
구조 설명
- 하드보드지와 3D 모델링 부품으로 지지대를 만들었으며 손소독제 펌프 윗부분에 고정함.
- 구멍을 뚫어서 손소독제 펌프 아래에 손을 가져다 대면, 초음파 센서가 이를 인식해 서보모터가 작동하여 펌프가 되도록 구상함.

![image](/assets/images/auto_hand_seni1.png)
![image](/assets/images/auto_hand_seni2.png)
![image](/assets/images/auto_hand_seni3.png)
![image](/assets/images/auto_hand_seni4.png)
![image](/assets/images/auto_hand_seni5.png)
![image](/assets/images/auto_hand_seni6.png)
  
[소프트웨어 코드]
사용한 아두이노 라이브러리
- DHT라이브러리
- Liquid Crystal 라이브러리
  
소스코드
~~~ C

#include <DHT.h>
#include <Wire.h>
#include <LiquidCrystal_I2C.h>
#define DHTPIN 7
#define DHTTYPE DHT11

LiquidCrystal_I2C lcd(0x27, 16,2);
DHT dht(DHTPIN, DHTTYPE);
void setup()
{
  lcd.init()
  Serial.begin(9600);
  dht.begin();
}
void loop() {
  int h = 54;
  int t = 26;

  Serial.print("humidity: ");
  Serial.print(h);
  Serial.println(" %");
  Serial.print("temperature : ");
  Serial.print(t);
  Serial.println(" 도");

  lcd.backlight();
  lcd.displat();
  lcd.print("TEMP:           ");
  lcd.print(t);
  lcd.setCursor(0,1);
  lcd.print("HUMIDITY:       ");
  lcd.print(h);
  delay(1000);
}
  

   
~~~
