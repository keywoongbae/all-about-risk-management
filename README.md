# All about Risk-management

이 레포는 **리스크관리**와 관련된 다양한 자료, 논문들을 정리하여 요약 및 리뷰를 하는 모음입니다.

This repo is a collection of summaries and reviews of various links and papers related to **Risk management.**

### Related Links/Posts

- **Catastrophic Risk**
  - **Machine Learning for Disaster Risk management** [[Website]](https://www.gfdrr.org/sites/default/files/publication/181222_WorldBank_DisasterRiskManagement_Ebook_D6.pdf)
    - The World Bank
    - Global Facility for Disaster Reduction and Recovery (GFDRR)



### Papers

- **Cyber risk**
  - **The drivers of cyber risk** [[Paper](./papers/Aldasoro_JFS_2022.pdf)] [[Review](./review/the_drivers_of_cyber_risk.md)]
    - Iñaki Aldasoro, Leonardo Gambacorta, Paolo Giudici, Thomas Leach
    - Journal of Financial Stability 2022.
    - 두터운 꼬리 분포를 띄는 사이버리스크는 회사의 크기가 클수록, 사건이 우발적일수록(극단적인 케이스 제외), 디지털 사용 점유율(클라우드 서비스)이 클수록 커지며, 피싱/스키밍 분야의 사건이 cyber cost가 높다.



- **Lee-Carter models & morality rates**
  - **A Neural Network extension of the Lee-Carter model to multiple populations** [[Paper](./papers/Richman_and_Wuthrich_AAS_2021.pdf)] [[Review](https://newindow.tistory.com/319)]
    - Ronald Richman, Mario V. Wüthrich
    - Annals of Actuarial Science 2021.
    - 보험에서 중요한 지표인 사망률 추정에는 Lee-carter 계열 모델(CAE, ACE)보다 인공신경망을 사용하는 것이 더 성능이 좋다.
  - **Time-series forecasting of mortality rates using deep learning** [[Paper](./papers/Perla_et_al_SAJ_2021.pdf)] [[Brief]()]
    - Francesca Perla, Ronald Richman, Salvatore Scognamiglio & Mario V. Wüthrich
    - Scandinavian Actuarial Journal 2021.
    - 본 논문에서는 사망률 추정을 위해 Lee-carter 모델의 alternative로 딥러닝을 제시한다. 딥러닝 모델로는 CNN을 이용한 모델인 LCCONV, 그리고 RNN의 상위버전인 LCLSTM을 사용하였으며, tanh함수와 relu함수로 차이를 두어 어떤 모델이 예측을 더 잘하는지를 보았다. 실험 결과 LCCONV가 제일 성능이 좋았으며, 전반적으로 tanh 함수를 사용했을 때 성능이 더 좋았다.