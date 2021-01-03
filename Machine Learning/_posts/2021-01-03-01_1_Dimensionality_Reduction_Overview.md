---
layout: page
title: 01_1_Dimensionality Reduction Overview

---

이 글은 고려대학교 산업경영공학과 강필성 교수님의 IME654 강의를 참고하여 작성되었습니다.

---

### 차원축소란?
머신러닝을 수행하는 과정은 크게 3단계로 나누어진다.
1. Pre-Processing (전처리)
2. Learning (학습)
3. Error Analysis (오차분석)

data를 전처리(Pre-processing) 하는 방법은 크게 3가지가 있는데,
대표적으로 Normalization(정규화)와 Dimension Reduction(차원 축소)가 있다.
이 글에서는 차원 축소에 대해 알아보도록 하겠다.

---
### 차원 축소의 목적
원래 가지고 있던 데이터의 변수의 개수를 줄여서 학습의 속도를 빠르게 하고 비용을 줄이는 것이다. 동시에 예측 모형의 성능저하가 최대한 일어나지 않도록 해야 할 것이다.

---
### 차원축소를 해야하는 이유
높은 차원을 가지는 data가 증가하여, 차원축소를 하지 않고서는 data를 사용하는 것이 불가능하거나 매우 어렵기 때문이다.

---
### 차원의 저주 (Curse of dimensionality)
동일한 설명(표현)을 위해서, 변수(variables)의 개수가 선형적으로 증가한다면 객체(sample)의 개수는 지수적으로 증가하여야 한다.
즉, n 차원의 정보를 손실 없이 표현하기 위해서는 $2^n$ 개의 sample이 필요하다.
> "If there are various logical ways to explain a certain phenomenon, the __simplest__ is the best"-Occam's Razor

#### 변수가 많아지는 경우 생기는 문제점
1. data에 noise가 포함될 확률이 높아진다 -> 성능을 저하시킨다.
2. 학습과 실제 Applying에 있어서 computation burden(계산복잡도)가 높아진다. -> 느려진다.
3. 동일한 일반화 성능을 얻기 위해서 더 많은 sample이 필요하다.

#### 차원의 저주를 해결하는 방법
1. 잘 알고있는 domain knowledge를 기반으로 명시적인 변수를 선택한다.
2. Objective function에서 Regularization term을 사용한다. (ex. 선형회귀분석의 Ridge, LASSO 등)
3. 정량적인 __차원축소__ 방법을 사용한다.

실제로 intrinsic dimension(고유 차수)이 original dimension보다 작은 경우가 많다.

---
#### Backgrounds
1. 이론적으로, 변수의 수가 증가한다면 모델의 성능도 향상되어야 한다. __단, 각 변수가 독립적이어야 한다__ (현실적으로 불가능)
2. 현실에서는, 서로 종속적인 변수의 수가 증가한다면 noise가 증가하게 되고, 모델의 성능이 저하된다.

#### 차원 축소의 목적
- 모델에 가장 적합한 변수들의 부분 집합을 찾는 것
#### 차원 축소의 효과
1. 각 변수간의 상관관계 제거
2. Post-processing의 간략화
3. 필요 없는 변수의 제거
4. 시각화를 하기에 더 용이해진다.

---
### Supervised vs. Unsupervised Dimentionality Reduction
- Supervised Dimentionality Reduction
Feedback loop가 있어서, 변수 선택 과정에서 data mining model이 사용된다.
- Unsupervised Dimentionality Reduction
Feedback loop가 없고, 변수 선택 과정에서 data mining model이 사용되지 않는다. Dimentionality Reduction과정이 독립적으로 수행된다.
  
---
### Variable/feature Selection vs. Extraction
- Variable/feature Selection
원본 변수 집합 중 사용할 부분 집합을 선택한다.
- Variable/feature Extraction

