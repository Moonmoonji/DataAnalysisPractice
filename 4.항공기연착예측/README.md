## Summary 1

2004년 1월동안 Washington DC 지역으로부터 New York City로 운행한 2201개의 항공기 운행 기록 데이터로부터 항공기 연착(delay)여부 예측 

*README는 데이터 분석 내용에 대해 간락하게만 정리한 것으로 구체적인 코드는 Rmd 파일 또는 html 파일 참고*

### 변수들 간의 상관관계 시각화 
![image](https://user-images.githubusercontent.com/87505072/130908642-4476aac2-3525-4f87-bb39-3507f0bec5d6.png)

feature들간에 상관관계가 높지 않아 feature들 사이의 multicolinearity는 낮을 것임. 

### Baseline model

weather 변수가 Bad 일 경우 항공기 연착, weather OK일 경우 항공기 연착되지 않는 것으로 예측하는 모델 
![image](https://user-images.githubusercontent.com/87505072/130909527-529fc722-440f-41b8-bd7d-4bc0ae47db42.png)

Baseline 모델에 대한 confusion matrix 

### Logistic regression model 

모든 feature를 포함한 logistic regression model 

#### > threshold = 0.2
![image](https://user-images.githubusercontent.com/87505072/130909831-68879de6-d3e0-4502-ba33-6af67b9f2089.png)

#### > threshold = 0.3
![image](https://user-images.githubusercontent.com/87505072/130909870-6504c827-bc4c-4595-a3f6-c92b2a7b74f2.png)

#### > threshold = 0.5
![image](https://user-images.githubusercontent.com/87505072/130909918-1ffb5a20-a66b-4c28-91ef-97ff208bf5be.png)

#### > threshold = 0.7
![image](https://user-images.githubusercontent.com/87505072/130909954-b4d74d77-4af0-4ce7-803e-f61d610ccb86.png)


### Backward stepwise selection 적용한 logistic regression model 

#### > threshold = 0.5
![image](https://user-images.githubusercontent.com/87505072/130910131-114af82e-7483-49d5-95c7-a1bb66ef44e0.png)

### Lasso regression 적용한 logistic regression model 
![image](https://user-images.githubusercontent.com/87505072/130910192-452d475e-dd59-4cce-abe7-8a211db7f33e.png)

#### > threshold = 0.5
![image](https://user-images.githubusercontent.com/87505072/130910245-ca4be849-c69c-4d2f-9a44-8475bcc8b661.png)

## Conclusion 
### logistic regression model들의 test set에 대한 성능 나타내는 ROC Curve 

![image](https://user-images.githubusercontent.com/87505072/130910692-8dee11b6-e50e-4cdd-9259-fad0bdfe5afe.png)

Darkred : 기본 logistic regression model 

Darkblue : backward stepwise selection 적용한 logistic regression model 

Darkgreen : lasso regression 적용한 logistic regression model 

## Summary 2

Citrus Hiil과 Minute Maid Orange juice 구매한 1070명 고객 정보 포함된 데이터에서 feature Purchase의 두가지 factor 중 어떤것을 구매할지 예측하는 모델 (SVM 사용) 

### linear kernel SVM 
![image](https://user-images.githubusercontent.com/87505072/130911809-23e0204a-3dc6-494f-9f98-54efb0c0f688.png)

### RBF kernel SVM 
![image](https://user-images.githubusercontent.com/87505072/130911968-77f99d52-51e4-4d64-89eb-1e34b9235cdc.png)
![image](https://user-images.githubusercontent.com/87505072/130911999-ffe174ea-e73f-48ca-958a-a49e5640a756.png)

### polynomial kernel SVM 
![image](https://user-images.githubusercontent.com/87505072/130912060-cb0fd9bd-2eb0-4153-b7e3-8773d80465ff.png)

## Conclusion
세가지 kernel에 대해서 parameter tuning을 진행한 결과 linear kernel이 cost가 0.01일때 가장 좋은 성능을 보임 
![image](https://user-images.githubusercontent.com/87505072/130912625-b370203a-0c71-45cf-82ca-5c6fd495d7d7.png)

