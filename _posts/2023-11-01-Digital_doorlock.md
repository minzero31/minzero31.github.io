---
layout: single
title: "디지털 도어락 제작 프로젝트"
---

[사용 언어]
- 아두이노

[하드웨어]

사용 부품
- 아두이노 우노보드
- 서보모터
- RFID 모듈

구조 설명
- RFID 모듈에 지정된 태그를 가져다 대면, 서보모터가 작동해 도어락이 열리는 형태로 제작.
- 우드락을 사용해 집 구조를 제작하고, 서보모터의 날개에 문을 달아 도어락이 열리도록 제작함.
- 사전에 디지털 도어락의 카드키로 사용할 RFID태그의 코드를 찾아 등록해두어야 함. 
  
[소프트웨어 코드]

사용한 아두이노 라이브러리
- MFRC522 라이브러리 : SPI 통신을 이용해 RFID 카드나 태그를 읽고 쓰도록 하는 기능 포함.
  라이브러리 속 'ReadNUD' 예제 : 사전에 디지털 도어락의 카드키로 사용할 RFID태그의 코드를 찾아 등록해두어야 함. 
- Servo 라이브러리 : 서보모터 사용을 위한 라이브러리.
  
소스코드
~~~ arduino

#include <SPI.h>  // SPI 통신을 사용하기 위한 라이브러리 헤더파일
#include <MFRC522.h> //FRID 사용
#include <Servo.h> // 서보모터 사용

const int RST_PIN = 9; #디지털 핀 번호 지정
const int SS_PIN = 10;

MFRC522 mfrc522(SS_PIN, RST_PIN);   // MFRC522 인스턴스

byte CardUidByte[4] = {0xB7, 0x42, 0xA6, 0x7A}; // 사용할 엑세스 카드의 고유번호
boolean state = false; // 서보모터 초기 상태값

Servo servo;
const int SERVO_PIN = 8; // 서보모터 핀 번호 지정

void setup() {
  Serial.begin(9600);  
  while (!Serial);     
  SPI.begin();         //SPI 통신 시작
  mfrc522.PCD_Init();  //MFRC522 초기화
  servo.attach(SERVO_PIN);
  servo.write(0); // 서보모터 원위치
  delay(50); 
}

void loop() {
  // 새 카드 확인
  if ( ! mfrc522.PICC_IsNewCardPresent()) return; 

  // 카드 읽기
  if ( ! mfrc522.PICC_ReadCardSerial()) return; 

  //읽은 카드의 고유 번호와 등록된 고유 번호가 일치하는 확인하기
  if (mfrc522.uid.uidByte[0] == CardUidByte[0] && mfrc522.uid.uidByte[1] == CardUidByte[1] &&
        mfrc522.uid.uidByte[2] == CardUidByte[2] && mfrc522.uid.uidByte[3] == CardUidByte[3] ){
   
         state=!state;    
                 
         if(state == true){
           Serial.println("Open");
           servo.write(90); //출입문 열기(90도 회전)
           delay(3000); //3초 대기
           servo.write(0);  //출입문 닫기(원위치로 회전)
          }
         delay(2000);
   }  
}
  

   
~~~
