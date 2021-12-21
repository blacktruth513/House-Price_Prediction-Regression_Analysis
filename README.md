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

## 4. 프로젝트 분석 방법 

모델링을 위한 불필요 변수 제거, 데이터에 포함된 한자 제거, 화폐 단위 통일, 데이터의 이상값 제거 등의 전처리를 수행하고 통계분석을 실시하여 특성 변수(독립 변수) 간 상관 관계 분석을 통한 다중 공산성을 확인한다. 이후, 베이스 라인 모델(기준 모델) 설정하여 기준 모델을 통해 프로젝트의 최종 모델을 선정한다. 모델링 과정에서는 랜덤 포레스트, 다중선형회귀모델, 라쏘 회귀모델, 릿지 회귀모델, GradientBoosting 모델, AdaBoost 모델, XGBoost 모델의 베이스 모델링을 통해, 모델 학습 간 모델 성능 지표로 MAE, RMSE, R^2 Score를 사용하여 하이퍼파라미터 튜닝을 진행할 최종 모델을 선정한다. 그리고 하이퍼파라미터 튜닝한 최종 선정된 모델을 통해 테스트 데이터를 통하여 모델 성능을 평가한다.  

## 5. 프로젝트 결과 분석 

교차검증을 통한 하이퍼파라미터 튜닝을 진행한 GradientBoosting 모델을 최종 모델로 선정한 결과, 검증 데이터셋의 MAE는 47.54924681807521, RMSE는 64.33990907362772, R^2 Score는 0.8837223296474156의 값이 각각 나왔으며, 최종적으로 테스트데이터에 적용한 결과, MAE는 102.45717046954115, RMSE는 122.09552862680415, R^2 Score는 0.6209109086870994의 값을 도출했다. 또한, 최종 모델에 대한 특성 변수의 중요도를 시각화한 결과, 타겟 변수에 가장 큰 영향력을 행사한 특성 변수는 'communityAverage', 'square' 순이었다.  


