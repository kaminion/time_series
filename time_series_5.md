# 시계열 예측 방법론 : 데이터 기반

# 금융 / 계량
- ARIMA와 변형 모형
    - Benchmark 모형 많이 쓰임
        - Univariate (단변량) 시계열 예측
- 계층적 시계열 모형
    - 시계열 특성 큰 변화가 생겼을 경우 사용
    - e.g. 금융위기 부근에서 데이터 특성이 변동된 경우
- VAR과 변형 모형
    - Vector AutoRegressive : AR 모델 변수 확장
        - Multivariate(다변량) 시계열 예측할 때 널리 사용
- GARCH와 변형 모형
    - 변동성에 전체 시계열이 영향을 받는 경우 (ex. 주식 종목 별 등락데이터) 변동성을 고려한 예측 모형
    - High frequency (일단위) 예측에 사용

# 딥러닝
- RNN
    - Recurrent Neural Network 모델
    - AR(VAR) 모델의 딥러닝 버전
    - 과거 데이터를 현재 예측에 집어넣는 모형

- LSTM
    - Long Short-Term Memory 모델
        - 장기 기억도 가능하도록 Memory - Selection Gate 정의
    - 기존 학습내용 지워지는 것 보완
    - Rare disaster 와 같이 high order term이나 계층적 시계열 특성 반영

# 시계열 예측 방법론: 최적화 기반

- 매 시간 + 최적화 = Dynamic Programming(동적 프로그래밍)
    - 현재 상태에서(State Variable = 자본, 기술, 고용 수준 등..)
    - 외부 변화가 주어질 경우(Exogenous Variable = 세금상승, 규제등...)
    - 이후 예상되는 모든 후생을 최대화 하도록(Value Function = Life time Utility)
    - 행동한다. (Policy Function)
- 거시 경제, 금융에서 많이 사용
- 지금 소비(투자)할 것인가? 다음 기회에 소비(투자) 할 것인가?

**최적화 기반 방법 두가지**

- Deterministic Decision(확정적 결정)
    - Dynamic Stochastic General Equilibrium model
        - 외부 요소는 확률적이지만 agent 결정은 확정적
        - 매기 최적의 Decision을 도출

- Stochastic Decision(확률적 결정)
    - Enforcement learning model(강화학습)
        - 외부 요소 뿐만 아니라, agent의 결정도 '확률적'임
        - 최적화일 확률이 높은 Decision을 도출
        - e.g. 바둑은 미래 상대의 결정을 알 수 없기 때문에 모든 결정이 확률적임.