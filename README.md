# Data-Mining-Project

### 당뇨병 진단 예측 모델

<br/>


## 1. 개요
#### [프로젝트 주제 및 주제 선정 배경]
+ 식생활 패턴의 서구화, 운동량 감소, 사회의 복잡성 등으로 인하여 당뇨환자가 꾸준히 증가, 따라서 이에 따른 당뇨병 진단 모델을 구축해보고자 함

![image](https://github.com/jiseong99/Data-Mining-Project/assets/137580822/611c5d77-fbcd-4d75-91cd-ab675247549a)
![image](https://github.com/jiseong99/Data-Mining-Project/assets/137580822/b9477df0-cdf8-471f-b3ad-0ea55881d3f2)

<br/>

  
## 2. 데이터 처리
### 활용 데이터 확인 및 시각화
![image](https://github.com/jiseong99/Data-Mining-Project/assets/137580822/25334d3b-5a57-43f1-9c9e-1b8593403126)
![image](https://github.com/jiseong99/Data-Mining-Project/assets/137580822/3ad2aa9f-fc47-45d9-9bdc-dc8ba6c47a93)


<br/>


### 데이터 스케일링 / StandardScaler
![image](https://github.com/jiseong99/Data-Mining-Project/assets/137580822/d2258d6f-eca1-4c16-b8c1-5a89f74f3ac0)

+ StandardScaler를 활용, 수치형 변수들 스케일링 진행


<br/>

### 상관관계 확인 / Correlation Matrix
![image](https://github.com/jiseong99/Data-Mining-Project/assets/137580822/e611efc0-f4a2-46d8-94d3-df2aca4c2471)


+ 상관관계가 0.1 미만인 Bloodpressure, SkinThickness 컬럼 제거
+ 
<br/>

### 다중공선성 확인
![image](https://github.com/jiseong99/Data-Mining-Project/assets/137580822/f6a964e3-8c52-45ec-b751-10105aef7248)

+ 분류 모델은 대체적으로 다중공선성에 민감하지 않지만 Logistic Regression 과 같은 모델의 경우 다중공선성에 영향을 받을 수 있으므로
+ VIF(분산팽창지수)를 확인, VIF가 10이 넘으면 다중공선성의 증거가 됨

<br/>

## 3. 모델 학습

+ Logistic Regression, K-nearest Neighbors, Support Vector Machine, Decision Tree Classifier, RandomForest Classifier
+ 총 5가지 모델에 대해서 학습

  ![image](https://github.com/jiseong99/Data-Mining-Project/assets/137580822/dc7e60fc-73c8-4f40-af5b-c3e41e3c3edc)

+ 성능이 가장 좋았던 모델은 Logistic Regression

<br/>

## 4. 파라미터 튜닝

+ Optuna를 활용해서 파라미터 튜닝을 진행
  
![image](https://github.com/jiseong99/Data-Mining-Project/assets/137580822/fa2195bf-c014-4a9d-a61f-04835193fe0c)


![image](https://github.com/jiseong99/Data-Mining-Project/assets/137580822/675888d3-3820-4e99-8da9-cf528cff6f35)

+ 최종 결과
+ Train Accuracy : 약 0.7830
+ Test Accuracy : 약 0.7396


