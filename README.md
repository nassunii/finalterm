# OSS_finalterm_20223507

  
## Configuration Information

### 1. What you do in your project

#### training data를 통해 algorithm을 학습시키고 parameter조정을 통해 test data의 정확도를 높였다.

### 2. Explain the training dataset
#### 여러가지 뇌종양 있는 세포들과 표본 뇌 데이터들

### 3. Explain the algorithm you choose
#### SVC, KNN, ExtraTreeClassifier
  
    SVC는 Classification에 사용되는 SVM 모델을 의미하며, 분류에 사용되는 지도학습 머신러닝 모델이다.
    Support vectors를 사용해서 decision boundary를 정의하고, 분류되지 않은 점을 해당 decision boundary와 비교해서 분류한다. 
    퍼셉트론 기반의 모형에 가장 안정적인 결정 경계를 찾기 위해 제한 조건을 추가한 모형이다. 
    데이터가 선형인 경우에는 잘 작동하지만, 데이터가 비선형인 경우에는 잘 작동하지 않을 수 있다. 
    Gamma변수와 c변수를 조절하여 튜닝이 이루어진다.
    
    KNN은 새로운 데이터가 들어오면 데이터 베이스에 저장되어 있는 학습 데이터와 비교하여 가장 거리가 가까운(유사도가 높은)
    k의 데이터로 예측 또는 분류를 수행한다. 별도의 모델을 학습하지 않기 때문에 lazy learning이라고 부른다.
    K가 작으면 over fitting되기 쉽고, 너무 크면 under fitting의 위험이 있다.
    
    ExtraTreeClassifier은 decision tree를 랜덤하게 만들고 그 랜덤 decision tree들의 숲을 만든 뒤 
    각 decision tree의 예측을 평균내어 최종 예측을 만든다. Random forest와 비슷하지만, 각 decision tree의 훈련데이터는 
    전체 훈련 세트이고, 트리의 node를 무작위로 분할한다는 특징이 있다. 이는 계산 속도가 빠르고, 
    하나의 decision tree만 생각하면 score가 낮아질 수 있지만 결국 decision트리의 앙상블이므로 
    score가 보완되고 결과적으론 과대적합을 막는다.

### 4. parameter
      n_neighbors : 갯수가 많아지면 결정 경계가 단순해진다.
      c : 각 포인트의 중요도를 제한하는 매개변수로, 해당값이 커질수록 결정경계가 데이터에 정확하게 맞춰진다. 
      (작을수록 과대적합을 방지함)
      
      gamma : 하나의 훈련 샘플이 미치는 영향의 범위를 결정한다. 
      클수록 정확해지지만 경사가 급해지면서 과대적합이 될 수 있다. (작을수록 과대적합 방지)
      
      n_estimators : 생성할 의사결정 나무 개수이다.

## Contact information
#### Yeseon Hong
#### ghddptjs@cau.ac.kr
