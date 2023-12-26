# MyTalkCon-with-StlyeGAN-Toonify-TalkingHead

## 목차
- 

## 프로젝트 개요
<div align="left">
 <img width="100%" src="https://github.com/tlsdmswn01/NLP_Project---Audio/blob/main/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20PPT/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20%EA%B0%9C%EC%9A%94.png?raw=true"/>  
</p>

 
 ## 최종 결과물
 <p align='left'>
 <img width="100%" src="https://github.com/tlsdmswn01/NLP_Project---Audio/blob/main/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20PPT/%EC%B5%9C%EC%A2%85%20%EA%B2%B0%EA%B3%BC%EB%AC%BC.png?raw=true"/>

</div>

</p>


## 🗂️프로젝트 소개
본 프로젝트는 성조 시각화 자료와 성조 운율 점수 제시를 통해,  
* 학습자들이 중국어 선생님 없이 자신의 성조를 스스로 피드백하고,
* 학습자들의 자가학습을 도와주는 보조자료 제작에 목표를 둡니다.

--- 

## 📃아이디어 제안 배경
 
 ### 중국어 교육의 필요성 
   - 한국의 수출입액의 1위 국가는 중국이며,
   - 한국과 중국의 무역 비중은 20%정도를 차지할 정도로 여전히 교류가 활발합니다.
   - 이를 통해 한국에서는 여전히 중국어 교육에 대한 수요를 가지고 있을 것이라 예상합니다.
   
 
 ### 중국어 비대면 교육 활성화
 - 중국어 교육의 현황은 크게 코로나 전후로 나눌 수 있는데, 
 - 코로나 이전에는 방문교육이 활성화 되었다면 코로나 이후부터는 ICT를 접목한 이러닝의 규모가 커짐으로써(KDB 미래전략 연구소에 따르면) 중국어 비대면 교육이 더욱더 활성화 되었습니다.  

## 📃중국어 구조와 성조에 대하여

 ### 중국어란?
 - 글자 하나하나가 의미를 가지는 표의문자입니다.
 - 중국어는 성조 언어로, 같은 음의 발화여도 음높이의 변화에 따라 의미가 구별됩니다.
 
### 중국어 성조 교육
- 총 4개의 성으로 구성됩니다. 한자에 따라 성조가 없는 경성도 존재합니다
- 현재 통용되고 있는 성조교육방식으로 오도제 표기법(성조의 상대적인 음의 고저를 5에서 1로 선으로 그린 도표)가 있습니다. 이는 성조 교육 시 음높이와 방향을 직관적으로 제시해 교육에 도움을 줍니다. 
 
<div align="center">
 <img width="50%" src="https://github.com/tlsdmswn01/NLP_Project---Audio/blob/main/%EC%84%B1%EC%A1%B0%20%EC%98%A4%EB%8F%84%ED%91%9C%EC%8B%9C%EB%B2%95.png?raw=true"
/>
</div>

### 성조가 중요한 이유
- 성조는 의미를 변별해주는 역할을 해줘, 성조가 다르면 어법 어휘까지 달라집니다.
- 유창한 중국어를 구사하는데 성조는 필수적인 요소입니다.
- 직관적인 예로, 같은 발음 'shi'여도 모두 서로 다른 의미를 가집니다. 

### 성조교육이 어려운 점 - 성조변화
- 성조언어에서 흔히 나타나는 현상으로, 두 개 이상의 음절을 이어서 읽을 때 성조가 변화하는 현상을 말합니다.
- 실질적인 성조 표기와 실질적인 성조의 운율이 상이합니다. 

<div align="center">
 <img width="50%" src="https://github.com/tlsdmswn01/NLP_Project---Audio/blob/main/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20PPT/%EC%84%B1%EC%A1%B0%20%EB%B3%80%ED%99%94%20%EC%96%B4%EB%A0%A4%EC%9B%80.png?raw=true"
/>
</div>


 ---
 
 ## 기존 서비스와의 차별점
 
 ### 오색중국어
 - 5가지 색깔로 성조 표현
 - 직접 녹음 및 듣기 가능
 - 하지만 알맞지 않은 성조로 중국어를 구사해도 잘했다고 피드백을 줄 정도로 성조 오류에 대한 피드백이 없습니다.

 ### Hello Chinese
 - 내가 녹음한 것에 대해 전체적인 평가 점수 피드백이 있었고,
 - 틀린부분도 빨간색으로 표시해주었습니다.
 - 하지만, 평가 점수에 반영된 것이 성조가 틀린 건지 발음이 틀린 건지 구분이 없었습니다.
 - 또한 어떤 방향으로 개선해야 되는지에 대한 피드백은 없었습니다.

---
 
## 📈성조 시각자료 제작
- 분석목표: 각 Pitch값 즉 음 높낮이 값으로 중국어 성조 시각화하는 것입니다.
- 데이터 : 총 2명의 발화자 음성 데이터
 1. 중국인의 발화음성 - AI hub (노이즈 X)
  2. 한국인의 발화음성 - 직접 녹음 (노이즈 존재, 따로 전처리 진행)
     (한 문장에 대한 -> 연습 이전, 중국어 고급자 , 연습 이후 총 3개의 한국인 음성)
### 성조 시각화 플로우 차트

<p align='center'>
<div align="left">
 <img width="100%" src="https://github.com/tlsdmswn01/NLP_Project---Audio/blob/main/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20PPT/%EC%84%B1%EC%A1%B0%20%EC%8B%9C%EA%B0%81%ED%99%94%20%ED%94%8C%EB%A1%9C%EC%9A%B0%20%EC%B0%A8%ED%8A%B8.png?raw=true"/>  
 
 - 각 발화자 음성데이터에서 Praat을 통해 Pitch 값 추출  
 - 한국인 음성 데이터 노이즈 제거
 - 각 발화자 음성 데이터 배열을 합쳐 전처리 진행(음성 시작, 끝점 통일/ 음절 길이 통일 등)
 - 성조 시각화
</div>
</p>

### 성조 시각화
<p align='left'>
<div align="left">
 <img width="32.5%" height="250" src="https://github.com/tlsdmswn01/NLP_Project---Audio/blob/main/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20PPT/%EC%84%B1%EC%A1%B0%20%EC%8B%9C%EA%B0%81%ED%99%94%202.png?raw=true"/>  
 <img width="32.5%" height="250" src="https://github.com/tlsdmswn01/NLP_Project---Audio/blob/main/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20PPT/%EC%84%B1%EC%A1%B0%20%EC%8B%9C%EA%B0%81%ED%99%94%201.png?raw=true"/> 
  <img width="32.5%" height="250" src="https://github.com/tlsdmswn01/NLP_Project---Audio/blob/main/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20PPT/%EC%84%B1%EC%A1%B0%20%EC%8B%9C%EA%B0%81%ED%99%94%203.png?raw=true"/>  
 
  - 파랑색 점선 : 중국인 발화자 음성(정답)  
  - 빨간색 점선 : 한국인 발화자 음성
  - 연습 이전 음성은 정반 가량 성조가 틀린 것을 확인할 수 있었습니다. 
  - 중국어 고급자 음성은 정답과 매우 유사하게 성조를 말했음을 확인할 수 있습니다. 
  - 연습(프로젝트 기간 발화문장 연습) 이후 음성 선의 패턴은  연습 이전 음성에 비해 정답 선의 패턴과 조금 더 유사해짐을 확인할 수 있습니다.
</div>
</p>

### 성조 시각화 기대효과  
<p align='left'>
<div align="left">
 <img width="100%" src="https://github.com/tlsdmswn01/NLP_Project---Audio/blob/main/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20PPT/%EC%84%B1%EC%A1%B0%20%EC%8B%9C%EA%B0%81%ED%99%94%20%EA%B8%B0%EB%8C%80%ED%9A%A8%EA%B3%BC.png?raw=true"/>  

 - 한국인들이 가장 어려워하는 성조 : 2성과 3성
 - 연습 이후 음성을 보아도 여전히 3성을 틀린 것을 확인 할 수 있습니다.
 - 실제 발화자 인터뷰 내용 : 시각화 자료를 보기 전까지 어떤 부분에서 성조를 잘 못 말했는지 인지하지 못했는데, 시각화를 통해 정확히 알게 되었다고 합니다.
 - 이렇듯 성조 시각화 자료는 성조를 가시적으로 보여주면서 선생님의 피드백 없이도 스스로 피드백하며 자가학습을 할 수 있게 도와주는 보조역할을 합니다.
 </div>
</p>

## 🖥️ 운율의 유창성 평가 점수  
분석목표: 중국어의 성조 유창성 점수를 예측하는 회귀모델을 만드는 것입니다.
데이터 : 한국인의 중국어 발화 음성 데이터 - AI hub (노이즈 없음)  
타겟 데이터 : 전문 평가자의 성조 평가 점수

### 데이터 분석 및 모델링 플로우 차트  
<p align='left'>
<div align="left">
 <img width="100%" src="https://github.com/tlsdmswn01/NLP_Project---Audio/blob/main/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20PPT/%EB%8D%B0%EC%9D%B4%ED%84%B0%20%EB%B6%84%EC%84%9D%20%EB%B0%8F%20%EB%AA%A8%EB%8D%B8%EB%A7%81%20%ED%94%8C%EB%A1%9C%EC%9A%B0%20%EC%B0%A8%ED%8A%B8.png?raw=true"/>  
 
 - 음성 데이터 전처리 후 음성정보 중 하나인 크로마그램을 추출하였습니다. 
 - 이후 패딩을 진행하면서 최대길이 설정에 따라 모델 성능이 달라질 수 있다고 판단하여
 데이터의 벡터길이를 고려해 600,500,550이라는 3개의 패딩데이터를 저장하였습니다.  
 - 다양한 모델들로 데이터 실험 및 성능평가를 통해 CNN+LSTM과 LSTM+Attention모델을 보다 집중적으로 모델링 하여, 성능 평가 및 테스트를 진행하였습니다. 
  </div>
</p>

 ### 분석 및 모델링 과정 
 #### 음성 데이터 전처리
 
 문제인식 : 음성 데이터 길이가 모두 달랐습니다.

 - 짤게는 3초, 길게는 70초까지 음성 데이터 길이가 다양했습니다.
 - 데이터 패딩시 음성을 자르게 되면 몇몇 음성은 초반 음성에 대한 점수로 모델이 학습할 수 있어 이로 인한 왜곡이 우려되어 10초라는 특정 시간대 이후로의 데이터는 삭제했습니다.
   (10초 이전 : 데이터가 90%이상 분포하고 있는 구간 )

#### 음성 정보 채택 및 추출

**다양한 음성 정보**  

- Mel Spectogram : 사람의 청각인지를 반영하기 위한 스펙초그램에 Mel sclae를 적용한 특징 추출 기법
  (Mel Scale : 실제 주파수 정보를 인간의 청각 구조를 반영하여 수학적으로 변환하기 위한 방법
  예- 돌고래 소리의 주파수가 매우 높아 사람이 듣지 못하는 개념을 스펙토그램에 반영한 것)
- MFCC(Mel-Frequency Cepstral Coefficients) : 사람의 청각 구조와 음색의 차이를 반영한 음성 데이터 특징 추출 기법
  (Ceptral 분석 : 배음의 구조를 파악해 음색의 차이를 구별하는 분석법 - 악기나 성대의 구조 차이에의해 발생)
- 크로마그램 : 인간 청각이 옥타브 차이가 나는 주파수를 가진 두 음을 유사음으로 인지한다는 음악이론에 기반
  (12개의 Bin으로 특징이 추출된다. - 도,도샵,레, 레샵 ~ 시 12개 음계값)

**크로마그램 채택** 

- 중국어 성조는 음절에 해당하는 소리의 높이 변동
- 중국어 성조 중 2성은 미에서 솔까지 올리면 2성이 됩니다. 이와 같이 성조는 12개의 음계와 매우 밀접한 관련이 있다고 판단해 음성데이터에서 크로마그램을 추출해 분석했습니다.

**크로마그램 추출 후 패딩 + 시각화**  

패딩

<p align='left'>
<div align="left">
 <img width="100%" src="https://github.com/tlsdmswn01/NLP_Project---Audio/blob/main/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20PPT/%ED%81%AC%EB%A1%9C%EB%A7%88%EA%B7%B8%EB%9E%A8%20%EC%B6%94%EC%B6%9C%20%ED%9B%84%20%ED%8C%A8%EB%94%A9.png?raw=true"/>  
 </div>
</p>

 시각화  
 <p align='left'>
<div align="left">
 <img width="100%" src="https://github.com/tlsdmswn01/NLP_Project---Audio/blob/main/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20PPT/%ED%81%AC%EB%A1%9C%EB%A7%88%EA%B7%B8%EB%9E%A8%20%EC%8B%9C%EA%B0%81%ED%99%94.png?raw=true"/>  

 - 크로마그램 시각자료를 보면 빨간색이 진한, 즉 크로마그램 특징이 투렷하게 추출된 음성 데이터의 점수가 높음을 확인할 수 있고, 점수가 낮을수록 크로마그램 특징이 뚜렷하지 않음을 확인할 수 있습니다.

 </div>
</p>

#### 모델링 과정 소개 및 결과
**DNN** 
결과 : 오버피팅 발생 - 문제의 복잡도에 비해 모델이 너무 단순하기 때문이라 판단했습니다.

**CNN+BILSTM**
 <p align='left'>
<div align="left">
 <img width="100%" src="https://github.com/tlsdmswn01/NLP_Project---Audio/blob/main/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20PPT/CNN+LSTM.png?raw=true"/>  
  <p align='left'>
<div align="left">
 <img width="100%" src="https://github.com/tlsdmswn01/NLP_Project---Audio/blob/main/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20PPT/CNN+LSTM%20%EA%B5%AC%EC%84%B1%EC%A0%95%EB%B3%B4.png?raw=true"/>  
 
 - 윤상혁 외 2명(2021), CNN-LSTM 모델 기반 음성 감정 인식, ACK 2021 학술발표대회 논문집 (28권 2호) 을 참고해 모델 작성하였습니다.

 <p align='left'>
<div align="left">
 <img width="100%" src="https://github.com/tlsdmswn01/NLP_Project---Audio/blob/main/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20PPT/CNN+LSTM%20%EC%84%B1%EB%8A%A5%EA%B2%B0%EA%B3%BC.png?raw=true"/>  

 - 각기 다른 패딩값을 가진 3개의 데이터로 실험을 해보았지만 큰 차이는 없었습니다.
 - 그 중에 패딩 최대길이가 500일때가 가장 MSE값이 낮아 해당 데이터로 분석을 진행하게 되었습니다.
 - 성능지표 그래프를 통해 Loss값과 MSE값 모두 한 값으로 수렴하면서 매우 낮아짐을 확인할 수 있습니다.
 </div>
</p>
  
**모델 성능 비교**  
 <p align='left'>
<div align="left">
 <img width="100%" src="https://github.com/tlsdmswn01/NLP_Project---Audio/blob/main/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20PPT/%EB%AA%A8%EB%8D%B8%20%ED%85%8C%EC%8A%A4%ED%8A%B8%20%EC%84%B1%EB%8A%A5%20%EB%B9%84%EA%B5%90.png?raw=true"/>  

 - CNN-BILSTM과 LSTM+Attention 모델의 성능지표값이 가장 좋았고, 근소하게 LSTM+ATTention의 Mse값이 더 낮음을 확인할 수 있었습니다.
 - 하지만 저희 서비스의 목적에 조금 더 부합한 모델이 CNN-BILSTM이라고 생각하고 이를 채택해 실제 데이터로 테스트 해보았습니다.
 </div>
</p>

**CNN-BILSM 실제 데이터 예측값**  
<p align='left'>
<div align="left">
 <img width="100%" src="https://github.com/tlsdmswn01/NLP_Project---Audio/blob/main/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20PPT/%EB%AA%A8%EB%8D%B8%20%ED%85%8C%EC%8A%A4%ED%8A%B8%20%EC%84%B1%EB%8A%A5%20%EB%B9%84%EA%B5%90.png?raw=true"/>  

 - 확인결과 실제값과 예측값의 결과가 매우 상이함을 확인할 수 있었습니다.
 </div>
</p>

### 모델링 한계점
1. 타겟 데이터의 주관성
   - 운율 유창성 점수는 평가기준이 있어도, 채점하는 교사의 주관이 반영됩니다.
   - 주관성으로 점수의 편차가 발생해, 절대적으로 평가점수를 신뢰하기 어렵습니다.
2. 데이터의 부족
   - 실제 값의 예측값이 3.5,3.4,3.75으로 타겟 데이터의 빈도가 높은 값으로 나와 정확한 예측을 하지 못함을 확인할 수 있었습니다.
   - 이는 데이터 부족으로 인한 문제이며 향후 데이터를 증강하고 모델을 개선하면 완화될 것이라 기대합니다.
  
### 💡 대안 모색  
 <p align='left'>
 <img width="100%" src="https://github.com/tlsdmswn01/NLP_Project---Audio/blob/main/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20PPT/%EB%8C%80%EC%95%88%EB%AA%A8%EC%83%89.png?raw=true"/>  
  </div>
</p>


## ✨ 성조 유사도 구하기 (DTW 유사도 기반)  
분석목표: 각 발화자의 Pitch값 추출 및 전처리 후 중국어 성조 유사도 구하기입니다.
데이터 : 성조 시각화에서 사용했던 동일한 데이터입니다. 


### 유사도 분석 플로우 차트

<p align='center'>
<div align="left">
 <img width="100%" src="https://github.com/tlsdmswn01/NLP_Project---Audio/blob/main/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20PPT/%EC%9C%A0%EC%82%AC%EB%8F%84%20%EB%B6%84%EC%84%9D%20%ED%94%8C%EB%A1%9C%EC%9A%B0%20%EC%B0%A8%ED%8A%B8.png?raw=true"/>  

 - 각 음성데이터에서 추출된 Pitch값을 전처리 후,
 - 유사도를 구하는 다양한 방법으로 어떤 유사도가 선생님* 평가 점수와 가장 유사한지 확인하였습니다.
 - 그 중에 코사인 유사도와 DTW유사도를 주의깊게 살펴보았습니다.
 - 두 유사도 중 선생님 평가점수 및 시각자료와 비교해 저희 서비스와 가장 부합한 DTW 유사도를 채택해 자료를 제작하였습니다.

*선생님 : 중국어 교원 자격증을 소지한자  

 </div>
</p>

### DTW 유사도란?  
- 두개의 시계열 데이터가 서로 얼마나 유사한지 비교하는 알고리즘입니다.
- 장점: 길이와 시점의 차이가 있는 시계열 데이터도 유사도를 비교할 수 있다

### Pitch 값 전처리 
- 각 발화자가 갖는 각각의 끊어져 있는 Pitch 값들을 모두 연결해 시간에 따른 Pitch값의 변화를 나타내는 시계열 데이터로 만들어주었습니다.

<p align='left'>
<div align="left">
 <img width="49%" height="250" src="https://github.com/tlsdmswn01/NLP_Project---Audio/blob/main/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20PPT/DTW%20%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98%EC%9D%84%20%EC%9C%84%ED%95%9C%20%EC%A0%84%EC%B2%98%EB%A6%AC%201.png?raw=true"/>  
 <img width="49%" height="250" src="https://github.com/tlsdmswn01/NLP_Project---Audio/blob/main/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20PPT/DTW%20%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98%EC%9D%84%20%EC%9C%84%ED%95%9C%20%EC%A0%84%EC%B2%98%EB%A6%AC%202.png?raw=true"/>  

 </div>
</p>

 
### DTW 알고리즘 

<p align='left'>
<div align="left">
 <img width="100%" src="https://github.com/tlsdmswn01/NLP_Project---Audio/blob/main/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20PPT/DTW%20%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98.png?raw=true"/>  
 </div>
</p>

### DTW 유사도 점수화  
- DTW 유사도 결과 값 : 최단 거리값
- 범위 : 0~무한
- 유사도 해석 : 결과 값이 커질수록 두 시계열 데이터의 패턴은 유사하지 않습니다.
- 코사인 유사도 결과 값과 다르게 %로 나타내기 위한 기준값이 없습니다.

  **기준값 설정 후 점수화**
  - 학습자가 이해하기 쉽게 DTW 유사도 값을 점수화하고자 했습니다.
  - 각 학국인의 중국어 발화음성을 선생님이 평가한 점수와 DTW 유사도 값의 평균값, 중앙값, 임의의 기준 100점으로 DTW 유사도 값을 점수화 해 실제 선생님 점수와 비교해보았습니다.
  - 확인 결과 100점을 기준으로 DTW 유사도 값을 역수 취해 %를 구했을 떄, 실제 선생님 점수와 가장 유사했습니다.
 
## 최종결과물 
 <p align='left'>
 <img width="100%" src="https://github.com/tlsdmswn01/NLP_Project---Audio/blob/main/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20PPT/%EC%B5%9C%EC%A2%85%20%EA%B2%B0%EA%B3%BC%EB%AC%BC.png?raw=true"/>  
  </div>
</p>

## 팀원 소개 및 역할 분담  
 <p align='left'>
 <img width="100%" src="https://github.com/tlsdmswn01/NLP_Project---Audio/blob/main/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20PPT/%ED%8C%80%EC%9B%90%20%EC%86%8C%EA%B0%9C%20%EB%B0%8F%20%EC%97%AD%ED%95%A0%EB%B6%84%EB%8B%B4.png?raw=true"/>  
  </div>
</p>

## 기대 및 자체평가 의견  

 <p align='left'>
 <img width="100%" src="https://github.com/tlsdmswn01/NLP_Project---Audio/blob/main/%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8%20PPT/%EA%B8%B0%EB%8C%80%20%EB%B0%8F%20%EC%9E%90%EC%B2%B4%ED%8F%89%EA%B0%80%EC%9D%98%EA%B2%AC.png?raw=true"/>  
  </div>
</p>

