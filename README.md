# 🎯 얼굴형 분류 모델
한국인 얼굴형 분석을 통한 개인맞춤 스타일링 개발

## 📊프로젝트 PPT 링크
발표용 슬라이드: https://docs.google.com/presentation/d/1vIqPWrA0r6WLZFZF5KLfhbBrjCoYsIqt5f61jaT4Pg/edit#slide=id.g22d6093be98_0_0

## ✨ 프로젝트 소개
![image](https://user-images.githubusercontent.com/119157378/231558640-67dd5bff-2836-4eb2-906d-754a59a6270c.png)


 *딥러닝 모델을 활용해 한국인 얼굴형의 특징을 학습하여, 분류하는 모델을 설계. 나아가 퍼스널 스타일링에 활용할 수 있는 결과물을 지향*

-----------------------------------------------------------------------------------------------------------------------------
### 데이터의 나이대 별 얼굴형 분포 그래프 
![image](https://user-images.githubusercontent.com/119157378/231559788-c34c5eb8-7c36-41c2-ad19-23bf428190c1.png)




## ✨ 프로젝트 과정
#### **1.전처리**

  - JSON 파일에서 필요 feature 추출
  - 용량문제로 전 데이터 사이즈 조정
  - 이미지 정규화

#### **2. CNN 모델 사용**
  
  - Optimizer : ADAM
  - Loss : Categorical_crossentropy
  - Metrics : Accuracy 
  - Training Set Acc : 약 54%   /  Test Set ACC : 약 48% 
    
    
    ![image](https://user-images.githubusercontent.com/119157378/231561368-6b460ea3-6274-4145-aba7-cee44089d4f2.png)



#### **3. ResNet으로 전이학습**

  - Optimizer : SGD
  - Loss : CrossEntropyLoss
  - Metrics : Accuracy 
  - Training Set Acc : 약 56%   /  Test Set ACC : 약 54% 

![image](https://user-images.githubusercontent.com/119157378/231562576-c1df4526-63a2-4680-a11d-9aca790003b6.png)

#### **4. 결과**

  - 이미지 데이터셋 자체에 얼굴형을 분류할때 얼굴의 너비, 길이같은 객관적 수치가 필요할것으로 보임.
  - 긴형, 사각형의 오답률이 높았으며, 계란형과 둥근형으로 분산・분류되었다. 
  - 마름모형과 역삼각형은 결과가 0으로 나왔으나, 이는 데이터 수의 부족이 원인으로 보인다.
  - 둥근형의 경우 정답률이 비교적 높음.
  - 사각형의 경우에는 둥근형을 예측하는 비율이 매우 높음



## 📜 기술 스택
![image](https://user-images.githubusercontent.com/119157378/231568042-ec93f76d-50be-406c-a16e-b5136861e018.png)

![image](https://user-images.githubusercontent.com/119157378/231568094-ee5d7da4-700b-43f6-83d9-80a43af21c5b.png)
