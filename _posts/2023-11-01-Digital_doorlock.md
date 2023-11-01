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

![image](/assets/images/doorlock1.png)
![image](/assets/images/doorlock2.png)
![image](/assets/images/doorlock3.png)

[소프트웨어 코드]

사용한 아두이노 라이브러리
- MFRC522 라이브러리 : SPI 통신을 이용해 RFID 카드나 태그를 읽고 쓰도록 하는 기능 포함.
  라이브러리 속 'ReadNUD' 예제 : 사전에 디지털 도어락의 카드키로 사용할 RFID태그의 코드를 찾아 등록해두어야 함. 
- Servo 라이브러리 : 서보모터 사용을 위한 라이브러리.
  
소스코드

<script src="https://gist.github.com/minzero31/6b60325c2abdb4d468dbabc7e7943ed7.js"></script>

