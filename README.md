# 2020 금융 페스티벌 
# 보험금 청구건 분류 분야
## EDA 및 모델링 파일

성능 - public 88.059로 1등으로 마무리

EDA를 통해 모델 선택에 있어 기본적 선택의 기준을 얻을 수 있었음

실제로 경험기반의 모델과 규칙기반의 모델을 적절히 가중평균 한 값이 가장 좋았음. 

경험기반의 모델을 위해서 KNN을 사용하였고 
규칙기반 모델을 위해서 ExtraTree를 사용하였다.

이때 Extra Tree의 경우 Random성과 과적합의 위험이 높았기 때문에 Random_state를 다르게 설정한 모델 3개를 기하평균을 하여 모델의 안정성을 높였다.

## 사용한 패키지와 버전

* Pandas -- 0.25.1
* Numpy -- 1.16.5
* Matplotlib -- 3.1.1
* Seaborn -- 0.11.0
* Sklearn -- 0.23.1
