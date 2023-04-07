<img src="https://github.com/bloblog/Card_AnomalyDetection/blob/main/img/card_main.png?raw=true">

### <p align='center'> 💳 신용카드 사기 거래 탐지 AI 경진대회 참여작</p>

<br>

## 프로젝트 기간
2023.03.05 ~ 2023.03.19

<br>

## 프로젝트 정의
- 사기 거래를 감지하는 ai 솔루션 개발
- 주어진 데이터를 통해 이상 거래를 탐지하는 분석 모델 개발

<br>

## 분석 과정

1️. 데이터 탐색 및 EDA  

- feature 개수
- 이상치, 정상 데이터 각 feature 분포

<br>

2️. Feature Engineering

 (분포 기반) feature 선택* / 전체 feature / PCA* 비교  
  
    *feature 선택 → 이상치와 정상 데이터가 육안으로 확연하게 구분 가능한 특성 선택  
    *PCA → 특성 개수에 따른 설명력을 살펴보고, 최종 25개로 선정

<br>

3️. 모델 성능 비교 

- 이상치 탐지 모델 공부 및 비교
- KNN, EllipticEnvelope, IsolationForest, MissForest, LOF, VAE, kernel PCA 등

<br>

4️. 최종 모델 선정  

`EllipticEnvelope` 모델 선정

<br>

### 모델 선정 기준

- 데이터셋 특성에 잘 맞고 성능이 좋으며, 너무 느리거나 복잡하지 않은 **모델 3개**를 1차적으로 선정
    -  `EllipticEnvelope`, `IsolationForest`, `AutoEncoder`
- 세 모델을 단독으로도, 모든 경우의 수로 앙상블 역시 진행하여 `f1 score` 측정
    - 각자 모델에 대해 feature engineering 진행
    - 팀원들의 결과를 확인하고, 코드를 조합하여 마지막으로 평가 후 모델 선정
- 단독으로 사용하여도 `f1 score`가 확연히 높은 `EllipticEnvelope` 모델이 최종 선정됨.

<br>

## 최종 제출 코드 및 결과

### 제출 코드
[Google Colaboratory 링크](https://colab.research.google.com/drive/1ZDJL-SKoV8s2Xb-7GYa9vZWFtqaPv1MT#scrollTo=zvfSS0Obi3ea)

### 사용 모델 및 특성
`elliptic envelope` - 모든 feature 사용

### 최종 점수
192위 / public 점수 0.928 🎉

<br>
