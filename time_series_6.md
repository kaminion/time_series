# 시계열 예측 모형 만들기

# ARMA / ARIMA 모형을 이야기하기에 앞서 복습

- 시계열 
    - AR 모델
        - 이번기의 결과는 이전기의 결과 영향을 받는 모델
    - MA 모델
        - 외부의 충격이 e기 이상 지속되는 모형

- 이것을 합친 것을 ARMA 모형이라고 함

# ARIMA(Auto Regressive Integrated Moving Average)
- 대부분의 모형은 안정적이지 않아서 안정적인 모형인 ARIMA 모형을 씀
- 얼마나 차분 할 지 결정적인..
- 차분값을 활용하기보다 변동률로 변환하기 위해 원계열에 log나 log difference를 취하는 경우도 많다

- 예측 모형 만드는 순서
    - 안정성 검토
    - 데이터 특성에 맞는 모형 결정(AR차수와 MA차수)
    - 학습
    - 평가

# 학습 및 평가
1. 학습데이터를 평가에 사용하는 경우
    - 의미가 없다
2. 학습 데이터와 테스트 데이터를 분리하여 사용하는 경우
    - 예측 가능