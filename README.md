# 전공종합설계 프로젝트

## 주제선정 및 배경

:bulb:**서울특별시 강남구 전기차 급속충전소 최적입지 선정**

![tree](https://news.unist.ac.kr/kor/wp-content/uploads/2020/11/%EB%B2%84%EC%A0%84-B.png)

* 정부의 전기차 보조금 확대, 현대자동차의 2030년 이내로 내연기관 생산 중단 등 전기차 시장은 빠른 성장에 비해 급속충전소 공급이 부족한 상황 

* 전기차 보급의 핵심 요소인 급속충전소 인프라는 실제 소비자의 전기차 구입 시 가장 큰 고려사항으로 자리잡음 

* 강남구의 전기차 충전소 현황을 파악하고, 도로상황 및주변 입지와 지리적 특성을 고려하여 전기차 급속충전소 위치 선정


## 목적

:bulb: **서울특별시 내에서 가장 혼잡한 도로가 위치한 강남구의 전기차 충전소 현황 및 최적의 입지를 선정**


## 데이터 종류 및 수집 경로


**1. 서울특별시 강남구 전기차충전소 정보**  
:link: <https://data.seoul.go.kr/dataList/OA-15007/S/1/datasetView.do>

**2. 서울특별시 강남구 공영주차장 정보**  
:link: <https://data.seoul.go.kr/dataList/OA-15012/S/1/datasetView.do>

**3. 서울특별시 강남구 도시공원 정보**  
:link: <https://data.seoul.go.kr/dataList/OA-15004/F/1/datasetView.do>

**4. 인스타그램 게시글 크롤링(트렌드 분석)**

**5. 2020년 서울특별시 주요도로 교통량조사 보고서(강남구 기준 분석)**  
:link: <https://topis.seoul.go.kr/refRoom/openRefRoom_2.do>



## 개발 환경

<div align=left> 
   <img src="https://img.shields.io/badge/python-3776AB?style=for-the-badge&logo=python&logoColor=white"> 
   <img src="https://img.shields.io/badge/jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white">
   <img src="https://img.shields.io/badge/google colab-F9AB00?style=for-the-badge&logo=google colab&logoColor=white"> 
   <br>
</div>

## 프로젝트 추진 전략

**1. 요건 정의**
- 계획수립 및 자료조사, 행정동별 전기차 및 전기차 급속충전소 현황

**2. 입지 후보 선정**
- 총 92개의 급속충전소 입지 후보를 선정
    - 공공 체육 및 여가시설
    - 강남구 소재 공원
    - 강남구 소재 공영주차장 및 학교

**3. 품질 기능 전개(QFD)**
- 전기차 급속 충전소 서비스를 제공하기 위해 소비자의 needs와 기술적 특성을 구조화
- 고객 요구속성 : 급속 충전소를 설치하기 위한 고객 요구사항
    - 휴게 시설  
    - 위치 적절성  
    - 접근 용이성  
    - 이용 무제약성  
    - 효율성  

- 기술특성 : 충전소 후보지에 영향을 미치는 요소 간 중요도 및 가중치 평가
    - 후보지가 주요 도로(교통량 많은 곳)가 근처에 있는가?
    - 후보지가 속한 동에 전기차가 많이 있는가?
    - 급속전기차 충전소가 근처에 있는가?

- HOQ(품질의 집)을 통해 충전소 후보지에 가중치를 부여
    - 가중치 = (대로변 점수 * 대로변 가중치) + (동 점수 * 동 가중치) + (충전소 인접 여부 점수 * 충전소 인접 여부 가중치)

**4. 분석 기법**
- k-means clustering
    - 주어진 데이터를 총 k개의 cluster로 군집화하여 입지 선정
- k-medoid clustering
    - 현재 선정한 후보지 외에도 충전소 입지로 적합한 장소를 찾아 가장 가까운 대표 object를 선정 

**5. 최종 위치 선정**
- k-means clustering과 k-medoid clustering을 통해 선정한 최종 위치 선정



## 프로젝트 기대효과
- 현재 위치와 k-means,k-medoid clustering을 통한 위치를 비교함으로써 급속충전소 설치를 위한 관련 종사자 및 소비자에게 전기차 급속충전소 입지에 대한 인사이트 제공










