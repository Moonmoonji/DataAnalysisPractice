## Summary 1

MNIST 데이터셋에서 숫자 분류하는 image classification model 만들어 보기 (Decision Tree 사용) 

#### > cost complexity parameter alpha=0, leaf node가 가지는 최소 데이터수가 50인 Tree
![image](https://user-images.githubusercontent.com/87505072/130914627-d8432420-73eb-49d1-9aee-01f0303f5830.png)

---

#### > cost complexity parameter alpha=0, depth가 최대 3인 tree 
![image](https://user-images.githubusercontent.com/87505072/130914692-6421b346-8ce3-4de6-81f1-9f2c59222820.png)

---

#### > cross validation 활용한 pruning

cross validation 결과 시각화 

![image](https://user-images.githubusercontent.com/87505072/130914812-dfcd5b98-31bc-4ca4-91aa-f032c5f1d8d6.png)

best cp 값일 때의 tree 시각화 

![image](https://user-images.githubusercontent.com/87505072/130915027-4814011b-3ee0-41e2-9289-8ae838709fe7.png)


## Conclusion
pruning 후 얻은 tree로 test set에 대한 예측 수행하고 confusion matrix 계산 
![image](https://user-images.githubusercontent.com/87505072/130915254-35868fd2-7c6a-45b7-a161-e16fcae35f5f.png)

## Summary 2

MNIST 데이터셋에서 숫자 분류하는 image classification model 만들어 보기 (randomForest 사용) 

#### > bagging model 

##### tree 개수 증가에 따른 OOB classification error rate 
![image](https://user-images.githubusercontent.com/87505072/130915765-4687ddcd-49de-45e8-9ea3-1afb285d4e34.png)

#### > random forest model 

##### tree 개수 증가에 따른 OOB classification error rate
![image](https://user-images.githubusercontent.com/87505072/130915890-a8f69bbd-5dc1-408c-9b22-ed14864c755b.png)

## Conclusion 

#### bagging model 
![image](https://user-images.githubusercontent.com/87505072/130916631-065532aa-dd9c-403d-a804-a0acad60e5f6.png)

#### random forest model
![image](https://user-images.githubusercontent.com/87505072/130916668-236dd982-5749-4042-962b-8237e593650f.png)
