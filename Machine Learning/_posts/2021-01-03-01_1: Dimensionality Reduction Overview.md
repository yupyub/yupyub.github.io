---
layout: page
title: 01_1: Dimensionality Reduction Overview

---

## 차원축소란?
머신러닝을 수행하는 과정은 크게 3단계로 나누어진다.
1. Pre-Processing (전처리)
2. Learning (학습)
3. Error Analysis (오차분석)

data를 전처리(Pre-processing) 하는 방법은 크게 3가지가 있는데,
대표적으로 Normalization(정규화)와 Dimension Reduction(차원 축소)가 있다.
이 글에서는 차원 축소에 대해 알아보도록 하겠다.

차원 축소를 통해 하고자 하는 것은 원래 가지고 있던 데이터의 변수의 개수를 줄여서 학습의 속도를 빠르게 하고 비용을 줄이는 것이다. 동시에 예측 모형의 성능저하가 최대한 일어나지 않도록 해야 할 것이다.
