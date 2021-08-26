### Summary 

k-NN을 활용하여 새로운 고객의 정보가 주어졌을 때 이 고객이 개인 대출 상품을 가입할 지를 예측 

#### > 5-NN
![image](https://user-images.githubusercontent.com/87505072/130892475-34cc22a1-964b-45c8-a913-604983e985a6.png)

#### > validation set 지정됐을 때 k-NN 적용
![image](https://user-images.githubusercontent.com/87505072/130893388-e4dcc548-4db9-4de8-a9e1-cc5ad56291b9.png)

k=1 일때 accuracy 가장 높지만 일반적으로 k=1 자주 사용하지 않기 때문에 k=5 일때 accuracy 인정

#### > 5-fold cross validation 5회 반복. 가장 성 능 좋은 k 값 찾기 
![image](https://user-images.githubusercontent.com/87505072/130893538-4e179f24-a40c-425e-b55c-61cd0edb1b1b.png)

k=3 일때 accuracy 가장 높음 

![image](https://user-images.githubusercontent.com/87505072/130893588-9a0ce5c4-a9df-4abb-9808-3d070eb52ca7.png)

모델에 적용 

### Concolusion

#### Accuracy 비교

5NN : 0.962

validation set 지정되어 있을 때 : 0.95xx

5-fold cross validation 5회 반복 : 0.967 
