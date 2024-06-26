---
layout: single
title: "도서관 QR코드 패스 인식기 개발 프로젝트"
---

[사용 언어]
- 파이썬

[해당 프로젝트 사용 포스터]


![image](/assets/images/qrrecog1.png)

[개발 목적]

코로나19 당시 특정나이 이상부터 개인정보 패스(QR코드)가 발급되었음.  
하지만 발급되지 않는 어린이, 청소년들이 주로 사용하는 이음터(복합문화센터와 비슷한 장소) 도서관에서는 수기로 명부를 작성해야 하는 불편함이 있었음.   
또한 제대로 기록되지 않았음.  
코로나 바이러스 확진 시 동선 파악 및 n차 감염자를 확인하기 위해 개인 QR코드를 학생들을 대상으로 발급하고 이를 통해 출입 기록을 할 수 있도록 하는 프로그램을 개발하게 되었음.

[소프트웨어 코드]

사용 모듈, 라이브러리
- pandas
- time
- datetime
- getpass
- csv
- os

코드 설명
- 프로그램이 초기에 실행되면 오늘날짜를 이름으로 csv파일을 생성함. 속성값은 방문시간, 이름, 주소, 연락처가 되고 만약 이미 오늘날짜의 csv파일이 있다면 중복해서 생성하지 않음.
- QR코드를 찍게 되면 사용자의 이름, 주소, 전화번호 정보가 순서대로 프로그램으로 전달됨.
- 전달받은 정보를 출입시간(QR코드가 찍힌시간)과 함께 오늘날짜 csv 파일에 추가함.



소스코드

QrRecog.py

<script src="https://gist.github.com/minzero31/ad726a93d760f1031a4234c94a3d3875.js"></script>
