## Summary 

트위터에서 미국의 6개 항공사를 언급하는 트윗 14640개에 대한 정보가 들어있는 데이터셋에서 텍스트의 positive/negative/neutral 여부를 판별하는 모델을 만들기 

### wordcloud 생성

#### > negative
![image](https://user-images.githubusercontent.com/87505072/131079573-7d13db4e-5946-47e6-a3ab-4abd521df4b3.png)

#### > neutral
![image](https://user-images.githubusercontent.com/87505072/131079593-347d2ad5-640a-4dc2-8aa3-dfe329f2fc77.png)

#### > positive 
![image](https://user-images.githubusercontent.com/87505072/131079611-813e8153-c997-418f-bff1-7be1605a402b.png)

--- 

### Preprocessing 

#### > create corpus 
![image](https://user-images.githubusercontent.com/87505072/131079788-6da7418e-c938-4abb-a634-52c7bcceb6c3.png)

#### > 대문자 소문자로 전환 
![image](https://user-images.githubusercontent.com/87505072/131079892-f8fad4dc-efb4-433c-b5fb-fd0ffce8f396.png)

#### > 숫자 제거
![image](https://user-images.githubusercontent.com/87505072/131079907-6b951fd3-f7f0-443d-82d7-5534ea10f11f.png)

#### > stopword제거 
![image](https://user-images.githubusercontent.com/87505072/131079930-adb8b7ef-b993-4815-81ff-473572f39ad1.png)

#### > 문장부호 제거 
![image](https://user-images.githubusercontent.com/87505072/131079951-1ce1bbe2-184d-4963-b6db-05aa4753af31.png)

#### > 단어들의 어미 제거 (stemming) 
![image](https://user-images.githubusercontent.com/87505072/131079970-44189bc9-853c-44a9-bd75-4433bec6efd5.png)

#### > 공백 제거 
![image](https://user-images.githubusercontent.com/87505072/131079997-5136f152-629b-4434-90e3-caad4a1c1aa2.png)

---

### Predictive model 만들기 

#### DTM 사용한 predictive model 

전체 document 중에 0.5% 미만의 document에서 발생하는 단어는 제외하도록 preprocessing 
![image](https://user-images.githubusercontent.com/87505072/131080256-f3a83a8f-c585-42d1-97cb-cb78106fd23b.png)

### 모델 활용 

#### > k-NN algorithm 
![image](https://user-images.githubusercontent.com/87505072/131080573-cbc8bf66-42da-43e7-be7f-4f71cc3e6793.png)

#### > logistic regression algorithm 
![image](https://user-images.githubusercontent.com/87505072/131080528-ddd4d88e-1b21-4056-b352-d1fda32090a3.png)


#### > svm algorithm 
![image](https://user-images.githubusercontent.com/87505072/131080463-ef9126ed-fd3c-4960-9df0-67e93b5259e8.png)


#### > random forest algorithm 
![image](https://user-images.githubusercontent.com/87505072/131080495-a649a632-e4e9-4fa7-89ca-fcf7061b1ac3.png)

## Conclusion
random forest algorithm이 가장 성능 우수 
