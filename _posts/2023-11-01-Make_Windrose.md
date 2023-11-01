---
layout: single
title: "파이썬으로 수원관측소의 2021년 바람장미 그리기"
---

[사용 언어]
- 파이썬
- 구글 코랩 사용



[개발 목적]

코로나19 당시 특정나이 이상부터 개인정보 패스(QR코드)가 발급되었음.
하지만 발급되지 않는 어린이, 청소년들이 주로 사용하는 이음터(복합문화센터와 비슷한 장소) 도서관에서는 수기로 명부를 작성해야 하는 불편함이 있었음. 또한 제대로 기록되지 않았음.
코로나 바이러스 확진 시 동선 파악 및 n차 감염자를 확인하기 위해 개인 QR코드를 학생들을 대상으로 발급하고 이를 통해 출입 기록을 할 수 있도록 하는 프로그램을 개발하게 되었음.


[바람장미]

바람장미란
- 바람장미 :  각 방위별 풍향 출현 빈도를 방사 모양의 그래프에 나타낸 것 / 특정 지점에서 나타나는 풍속과 풍향의 일반적인 특징을 시각적으로 간결하게 표현한 것
- 그 지역의 바람 특성을 이해할 때, 또는 바람기후학에서 매우 유용함.
- 대부분의 바람장미는 특정 방향과 풍속에 대해서 높은 빈도가 나타나는 형태임.

바람장미 해석하기
- 출현 빈도 : 그래프에서 선의 길이(중심에서부터의 거리) 
- 풍향(바람이 불어오는 방향) : 선이 그려지는 방향 
- 풍속(바람의 세기) : 그래프에 나타나는 색
ex) Bar, Box 형태는 [ 푸른색 -> 노란색 -> 붉은색 ]으로 갈수록 풍속이 세진다. 



[파이썬으로 바람장미를 그리는 과정]

1. 구글 코랩에서 파이썬으로 바람장미를 그리기 위해 windrose 패키지 다운로드
   - windrose 패키지는 바람장미를 파이썬으로 그릴 수 있게 만들어진 패키지임.
     
2. 기상청 기상자료개방포털에서 종관기상관측 데이터를 수집함.
   - 종관기상관측자료 : 기온, 강수, 바람, 기압, 습도 등 다양한 관측 데이터를 한 달 단위로 csv 파일로 제공한다.
   - 전국의 많은 관측소 중에서 수원관측소의 2021년 8월, 11월의 자료를 수집했다.
     
3. 기상관측데이터(csv)파일을 pandas의 dataframe 형태 (표형태), 한글타입으로 변환시킴
   - csv : 데이터들을 쉼표 (,)단위로 구분한 텍스트 파일, 엑셀과 비슷하다고 볼 수 있음.
   - pandas : 데이터 처리가 용이한 파이썬 라이브러리
   - dataframe : 엑셀과 비슷한 스프레드 시트 형식의 자료구조

4. 일시 데이터를 datetime 모듈을 사용해 숫자로 변환시킴.
   - datetime 모듈 : 날짜와 시간 데이터 처리를 하는 모듈
   - 기상관측데이터가 일시별로 기록되어있기 때문에 일시를 모두 숫자로 변환해준다.

5. 바람장미 그리기
   - 바람장미를 4가지 형태로 그림. (Bar, Box, Contour-f, Contour)
   - 공통적으로 3)번에서 변환시킨 기상관측데이터 중 ‘풍속’과 ‘풍향’ 데이터를 수집해서 바람장미를 그림




[바람장미 결과 형태 비교하기]

1. 형태별 비교(3가지 형태)
   - Bar(하나의 막대형태) : 한 방향에서 나타나는 풍속의 모든 범위가 연결되어있음.
   - Box(사각형 형태) : 한 방향에서 나타나는 풍속이 범위마다 사각형으로 나뉘어져 표현됨.
   - Contour-f(채워진 등고선) : 등고선 형태로 이어져 있으며 각 등고선 사이가 채워진 형태
   - Contour(등고선 형태) : 등고선으로만 표현된 형태
![image](/assets/images/windrose1.JPG)

2. 월 별 비교(수원관측소 2021년 2월-5월-8월-11월)
   - 전체적으로 서풍이 차지하는 비율이 가장 높은 편입니다.
   - 2월과 5월을 비교해보면 형태는 비슷하지만 5월에 정서풍의 비율이 더 높습니다.
   - 4개 달 중 8월의 바람장미에서 동풍과 서풍의 비율이 가장 높게 나타납니다.
   - 색 분포(풍속)을 비교해보면, 2,5,11월은 비교적 풍속이 강한 분홍색, 보라색이 잘 보인다면 8월은 주로 풍속이 약한 파란색으로 주로 형성되어있습니다.
![image](/assets/images/windrose2.JPG)

3. 바람장미는 matplotlib에서 제공하는 colormap을 이용해 다양한 색으로 표현할 수 있다.
   - matplotlib : 파이썬에서 데이터를 시각화 하는데 사용되는 라이브러리
![image](/assets/images/windrose3.JPG)




[소프트웨어 코드]

구글 코랩 링크 
https://colab.research.google.com/drive/1ys0k1LW5p3z6N0WoHQru1IOO_DFHOwmi?usp=sharing


사용 모듈, 라이브러리


코드 설명


소스코드

수원관측소에서의 2021년 8월을 예시로 코드를 작성함. 

1. 바람장미 표현을 위한 windrose 패키지 다운로드
<script src="https://gist.github.com/minzero31/6f4f120e251a3f1651b8af9ac84b6bae.js"></script>

2. 바람의 풍속과 풍향 데이터를 사용하기 위해 csv파일 전처리 하고 읽기
<script src="https://gist.github.com/minzero31/6f0541fd9f7dae489163b81377c00b9d.js"></script>

3. datetime 모듈로 문자열의 일시 데이터를 실제 시간으로 변환하기
<script src="https://gist.github.com/minzero31/10c2e944ba4408ec0663182dbdef7fd0.js"></script>

4. Bar 형태의 바람장미 그리기
<script src="https://gist.github.com/minzero31/04a2f0d3c630568de4aa2b1120d9500f.js"></script>

5. Box 형태의 바람장미 그리기
<script src="https://gist.github.com/minzero31/e5e41b94b8afc21272c234bfec3b5781.js"></script>

6. Contour-f 형태의 바람장미 그리기
<script src="https://gist.github.com/minzero31/a664e035c780327262c001fb8b44fdad.js"></script>

7. Contour 형태의 바람장미 그리기
<script src="https://gist.github.com/minzero31/7126c49461c900e47373757b427496cc.js"></script>

8. Stick (막대그래프) 형태의 데이터 표현
<script src="https://gist.github.com/minzero31/d076e61433f4601f9712a8fa373ce8c9.js"></script>



[참고 문헌 및 자료]

https://windrose.readthedocs.io/en/latest/usage.html
https://matplotlib.org/stable/tutorials/colors/colormaps.html

