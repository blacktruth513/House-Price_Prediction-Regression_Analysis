# <div align="Center">BeiJing_House-Price_Prediction-Regression_Analysis </div>

## 1. 프로젝트 주제 

머신러닝 회귀 모델 기반 중국 베이징 주택 가격 예측 프로젝트 

## 2. 프로젝트 문제 정의 

베이스 모델(타겟 변수의 평균값을 기준으로 함)을 설정하고, 머신러닝 모델링을 통해 모델 성능 지표를 활용하여 타겟 변수인 주택 가격을 예측하는 회귀분석을 진행하며, 분석 간 어떠한 특성 변수가 타겟 변수에 영향력을 크게 행사했는지 추가적으로 확인한다. 

## 3. 프로젝트 데이터 

<br>
<div align="Center"><img src='https://imgur.com/CxTKWWn.png' width = '300'></div>
<br>
데이터 출처 : https://www.kaggle.com/ruiqurm/lianjia

- 캐글 출처의 리엔지아 플랫폼 기반 중국 베이징의 2011년부터 2017년까지의 약 30만 개의 값을 포함하는 주택 데이터를 사용하여 주택 가격을 예측하면서 지금까지 배운 머신러닝 내용을 적용하여 중국과 관련된 도메인 지식 확장을 추구하고자 한다.

### 데이터 세부 내용

- url: the url which fetches the data
- id: the id of transaction
- Lng: and Lat coordinates, using the BD09 protocol.
- Cid: community id
- tradeTime: the time of transaction
- DOM: active days on market.Know more in https://en.wikipedia.org/wiki/ / Days_on_market / 부동산이 매물로 시장에 나와 있는 기간
- followers: the number of people follow the transaction. / 거래 참여자 수
- totalPrice: the total price
- price: the average price by square
- square: the square of house
- livingRoom: the number of living room
- drawingRoom: the number of drawing room
- kitchen: the number of kitchen
- bathroom the number of bathroom
- floor: the height of the house. I will turn the Chinese characters to English in the next version.
- buildingType: including tower( 1 ) , bungalow( 2 )，combination of plate and tower( 3 ), plate( 4 ). / 범주형 
- constructionTime: the time of construction
- renovationCondition: including other( 1 ), rough( 2 ),Simplicity( 3 ), hardcover( 4 ) / 범주형
- buildingStructure: including unknow( 1 ), mixed( 2 ), brick and wood( 3 ), brick and concrete( 4 ),steel( 5 ) and steel-concrete composite ( 6 ). / 범주형
- ladderRatio: the proportion between number of residents on the same floor and number of elevator of ladder. It describes how many ladders a resident have on average.
- elevator have ( 1 ) or not have elevator( 0 ) / 범주형
- fiveYearsProperty: It's related to China restricted purchase of houses policy / 범주형
- Community average price / 지역 주택 평단가 가격

