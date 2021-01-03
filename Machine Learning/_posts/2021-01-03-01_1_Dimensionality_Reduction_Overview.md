---
layout: page
title: 01_1_Dimensionality Reduction Overview

---

이 글은 고려대학교 산업경영공학과 강필성 교수님의 IME654 강의를 참고하여 작성되었습니다.

-------

### 차원축소란?
머신러닝을 수행하는 과정은 크게 3단계로 나누어진다.
1. Pre-Processing (전처리)
2. Learning (학습)
3. Error Analysis (오차분석)

data를 전처리(Pre-processing) 하는 방법은 크게 3가지가 있는데,
대표적으로 Normalization(정규화)와 Dimension Reduction(차원 축소)가 있다.
이 글에서는 차원 축소에 대해 알아보도록 하겠다.

### 차원 축소의 목적
원래 가지고 있던 데이터의 변수의 개수를 줄여서 학습의 속도를 빠르게 하고 비용을 줄이는 것이다. 동시에 예측 모형의 성능저하가 최대한 일어나지 않도록 해야 할 것이다.

### 차원축소를 해야하는 이유
높은 차원을 가지는 data가 증가하여, 차원축소를 하지 않고서는 data를 사용하는 것이 불가능하거나 매우 어렵기 때문이다.

### 차원의 저주 (Curse of dimensionality)
동일한 설명(표현)을 위해서, 변수(variables)의 개수가 선형적으로 증가한다면 객체(sample)의 개수는 지수적으로 증가하여야 한다.
즉, n 차원의 정보를 손실 없이 표현하기 위해서는 $2^n$ 개의 sample이 필요하다.