# The drivers of Cyber risk

> Title : The drivers of cyber risk
>
> Authors : Iñaki Aldasoro , Leonardo Gambacorta , Paolo Giudici , Thomas Leach
>
> Journal : Journal of Financial Stablility

> **논문 읽으면서 궁금한 점**
>
> 1) 어드바이젠 데이터셋은 왜 

<hr>

### 초록

사이버 사건은 점점 더 정교해지고, 정량화되기가 어렵다. cyber event에 대한 데이터베이스를 사용해서, 본 논문은 사이버 사건의 특징과 원인을 정리한다.

cyber costs는 기업 규모가 커지거나 여러 조직들에 동시에 영향을 줄 수록 더 커지게 된다. (events with malicious intent tend to be less costly, unless they are on the upper tail of the loss distribution.) 

금융적인 부문은 사이버 공격에 더 노출되어 있으나, 평균적으로 비용은 적다. (the use of cloud services is associated with lower costs, especially when cyber incidents are relatively small.) 클라우드 서비스

마침내, 본 논문에서는 

본 논문에서 알고자 하는 것 : 

### 1. Introduction

IT 기술이 발전하면서 사이버리스크가 발생하게 됨.

- 사이버리스크란, IT 시스템의 실패로부터 발생하게 되는 조직의 재정적 손실, 분열, 혹은 평판적인 손해를 말함.

- 여러 기업에서는 cyber risk를 측정하기 위해 노력하지만 이는 측정하기 어려움. 
- 하지만 이러한 상황에도 cyber risk에 대한 cost, drivers, 그리고 potential mitigating factor에 대한 정보가 부족함.

### 2. Related literature

본 논문에서는 IT의 어떤 특징와 cost가 연결되어 있는지를 확인하고자 함.

Cyber cost와 sector간의 관계는 (1) 기업이 어떻게 운영하는지도 중요하지만 (2) IT 보완 투자 여부에도 영향을 받음.

-  경쟁이 덜 치열하고 성장이 덜된 산업에서 사이버 공격 가능성 더 높음.
- 

### 3. Data

본 논문에서는 advisen으로부터 얻은 데이터셋을 사용하며, 이 데이터셋은 다음과 같은 특징을 가지고 있음.

- 사건 분류 (데이터 유출, 데이터 피싱), 빈도 수, 사건 날짜, source of the loss, 손실의 종류, actor (state-sponsored, terrorist), 손실 금액, 기업 규모, 기업 종류, 직원 수, NAICS, 지질학적 정보라는 칼럼 등등.

- 데이터베이스 내 사건들은 대부분 미국에서 발생 (미국에서의 정보수집 자유도가 높기 때문)
- 정보 수집에 한계가 있기 때문에 각각 사건들에 대한 정보들을 보유하는 것은 불가능

기존 cyber event에 대한 비용은 3개의 구성요소로 구분됨.

- 직접 비용 : 사건의 피해자들이 입은 손실, 피해 및 기타 고통의 직접적인 가치
- 간접 비용 : 간접 비용은 사이버 사고의 결과로 사회가 부담하는 손실 및 기회 비용
- 완화 비용 : 사이버 위협 인식 교육의 바이러스 백신 소프트웨어와 같은 보안 제품에 대한 투자를 포함하는 비용

Advisen 데이터는 위의 3개의 구성요소 중, **직접 비용**으로 해석될 수 있음.

- Advisen 데이터셋은 모든 데이터 값들이 충분히 자세하게 채워지지는 않음.
- 따라서 본 연구에서 회귀분석을 하는 경우, 누락된 관측치를 제거하여 3705개의 샘플만 남겼음. <span style="color:red">Red Text</span>

cyber event의 빈도(frequency)와 비용(costs)은 부문마다 다름. 

- frequency : "금융 및 보험 활동"에서 cyber event가 가장 많이 발생하였음.
- cost : 도매무역, 운송및보관, 전문/과학 및 기술 순으로 cyber cost가 높았음을 알 수 있음.
  - 부문에 따라 비용의 표준편차가 상당히 큼(손실 분포가 두꺼운 꼬리를 가질 가능성이 높다)

![image-20230803110744557](C:\workspace\All-about-Risk-management\study\imgs\image-20230803110744557.png)

|                          cost 분포                           |                         빈도수 분포                          |
| :----------------------------------------------------------: | :----------------------------------------------------------: |
| - cost 분포에서 2012년에서는 ICT와 FI가 가장 높은 비중을 가짐.<br />- 금융 위기 이후 FI 부문의 사이버 사고 빈도 증가는 부분적으로 은행에 대한 표적 공격에 의해 주도되었을 수 있음. | - 빈도수 분포는 상대적으로 안정적임.<br />- 빈도수 분포를 보면 Finance/Insurance뿐 아니라 Admin. and Support도 비중이 높음. |

![image-20230803110836978](C:\workspace\All-about-Risk-management\study\imgs\image-20230803110836978.png)



### 4. Identifying the drivers of cyber costs

#### 4.1 경험적 접근

본 논문에서는 아래 모델을 통해 사건과 회사/부문 특징에 따른 사이버 사건의 비용을 설명하고자 함.

-  $C_{i,f,g} = \beta Z_{i,f,g}+\lambda W_{f,g}+\theta X_g + \eta_k + \alpha_t + u_{i,f,g}$

  - |  Notations  | Detail                 |
    | :---------: | ---------------------- |
    |     $i$     | 사건들 수 ($N_i 3705$) |
    |     $f$     | 사건이 발생하는 회사   |
    |     $g$     | 부문                   |
    | $C_{i,f,g}$ | 사건의 비용            |
    |    $X_g$    | sector-level controls  |
    |             |                        |
    |             |                        |
    |             |                        |
    |             |                        |






### 7. Conclusions

기술과 인터넷의 발전, 그리고 클라우드 서비스의 사용은 회사의 생산성을 향상시켰으나, 사이버 공격에 노출되었음.

사이버공격으로 인해 발생하는 사이버 리스크는 정량화하기가 어려움.

따라서 어드바이젠 데이터셋(a unique database at the firm level for the US)으로 연구를 진행하였음.

- 