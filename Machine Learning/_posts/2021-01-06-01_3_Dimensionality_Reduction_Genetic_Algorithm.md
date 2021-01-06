---
layout: page
title: 01_3_Dimensionality Reduction:Genetic Algorithm

---

이 글은 고려대학교 산업경영공학과 강필성 교수님의 IME654 강의를 참고하여 작성되었습니다.

---

### Meta-Heuristic Approach
- 매우 복잡한 문제들을 __효율적__ 으로 Trials and Error 방법을 통해 해결한다.
- 자연에서 발견되는 방법들을 응용하는 경우가 많다. (ex. Neural Network, Ant Colony Algorithm, Particle Swarm Optimization)

> Genetic Algorithm is an Evolutionary Algorithm that mimics the Reprodustion of Creatures

Genetic Algorithm은 유전과 진화를 모방하여 Reproduction과정을 반복하고 이를 통해 Superior Solution을 찾습니다.

- Selection : Quality를 향상시키는 더 좋은 해(Superior Solution)를 선택합니다.
- Crossover : 현재의 해들을 다양하게 조합하여 더 나은 대안을 찾습니다.
- Mutation : Local Optima에 빠지는 것을 방지하기 위해서 돌연변이를 발생시킵니다.

---

### Genetic Algorithm의 변수 선택과정 (Feature Selection)
1. Initiation : 염색체 초기화 및 파라미터 설정
2. Fitness : 각 염색체별로 대응하는 변수를 사용하여 모델을 학습시킨다.
3. Selection : 각각의 학습한 모델을 통해 각 염색체의 적합도 평가를 한다.
4. Mating(Crossover) : 적합도 평가를 통해 선택된 염색체들을 통해 새로운 세대를 생성한다.
5. Mutation : 새로운 세대들에 대하여 돌연변이를 발생시킨다. (2번으로 돌아가 과정을 반복한다)
6. Final Generation : 5까지의 수행결과가 수렴한다면 최종적으로 해당 염색체를 선택한다.

유전 알고리즘은 변수 선택에만 사용되는 것이 아니라, 다양한 최적화 문제에 사용됩니다.
이 글에서는 변수 선택에 사용되는 유전 알고리즘을 기반으로 설명하겠습니다.

--- 

### Step1: Initialization
- 인코딩 방법은 다른 종류의 task마다 다른 방법을 사용할 수 있습니다.
- Variable Selection에는 일반적으로 Binary Encoding을 사용합니다. 그 중에서 Chromosome을 이용해 보겠습니다.
#### Encoding Chromosomes
Chromosome 구조는 아래와 같습니다. 이때 각 x는 유전자(Gene)이고, 아래 0, 1 비트는 0이면 해당 변수를 모델링에 사용하지 않음을, 1이면 해당 변수를 모델링에 사용함을 나타냅니다.

|x1|x2|x3|x4|x5|x6|x7|x8|...|xd|
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|1|0|1|1|0|1|0|0|...|1|

#### Parameter Initialization
- The Number of chromosome (Population) : N개로 지정한다면 1 세대에서 N개의 변수 부분집합을 평가함
- Fitness Function : 각각의 Chromosome의 Quality를 평가하는 함수
- Crossover Mechanism : 교배 방법
- The rate of mutation : 돌연변이율
- Stopping criteria : 종료조건 (ex. minimum fitness improvement, maximum iterations)

19:40 (선형회귀분석...)
