---
description: 마르코프 결정 과정 - 다음 길은 어디로?
---

# Markov Decision Process

## Markov Process

### Purpose of Markov Process

* 강화학습 환경을 Formal하게 묘사하기 위함 
* 이때 이 환경은 Full Observable해야 한다. 즉, 현재 State가 process를 완전히 나타낼 수 있어야 함
* 거의 모든 강화학습 문제가 MDP로 구현될 수 있다.

  * 최적화 문제는 연속적인 MDP로!
  * Partial Observable한 문제 또한 MDP로 변환 가능
  * 이후의 예시는 "Bandit"\(State가 하나 있는 MDP\)를 예시로 듬

* 무기억성\(memoryless\) random process
* Markov property를 가진 random state $$S_1, S_2, ...$$의 시퀀스

### Recall : Markov Property 

* State $$S_t$$가 Markov이 되기 위한 필요충분 조건은, $$P[S_{t+1}|S_t] = P[S_{t+1}|S_1, ... , S_t]$$이다.
  * 즉, 현재로부터 과거의 정보 $$S_1, ..., S_{t-1}$$은 미래에 일어날 일과 독립이다!

### State Transition Matrix

* Markov state $$s$$와 그 뒤에 오는 $$s'$$에 대해 $$P_{ss'} = P[S_{t+1} = s' | S_{t} = s]$$
  * State Transition Matrix $$P$$는 모든 $$s$$→ $$s'$$로의 transition probability를 정의
  * $$P = \begin{bmatrix} P_{11} & ... & P_{1n} \\ ... &  & ... \\ P_{n1} & ... & P_{nn} \end{bmatrix}$$
  * 이때 $$\sum$$of row == 1

### Definition : Markov process\(=Markov Chain\)

* Tuple $$<S, P>$$
* $$S$$는 유한한 State들의 집합
* $$P$$는 State Transition Probability Matrix :$$P{ss'} = P[S_{t+1} = s' | S_{t} = s]$$



## Markov Reward Process

### Definition : Markov Reward Process

* Tuple $$<S, P, R, \gamma>$$
* Markov Chain에 Reward와 discount factor가 추가된 형태
* $$S$$는 유한한 State들의 집합
* $$P$$는 State Transition Probability Matrix :$$P{ss'} = P[S_{t+1} = s' | S_{t} = s]$$
* $$R$$은 Reward expectation : $$R_s = E[R_{t+1} | S_{t} = s]$$

