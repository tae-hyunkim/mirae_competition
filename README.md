# 2020 금융 페스티벌 
# 보험금 청구건 분류 분야
 보험금을 고객들이 청구할 때 해당 정보를 바탕으로 자동지급, 심사, 조사에 대하여 알고리즘을 통해 판단하는 모델을 만드는 대회 
 기본적으로 주어진 데이터는 비식별화 된 고객의 청구에 대한 자료와 해당 청구에 대한 자동지급, 심사, 조사에 대한 분류표 
 Unknown값을 가진 자료가 존재하며 다양한 값을 범주화 시켜 데이터를 제공 
 
## EDA 및 모델링 파일
올려준 ipynb 파일에 존재

### EDA를 위해 사용한 패키지
* matplotlib
* seaborn
### 분석을 위해 사용한 패키지 
* pandas
* numpy
* sklearn

## 결과 
성능 - public 88.059로 1등으로 마무리

EDA를 통해 모델 선택에 있어 기본적 선택의 기준을 얻을 수 있었음

모델 구축에 있어 다양한 모델을 고려하였고 각각의 모델에서 우리는 경험기반의 모델과 규칙기반의 모델의 앙상블을 활용하기로 함 

경험기반의 모델을 위해서 KNN을 사용

규칙기반 모델을 위해서 ExtraTree를 사용

* Extra Tree의 경우 Random성과 과적합의 위험이 높았기 때문에 Random_state를 다르게 설정한 모델 3개를 기하평균을 하여 모델의 안정성을 높였다.
* 만들어진 Predict_proba와 KNN의 Predict_proba값을 가져와 가중평균을 진행하며 마무리

# 최종 활용 서비스 제안 
식별화 데이터를 활용한 고객 군집화 서비스 제안 
* 질병 관리 군집
* 자산 정보 군집
* 소비 성향 군집

군집 정보를 활용하여 모델에 고객 유형별 정보 추가 삽입 효과 기대

위험 탐지 신호등의 기능을 활용해 자동지급에 대한 군집별 정보를 추가적으로 제공함으로써 자동지급에 대해 이상치를 탐지하고자 함 조사로 분류된 결과에 대해서도 특별조사로 분류하기 위한 기준의 요건으로 활용할 수 있을 것으로 예상됨

군집의 특징을 활용해 보험상품을 추천하는데 필요한 내용을 보장질병, 보험상품, 필요자금으로 분리하고 각 군집별 정보를 활용해 개인화된 추천서비스를 제공하고자 하였다. 
## 사용한 패키지와 버전

* Pandas -- 0.25.1
* Numpy -- 1.16.5
* Matplotlib -- 3.1.1
* Seaborn -- 0.11.0
* Sklearn -- 0.23.1
