## Summary 

1983년 5월부터 2008년 12월까지의 지구의 평균적인 대기 질 및 기후 관련 데이터가 포함된 데이터셋에서 세계의 평균 기온을 예측하기 위한 모델 만들기

### 변수의 상관관계 시각화 
![image](https://user-images.githubusercontent.com/87505072/130894735-3c439afd-ecb0-4712-a1b3-bae73bf3c1fe.png)

CO2, CH4, N2O, CFC.12 등의 feature 변수들이 Target 변수인 Temp와 강한 양의 상관관계 갖고, 이들 feature 변수들끼리도 매우 높은 상관관계 

### linear regression model 수립 
![image](https://user-images.githubusercontent.com/87505072/130895650-51183a49-ca60-4c07-8851-2e906a70559a.png)

#### Temp 변수에 영향 크게 미치는 feature 변수 
![image](https://user-images.githubusercontent.com/87505072/130895729-fbe65b39-27d7-488e-8c42-3e4ba31a873f.png)

#### 8개 feature 대상으로 cross validation 활용한 stepwise variable selection
>Forward Stepwise Selection

![image](https://user-images.githubusercontent.com/87505072/130903286-1f35ebdf-63a9-47a1-acd8-deabe624c829.png)

>Backward Stepwise Selection 

![image](https://user-images.githubusercontent.com/87505072/130903322-bd1ee7f4-014d-4195-83c5-27f649017a84.png)


## Conclusion
forward selection으로 선택한 변수의 coefficent 

![image](https://user-images.githubusercontent.com/87505072/130905679-ed21d5c9-57fa-4580-af92-1697192f927c.png)
