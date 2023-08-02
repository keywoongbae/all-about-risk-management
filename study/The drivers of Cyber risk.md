# The drivers of Cyber risk

> Title : The drivers of cyber risk
>
> Authors : Iñaki Aldasoro , Leonardo Gambacorta , Paolo Giudici , Thomas Leach
>
> Journal : Journal of Financial Stablility

### 초록

사이버 사건은 점점 더 정교해지고, 정량화되기가 어렵다. cyber event에 대한 데이터베이스를 사용해서, 본 논문은 사이버 사건의 특징과 원인을 정리한다.

cyber costs는 기업 규모가 커지거나 여러 조직들에 동시에 영향을 줄 수록 더 커지게 된다. (events with malicious intent tend to be less costly, unless they are on the upper tail of the loss distribution.) 

금융적인 부문은 사이버 공격에 더 노출되어 있으나, 평균적으로 비용은 적다. (the use of cloud services is associated with lower costs, especially when cyber incidents are relatively small.) 클라우드 서비스

마침내, 본 논문에서는 

### 1. Introduction

IT 기술이 발전하면서 사이버리스크가 발생하게 됨.

- 사이버리스크란, IT 시스템의 실패로부터 발생하게 되는 조직의 재정적 손실, 분열, 혹은 평판적인 손해를 말함.

- 여러 기업에서는 cyber risk를 측정하기 위해 노력하지만 이는 측정하기 어려움. 
- 하지만 이러한 상황에도 cyber risk에 대한 cost, drivers, 그리고 potential mitigating factor에 대한 정보가 부족함.



### 3. Data

본 논문에서는 advisen으로부터 얻은 데이터셋을 사용하며, 다음과 같은 특징을 가지고 있음.

- 사건 분류 (데이터 유출, 데이터 피싱), 빈도 수, 사건 날짜, source of the loss, 손실의 종류, actor (state-sponsored, terrorist), 손실 금액, 기업 규모, 기업 종류, 직원 수, NAICS, 지질학적 정보

- 데이터베이스 내 사건들은 대부분 미국에서 발생 (미국에서의 정보수집 자유도가 높기 때문)
- 정보 수집에 한계가 있기 때문에 각각 사건들에 대한 정보들을 보유하는 것은 불가능

cyber event에 대한 비용은 3개의 구성요소로 구분됨.

- 직접 비용 : 사건의 피해자들이 입은 손실, 피해 및 기타 고통의 직접적인 가치
- 간접 비용 : 간접 비용은 사이버 사고의 결과로 사회가 부담하는 손실 및 기회 비용
- 완화 비용 : 사이버 위협 인식 교육의 바이러스 백신 소프트웨어와 같은 보안 제품에 대한 투자를 포함하는 비용

Advisen 데이터는 위의 3개의 구성요소 중, **직접 비용**으로 해석될 수 있음.

- Advisen 데이터셋은 충분히 자세하게 채워지지는 않음.
- 따라서 본 연구에서 회귀분석을 하는 경우, 누락된 관측치를 제거하여 3705개의 샘플만 남겼음.

cyber event의 빈도(frequency)와 비용(costs)은 부문마다 다름. 

- "금융 및 보험 활동"에서 cyber event가 가장 많이 발생하였음.
- 도매무역, 운송및보관, 전문/과학 및 기술 순으로 cyber cost가 높았음을 알 수 있음.
  - 부문에 따라 비용의 표준편차가 상당히 큼(손실 분포가 두꺼운 꼬리를 가질 가능성이 높다)

<img src="C:\Users\Keywoong\AppData\Roaming\Typora\typora-user-images\image-20230802213636109.png" alt="image-20230802213636109" style="zoom: 45%;" />

빈도수 분포는 상대적으로 안정적임.

- 



### 7. Conclusions

기술과 인터넷의 발전, 그리고 클라우드 서비스의 사용은 회사의 생산성을 향상시켰으나, 사이버 공격에 노출되었음.

사이버공격으로 인해 발생하는 사이버 리스크는 정량화하기가 어려움.

따라서 어드바이젠 데이터셋(a unique database at the firm level for the US)으로 연구를 진행하였음.

- 