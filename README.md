# TF_Keras_RNN
순환 신경망 구축

SimpleRNN 레이어에는 한가지 치명적인 단점이 있습니다. 입력데이터가 길어질수록, 데이터의 타임스텝이 커질수록 학습능력이 떨어집니다.
이를 장기 의존성(Long-Term Dependency)문제라고 하며, 입력 데이터와 출력 사이의 길이가 멀어질 수록 연관 관계가 적어집니다.
현재의 답을 얻기 위해 과거의 정보에 의존해야하는 RNN이지만 과거 시점이 현재와 너무 멀어지면 문제를 풀기 힘들어지는점이 있습니다.
이러한 문제점을 개선하기 위해서 장기의존성 문제를 해결하기 위한 구조로 셉 호흐라이터(Sepp Hochreiter)와 유르겐 슈미트후버에 의해 LSTM이 1997년에 제안됩니다.

LSTM은 RNN에 비해 복잡한 구조를 가지고 있는데 가장 큰 특징은 출력외에 LSTM 셀사이에서만 공유되는 셀상태를 가지고 있다는점 입니다.
LSTM 레이어에는 활성화 함수로 tanh외에 시그모이드 함수가 쓰였습니다. 시그모이드 함수는 항상 0~1 범위의 출력을 내며, 시그모이드 함수는 이러한 출력의 특성
때문에 정보가 통과하는 게이트 역할을 합니다. 출력이 0이면 입력된 정보가 하나도 통과하지 못하는것이 1이면 100% 통과하는 형태로 진행됩니다
