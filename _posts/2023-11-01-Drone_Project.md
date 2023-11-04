---
layout: single
title: "드론 택배 프로젝트"
---

[사용 언어]
- 파이썬 (OpenCV 및 tellodrone 사용)

[하드웨어]

사용 부품
- 텔로드론
  
드론 비행 환경
- 드론 비행 지도 제작
- 장애물 제작
- 표지판 제작


[소프트웨어 코드]

1. 텔로드론 코딩을 위한 djitello 라이브러리 사용
2. 텔로드론 조종 메인 함수
3. 최단거리이동 기능
4. 장애물 피하기 기능(키보드 조종 기능)
5. 표지판 인식 후 동작 기능

  
소스코드

<djitello 라이브러리>
- 텔로드론 사용을 위한 라이브러리
- 텔로드론에 대한 내장 변수, 함수에 대한 정의들을 확인 할 수 있음.

[djitello.py 라이브러리](https://github.com/minzero31/minzero31.github.io/tree/e7feca0cdb98c1235eafab7137798a67a7073220/Projects/djitellopy
)

<TelloMain.py>
- 텔로드론 조종을 위한 메인 함수

<script src="https://gist.github.com/minzero31/8322e36dc6499d11c991668661af012b.js"></script>

<최단거리이동 기능 구현>
- 다익스트라 알고리즘 활용
- 사전에 제작한 드론 지도를 기반으로 정보를 넣어서 최단거리를 계산함.
- 출발지와 도착지를 선택하면 그에 따른 최단 경로로 드론이 이동할 수 있음.

<script
src="https://gist.github.com/minzero31/b22d2725d8b0f61c11fe576ba70801ee.js"></script>

<키보드 조종 기능>
- 키보드의 방향키/알파벳키를 이용해 드론의 움직임을 조종할 수 있음.
- 드론의 특성에 따라 여러 번 테스 트 후 속도 및 방향 유지 수준을 조종함.

<script src="https://gist.github.com/minzero31/e9ad1ac826a4c0c939d4511cf4c65d56.js"></script>

<장애물 피하기 기능>
- 키보드 조종 기능을 활용해 장애물을 피한다.
- 텔로드론에 내장된 카메라 모듈을 이용해 컴퓨터 화면에서 텔로 드론의 운행 화면을 확인할 수 있음.
- 실시간으로 송출되는 영상을 확인하여 키보드 조종으로 장애물을 적절하게 회피할 수 있음.

<script src="https://gist.github.com/minzero31/bf309463282397309cde0a2bb9c36625.js"></script>

<표지판 인식 기능>
- 구글의 Teachable Machine을 활용함.
- Teachable Machine을 파이썬에서 활용하기 위해 tensorflow의 keras 모델을 활용함.
- Up(이륙), Down(착륙), Turn(방향회전) 세 가지의 표지판을 학습시켜 이에 따른 동작을 하도록 함.

<script src="https://gist.github.com/minzero31/c017d3bf74190b638386b2a5edb97670.js"></script>


[참고 자료]
Teachable Machine 활용하기 (<https://doljokilab.tistory.com/27>)
다익스트라 알고리즘 (<https://brownbears.tistory.com/554>)
Drone Programming with Python Course (<https://www.youtube.com/watch?v=LmEcyQnfpDA&t=6566s>) 





