# 만료 및 탈퇴 회원 예측 모델

## Skills
<img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white"/>&nbsp; <!--scikitlearn-->
<img src="https://img.shields.io/badge/pandas-150458.svg?style=for-the-badge&logo=pandas&logoColor=white"/>&nbsp; <!--pandas-->
<img src="https://img.shields.io/badge/numpy-4d77cf.svg?style=for-the-badge&logo=numpy&logoColor=white"/>&nbsp; <!--numpy-->
<img src="https://img.shields.io/badge/Matplotlib-11557c.svg?style=for-the-badge&logo=Matplotlib&logoColor=white"/>&nbsp; <!--matplotlib-->

## 프로젝트 제목
**만료 및 탈퇴 회원 예측 모델 개발**

## 프로젝트 목표
회원의 상태를 "만료", "중지", "탈퇴"로 분류하여 고객 이탈을 조기 예측하는 머신러닝 모델을 개발하여 기업의 고객 유지 전략에 기여

## 사용한 데이터 셋
- **데이터**: 천재교육 서비스의 회원 데이터(`만료및탈퇴회원.csv`)
- **구성**: 만료, 중지, 탈퇴 상태를 포함한 회원의 활동 데이터를 기반으로 머신러닝 예측 모델을 학습

## 워크플로우

1. 패키지 임포트
- 사용한 주요 패키지: pandas, seaborn, numpy, matplotlib, scikit-learn, imblearn
2. 데이터 로드 및 요약
- 데이터를 로드하고 데이터프레임의 형태와 컬럼을 확인하여 데이터 구조를 파악
3. 데이터 전처리
- 결측값을 확인하고, 새로운 feature(`residual_point`)를 생성하여 추가
4. 스케일링 및 변수 변환
- `MinMaxScaler`를 사용해 데이터를 0과 1 사이로 스케일링하고 로그, 제곱근 변환을 통해 데이터 분포를 정규화
5. 오버샘플링을 통한 클래스 불균형 해결
- SMOTE(Synthetic Minority Over-sampling Technique)를 사용하여 소수 클래스의 데이터를 증강
6. 모델 학습
- 소프트맥스 회귀 모델을 사용하여 다중 클래스 분류 수행
7. 성능 평가 및 시각화
- Confusion Matrix, ROC 커브, AUC 점수를 통해 모델의 성능을 평가하고, 이를 시각화하여 비교

## 프로젝트 결과

### 구현 기능
- 데이터 전처리 및 변환을 통해 모델의 성능을 최적화
- 클래스 불균형 문제를 해결하여 모델이 모든 클래스에 대해 균등하게 학습할 수 있도록 개선
- 머신러닝 모델을 학습하고, 다양한 지표로 성능을 평가하여 최적의 모델을 선정

## 트러블 슈팅

- **오류**: ValueError - 데이터 형태 불일치로 발생한 `shapes (n,1) and (m,) not aligned` 오류
- **해결 방법**: `.reshape(-1, 1)`을 통해 데이터 차원을 맞춰 오류 해결

## 프로젝트를 통해 얻은 역량

- 데이터 전처리와 불균형 해결
- 데이터의 다양한 특성에 따라 최적의 모델을 선택
- 모델 성능 평가 및 지표 분석 능력 향상, 다양한 지표를 통해 모델 성능을 비교 및 개선
