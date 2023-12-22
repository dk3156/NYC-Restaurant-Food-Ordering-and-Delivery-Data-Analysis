Kaggle 의 nyc restaurant data - food ordering and delivery 데이터셋을 분석하고 시각화한 미니 프로젝트이다.
pandas 라이브러리를 통해 데이터 EDA를 진행하고 matplotlib, seaborn, plotly 시각화를 통해 결과 해석 도출했다.

## **food_orders.ipynb**
### EDA

데이터 전처리: 오타난 음식점 이름을 수정해 주었다. rating 의 not given 값을 np.nan 로 대체했다.

미국 음식점이 주문량이 가장 많았으며 cuisine_type 별 주문량의 차이가 크다.   

주말이 주중보다 주문량이 평균 2배 이상 높다.


## **AmericanStore.ipynb**
주문량, 고객수가 가장 많았던 미국 음식점 중심으로 고객 수 값과 평균 주문 금액(cost_of_the_order), 평균 음식 준비 시간(food_preparation_time), 평균 배달 시간(delivery_time) 의 상관계수를 계산했다. 

그 결과 상관계수가 모두 0.06 이하로 크게 유의미한 관계는 보이지 않았다. 

다른 나라의 음식점을 모두 포함해서 고객 수 상관계수를 계산했지만 큰 의미를 보이지 않았다. 

## **DA_food_order.ipynb**
팀원들의 EDA 와 시각화를 합친 최종 결과물이다. 

주문량이 많고 적은 식당을 비교 분석하기 위해 식당을 A, B, C 그룹으로 나누었다. 

주문량 상위 10위까지의 식당을 A, 주문량이 2개 이하인 식당을 C, 중간에 속하는 식당을 B 그룹으로 나누었다. 

qcut 메서드로 구간을 나누었지만 중간그룹 B가 주문량 2 초과 5 이하로 나뉘어졌고, 주문량이 매우 적다고 판단되어 A 그룹에 상위 10개 식당만 포함되도록 구간을 개선했다.

A, B, C 그룹으로 나누어 다시 상관계수를 구해본 결과 주문 금액, 음식 준비 시간, 평가와의 상관관계가 관찰되었다.

A, B 그룹은 주중/주말에 주문금액이 비슷한 분포가 관찰되었지만, C 그룹은 주말의 주문금액이 25 % / median / 75 % 가 더 높은 금액대에 분포한다는 걸 관찰했다.

A 그룹은 주말에 음식 준비 시간이 더 짧게 분포되어 있지만, C 그룹은 주말의 음식 준비 시간이 더 오래 걸리고 있는 것을 확인했다.

A 그룹은 주말과 주중의 평점 5점이 4% 차이를 보였지만, C 그룹은 주말과 주중 평점 5점이 9 % 차이를 보였다.

데이터 분석 결과 A 그룹은 주말 주문량이 주중의 약 3배나 많지만 평점과 음식 준비 시간이 큰 차이가 나지 않았다는 걸 확인했다.

A 그룹은 주말 주문량에 대한 대비를 하여 서비스 품질이 유지되도록 조치를 하는 것으로 판단된다. 
 
## 결론
결과적으로 주문량이 많지 않은 식당은 차후 식당 서비스 품질 향상을 위하여 주말의 주문 금액, 음식 준비 시간, 평점을 주중과 비슷하게 유지시킬 것을 제안해 볼 수 있다.

## 프레젠테이션
https://docs.google.com/presentation/d/16L1qF36Wseo42485VwU35djB4T9uhWJnxSjnJUW9bYo/edit?usp=sharing

## 설명 영상
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/_Ckgw3W1mrQ?si=BROD_enV1FQravnK/0.jpg)](https://youtu.be/_Ckgw3W1mrQ?si=325JIqpSP2eq7Lmq)