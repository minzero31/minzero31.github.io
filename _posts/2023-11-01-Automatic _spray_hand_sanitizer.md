---
layout: single
title: "자동분사 손소독제 개발 프로젝트"
---

[사용 언어]
- 아두이노

[하드웨어]
사용 부품
- 아두이노 우노보드
- 온습도 측정센서
- LCD보드
구조 설명
- 온습도 센서를 통해 온습도를 측정할 수 있음.
- 측정된 온습도 수치가 LCD판에 출력되며, 이를 확인하기 위해 투명한 아크릴 판을 사용하여 제작함.
  
[소프트웨어 코드]
사용한 아두이노 라이브러리
- DHT라이브러리
- Liquid Crystal 라이브러리
  
소스코드
~~~ arduino

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
~~~
