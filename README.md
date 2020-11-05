2020-02 서강대학교 캡스톤디자인1

# 오늘의 자리
#### 학생들이 열람실에 헛걸음하지 않도록 돕는 프로젝트
+ 열람실 좌석 획득 가능성 예측
+ 열람실 만석 시 빈자리 발생 예측
+ 자리 경쟁 현황 안내 및 경쟁에서 이기는 방법 제안

***
### 팀 Smart-Catcher 소개
|이름|소속|역할|
|------|---|---|
|이준하|서강대학교 컴퓨터공학과| |
|하민주|서강대학교 컴퓨터공학과|프론트엔드|
|최기용|서강대학교 컴퓨터공학과|DB, 서버|

***
### 프로젝트 개요
* ##### 어떤 문제를 풀고자 하는가?
열람실에 친구가 이미 가 있으면 열람실 분위기가 어떤지, 자리가 얼마나 빨리 차고 있는지, 지금 출발하면 자리를 잡을 수 있을지, 만석이지만 곧 자리가 날 것 같다던지 하는 것들을 물어서 알 수 있다. 하지만 열람실에 친구가 없는 '고독한 학생'은 그러한 정보를 알 수 없다. 직접 가봐야만 하기 때문에 헛걸음을 할 위험이 있다.

* ##### 어떻게 풀 것인가?
지금 가면 자리를 잡을 수 있을지, 만석이라면 언제쯤 나에게 차례가 돌아올지, 몇 명과 자리 경쟁을 하고 있는지를 알려주어 사용자의 효율적 선택을 돕는다.

* ##### 문제를 풀면 좋은가?
가보지 않고서는 모르는 열람실의 상황을 알 수 있기에 '고독한 학생'의 헛걸음, 시간 낭비를 줄일 수 있다.

***
### 기술 시스템
##### [Abstract Structure Map]
![image](https://user-images.githubusercontent.com/26410791/98261935-5aaadf00-1fc8-11eb-9639-3814cdb05ac6.png)

##### [Detail]
1. 정보 수집
    * J&K 열람실 : 로욜라 도서관 자리 정보 API를 활용하여 실시간 자리 정보를 얻어온다.
    * 서가 열람실(생각하는 숲) & 만레사존 : 적외선 센서로 실시간 출입 정보를 수집한다.
2. 정보 가공 및 결론 도출
<br/>

|Tool|Detail|
|------|---|
|센서|적외선 센서 (거리 감지 센서, 거리 측정 센서, 장애물 회피 센서 시도 예정)|
|서버| |
|데이터베이스| |
  
* 지금 가면 자리를 잡을 수 있을지 : 
<br/> (열람실까지 도달하는 시간을 고려하기 위해)나의 현재 위치, 빈 좌석 수, 좌석 발권 주기, 시험 기간 여부 등을 고려하는 머신러닝 결과를 도출
* 만석이라면 언제쯤 나에게 차례가 돌아올지 :
<br/> 좌석 발권 주기, 시험 기간 여부, 들락날락 횟수 등을 고려하는 머신러닝 결과를 도출
* 몇 명과 자리 경쟁을 하고 있는지 : 
<br/> 시스템을 통해 자리 정보를 확인한 사용자들을 카운트하고 위치 정보를 사용하여 자리 경쟁에서 이기려면 몇 분 안에 도착해야 하는지를 계산

3. 정보 제공
	* 웹으로 제공
	* 단순 정보 제공에서 나아가 자리 획득이라는 목표를 위해 취해야 할 행동을 추천

***
### 경쟁 우위 요소
* 학생 편의
사업성보다는 공공성을 가진 서비스이다.
학생들의 편의를 위해 학교에서 충분히 제공할 가치가 있다고 생각한다.
