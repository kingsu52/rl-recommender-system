# RL 기반 개인화 추천 시스템 (RL Recommender System)
본 프로젝트는 COIL2000 고객 데이터를 기반으로 고객 특성에 맞는 상품을 추천하기 위한  
강화학습(Reinforcement Learning) 기반 추천 환경을 구축하고,  
DQN, Double DQN, CQL 알고리즘을 적용하여 추천 정책의 성능을 비교·분석하는 것을 목표로 한다.

## 1. 프로젝트 개요
본 연구는 COIL2000 고객 데이터를 기반으로 고객 상태(State), 행동(Action), 보상(Reward)을 정의하여  
강화학습 기반 추천 환경을 구성한다.  
여러 RL 알고리즘을 동일 조건에서 학습시켜 정책의 안정성, 보수성, 추천 성능을 평가하며,  
고객 특성에 맞춘 맞춤형 상품 추천 정책을 도출하는 것을 목표로 한다.

## 2. 프로젝트 목표
- COIL2000 데이터를 활용한 강화학습 기반 추천 환경 구축  
- 고객 특성에 따른 맞춤형 상품 추천 정책 학습  
- DQN, Double DQN, CQL 알고리즘의 성능 비교  
- 보수적 Q-learning(CQL)을 통한 안정적 추천 정책 도출  
- 실제 서비스 시나리오에 적용 가능한 정책 탐색

## 3. 저장소 구조 
```
rl-recommender-system/
 ├── main.ipynb                # 환경 구성, 학습, 평가가 포함된 전체 코드
 ├── presentation/             # 발표 자료(PPT)
 │    └── rl_recommender_presentation.pptx
 └── README.md
```

## 4. 실행 방법 (Google Colab 기준) 
### (1) Colab에서 main.ipynb 열기 
### (2) 런타임 설정 
- 런타임 → 런타임 유형 변경 → GPU 선택(선택 사항) 
### (3) 필요한 라이브러리 설치 
```bash 
!pip install numpy pandas scikit-learn torch 
```
### (4) Google Drive 마운트 및 데이터 불러오기 
COIL2000 데이터는 Google Drive에 저장되어 있으며, Colab에서 아래와 같이 Drive를 마운트하여 불러온다. 
```
from google.colab 
import drive drive.mount('/content/drive') 
```
예시 데이터 경로 
```
base_path = './gdrive/MyDrive/Colab Notebooks/COIL2000/data.csv'
```
### (5) 셀을 순서대로 실행 데이터 로딩 → 환경 구성 → 모델 학습 → 평가 순으로 진행된다. 

## 5. 구현 알고리즘
```
DQN 
Double DQN
CQL (Conservative Q-Learning) 
```
## 6. 평가 지표 
평균 보상 추천 비율 Q-value 안정성 알고리즘 간 성능 비교 
## 7. 데이터 파일 관련 안내 
COIL2000 데이터는 용량 및 저작권 문제로 인해 저장소에 포함되어 있지 않으며, Google Drive에 업로드된 파일을 Colab에서 마운트하여 사용한다.

