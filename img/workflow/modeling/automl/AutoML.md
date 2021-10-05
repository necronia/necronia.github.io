---
sidebar_position: 1
---

# AutoML
데이터를 등록하고 최적의 파라미터로 수행가능한 모델을 찾을 수 있습니다. 각 experiment은 가용자원 한도 안에서 수행됩니다.

지도학습 방법 - 분류, 예측

## AutoML 생성
워크플로우 작업 선택에서 AutoML로 바로가기를 선택한 후 '다음' 버튼을 클릭하여 워크플로우를 생성합니다.
![](/img/workflow/modeling/automl/automl-01.png)

## 데이터 가져오기
가져올 데이터를 선택하여 추가하면 Wrangler 노드에서 데이터를 확인할 수 있습니다.   
건너뛰기 혹은 완료를 클릭하면 AutoML 노드가 준비됩니다.
![](/img/workflow/modeling/automl/automl-02.png)

## AutoML 설정 및 실행
### AutoML 실행
AutoML 노드를 선택하여 우측 패널에서 실행 버튼을 클릭하여 AutoML을 실행합니다.
![](/img/workflow/modeling/automl/automl-03.png)

분석 기법(분류, 회귀), 타깃, 지표를 선택한 후 실행하기 버튼을 클릭합니다.
![](/img/workflow/modeling/automl/automl-04.png)

### AutoML 설정
AutoML 노드를 마우스 우클릭하여 automl 노드 옵션에서 AutoML 설정하기를 클릭합니다.
![](/img/workflow/modeling/automl/automl-05-1.png)
* AutoML 설정
   + 기본 설정
   + 학습옵션 선택
   + 분할 (Optional)
   + 샘플링 (Optional)
   + 고급 설정 (Optional)
   + 리더보드

#### 기본 설정
![](/img/workflow/modeling/automl/automl-05-2.png)
* 분석 기법
   + 분류
   + 회귀
* 타깃
* 지표

#### 학습옵션 선택
![](/img/workflow/modeling/automl/automl-05-3.png)
* Data Columns 탭을 선택한 후 사용할 컬럼을 체크할 수 있습니다.
* 데이터 타입
   + OBJECT
   + INT64
   + FLOAT64
   + DATETIME64
   + TEXT
* 결측치 대체
   + NONE
   + DROP
   + MOST_FREQUENT
   + UNKNOWN
* 변형
   + NONE
   + LOG
   + SQUARED_ROOT
   + SQUARE
   + BOX_COX_TRANSFORMATION
   + YEO_JOHNSON_TRANSFORMATION
   + ADD_LAGS
* 이상치 제거

#### 분할 (Optional)
![](/img/workflow/modeling/automl/automl-05-4.png)
* Resampling Strategy
   + Holdout
   + CV
* Split Ratio
* Test 사용

#### 샘플링 (Optional)
![](/img/workflow/modeling/automl/automl-05-5.png)
* Sampling
* Sampling Target
   + ALL
   + TRAIN
* Sampling Size
* Balancer

#### 고급 설정 (Optional)
![](/img/workflow/modeling/automl/automl-05-6.png)
* Time Out (sec)
* Early Stopping
* Each Evaluation Timeout (sec)
* Use Ensemble Builder
* Include Estimators
   + logistic_regression
   + bernoulli_nb
   + adaboost
   + decision_tree
   + extra_trees
   + gradient_boosting
   + hist_gradient_boosting
   + k_nearest_neighbor
   + lda
   + liblinear_svc
   + libsvm_svc
   + nusvc
   + mlp
   + multinomial_nb
   + passive_aggressive
   + qda
   + random_forest
   + sgd
   + xgboost
   + lightgbm
   + catboost
   + autodl
* One Hot Encoding
   + includeOneHotEncoding
* Variance Threshold
   + includeVarianceThreshold
* Scaling
   + standardize
   + minmax
   + normalize
* Feature Engineering
   + SelectPercentile
   + SelectKBest
   + SelectFwe
   + Boruta
   + FastICA
   + FeatureAgglomeration
   + Polynomial
   + PCA
   + Nystroem

#### 리더보드
![](/img/workflow/modeling/automl/automl-05-7.png)
AutoML 진행상태(진행중, 완료)와 Score Trend를 확인할 수 있습니다.

## AutoML 진행
![](/img/workflow/modeling/automl/automl-06.png)
* AutoML 노드를 클릭하여 우측 패널을 열면 진행상태(진행중, 완료)와 Score Trend를 확인할 수 있습니다.
* 중지 버튼을 클릭하여 AutoML을 중지할 수 있습니다.

## AutoML 완료
![](/img/workflow/modeling/automl/automl-07.png)
AutoML이 완료되면 모델 노드가 추가됩니다.

![](/img/workflow/modeling/automl/automl-08.png)
모델 노드가 추가되어 AutoML 작업이 완료되었습니다.

## AutoML 노드 옵션
![](/img/workflow/modeling/automl/automl-09.png)
AutoML 노드를 마우스 우클릭하면 automl 노드 옵션이 나타납니다.
1. AutoML 설정하기
   + AutoML 결과와 설정을 조회하는 화면으로 이동합니다.
2. 이름 바꾸기
   + 노드 이름을 변경할 수 있습니다.
3. 즐겨찾기에 추가
   + 우측 패널의 즐겨찾기에 AutoML 노드를 추가합니다. 
4. 즐겨찾기 삭제
   + 우측 패널의 즐겨찾기에서 AutoML 노드를 삭제합니다.
5. 삭제
   + AutoML 노드를 삭제합니다.

## AutoML 상세 보기
AutoML 노드를 마우스 더블 클릭 또는 우클릭 하여 automl 노드 옵션에서 AutoML 설정하기를 선택합니다.

### Data Preview
![](/img/workflow/modeling/automl/automl-10-1.png)

### Data Columns
![](/img/workflow/modeling/automl/automl-10-2.png)

### EDA
![](/img/workflow/modeling/automl/automl-10-3.png)

#### Plot 생성하기
* Plot 생성하기를 클릭하고 Plot을 선택하여 생성할 수 있습니다.
![](/img/workflow/modeling/automl/automl-10-4.png)

![](/img/workflow/modeling/automl/automl-10-5.png)
* Available Plots
   + CORELATION MATRIX
      - Example
      ![](/img/workflow/modeling/automl/automl-10-6.png)
   + PAIR PLOT
   + VARIABLE ANALYSIS (ALL COLUMNS)
   + VARIABLE ANALYSYS (TARGET)
   + PARALLEL COORDINATES
      - Example
      ![](/img/workflow/modeling/automl/automl-10-7.png)
   + PARALLEL COORDINATES (parcate)

### Leaderboard
각각의 모델 정보를 확인할 수 있으며, 배포 버튼을 클릭하여 모델을 배포할 수 있습니다.
![](/img/workflow/modeling/automl/automl-10-8.png)

모델을 배포하면 AutoML 노드에 모델 노드가 생성됩니다.
![](/img/workflow/modeling/automl/automl-11.png)

## 모델 노드
AutoML이 완료된 후 모델 노드가 생성됩니다.
![](/img/workflow/modeling/automl/automl-13.png)
1. 모델 노드
   * AutoML이 완료된 후 생성된 모델 노드입니다.
2. 모델 노드 옵션
   * 모델 레지스트리 등록
      + 새 모델 등록
         ![](/img/workflow/modeling/labelling/labelling-11.png)
         - AI Runtime에 새 모델을 등록합니다.
         - 등록할 모델이름 입력하고 중복확인 후 확인을 클릭하여 새 모델을 등록합니다.
      + 새 버전으로 등록
         ![](/img/workflow/modeling/labelling/labelling-12.png)
         - AI Runtime에 배포된 모델이 있을 경우 해당 모델의 새 버전으로 모델을 등록할 수 있습니다.
         - 배포된 모델 중 하나를 선택한 후 확인을 클릭하여 새 버전으로 모델을 등록합니다.
   * 이름 바꾸기
      + 모델 노드의 이름을 변경합니다.
   * 삭제
      + 모델 노드를 삭제합니다.
3. 에측용 Workflow 생성
   * 현재 워크플로우 이름에 Predict prefix를 붙여서 예측용 워크플로우를 생성합니다.

## 예측용 Workflow
워크플로우 목록에서 예측용 워크플로우 선택하여 불러옵니다.

1. 데이터 가져오기를 클릭하여 가져올 데이터를 선택합니다.
![](/img/workflow/modeling/automl/automl-14.png)

2. 데이터 가져오기가 완료된 후 모델 노드를 선택하고 우측 패널에서 예측 버튼을 클릭합니다.
![](/img/workflow/modeling/automl/automl-15.png)

3. 예측 완료 후 예측 결과 데이터 노드가 생성됩니다.
![](/img/workflow/modeling/automl/automl-16.png)












