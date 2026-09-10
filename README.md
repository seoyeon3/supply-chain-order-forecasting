# 생산 계획 최적화를 위한 부품 발주량 예측 AI 모델링

> **D-day 발주량을 3일 전에 선제적으로 예측하여 생산계획 및 재고 운영을 지원하는 AI 예측 모델**

### Project Links
- [Project Slides](https://docs.google.com/presentation/d/1ds_Sudw_N1sMcK83l8A9bmKQjOSnuN-LXFlZLXpdrhY/edit?usp=sharing)
- [LSTM & XGBoost - Python Codes](https://github.com/seoyeon3/supply-chain-order-forecasting/blob/main/LSTM_XGBoost_Python.ipynb)
- [ARIMA - R Codes](https://github.com/seoyeon3/supply-chain-order-forecasting/blob/main/ARIMA_R.ipynb)

---

## 프로젝트 개요

공급망 데이터를 활용하여 **D-day 발주량을 3일 전에 예측하는 모델**을 구축했습니다.  
실제 예측 시점에서 확보 가능한 데이터만 사용하여 생산계획 및 자재 준비를 위한 **3일의 대응 리드타임 확보**를 목표로 했습니다.

---

## 주요 과정

- 데이터 품질 검증 및 예측 대상 부품 선정
- D-3 시점의 정보만 활용하는 **3-Day Ahead Dataset 구축**
- 시계열 패턴 학습을 위한 **LSTM 모델 구축**
- 과거 발주량 기반 통계적 기준 모델인 **ARIMA 적용**
- 발주량·계획량 간 비선형 관계를 학습하는 **XGBoost 모델 구축**
- 시간 순서를 유지한 Validation 및 모델 성능 비교
- Validation 기준 하이퍼파라미터 최적화 및 최종 모델 선정

---

## 모델 성능

| Model | Test MAE |
|---|---:|
| LSTM | **5.62** |
| ARIMA | **5.60** |
| XGBoost | **4.89** |

**XGBoost가 Test MAE 4.89로 가장 높은 예측 성능을 기록했으며, LSTM 대비 예측 오차를 약 13% 감소시켜 최종모델로 선정.**

---

## 핵심 성과

- **3일 후 발주량 선제 예측**
- **실제 발주량과 4.89개 차이**
- 생산량 조정 및 자재 준비를 위한 사전 대응 기반 마련
- 경험 중심의 생산계획을 데이터 기반 정량적 의사결정으로 전환

---

## Tech Stack

`Python` `R` `Pytorch` 
