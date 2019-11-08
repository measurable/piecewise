---
title: "2. 순수 수학의 등장 배경: 수학의 내부"
date: 2019-10-07T20:46:02+09:00
categories:
    - 방법
tags:
    - math
keywords:
inspired:
motivation: "사실, 지금은 당연하게 느껴지는 것이 처음엔 그다지 당연하지 않은 것이었음을 이해하기는 어렵다. 그래서 수학의 경우엔 일반적으로 지식의 확실성이라는 문제로만 접근된다. 그러나: 지식이 경험 세계와의 관련을 끊어버리는 과정은 그 자체로 엄청난 사고의 전환이 아닐까?"
draft: true
---

도대체 어떤 계기와 과정이 있었을까?
어떻게 해서 물리적 해석을 갖지 않은, 나아가 물리 세계에는 도저히 존재할 수 없을 듯한 개념과 구조와 이론이 탐구할 만한 흥미를 끌고 중요성을 갖는다고 생각하게 되었을까?
그게 바늘 끝에서 춤출 수 있는 천사의 수에 관한 탐구와는 어떤 점에서 다른가? 또, (시대를 고려하면) 비엔나 서클의 압도적인 철학적 제약을 어떻게 뚫을 수 있었을까?---의도적인 사상투쟁이 아님에도.

더 근본적인 문제가 있다.
수학이 물리적 세계와 관련을 갖지 않는다면, 수학의 진실성은 도대체 어떤 의미를 가지며, 또한 어떻게 보장할 수 있을까?
세 가지 줄기를 가지고 접근해 보자.

## 1. 수학의 요구

수학이 어떻게 해서 과학과 분리되어 자기 길을 가게 되었는가에 관한 첫번째 이야기는,
제기된 다양한 주제에 관한 연구 과정에서 과학적 동기를 갖지 않는 과제들이 자연스럽게 나타난다는 것이다.

예시적으로, 추상군 개념의 기원에 대해 살펴보자.
지금은 갈루아의 작업에서 치환군과 그 부분군이 하는 역할에 대해서 잘 이해하고 있다. 그러나,

1. 1830년 경, 갈루아 자신은 그런 개념을 만들어내지 않았다. 20여년 후 케일리에 이르러서야 비로소 그게 개념화됐다.
2. 놀랍게도, 케일리의 버전은, 나아가 그 이후의 데데킨트의 개념화도 그냥 묻혀버렸다. 그것은 단지 그런 개념을 유용하게 써먹을 수 있는 군의 사례가 충분히 많이 연구되지 않고 있었기 때문이다.
3. 1870년대에 이르러서야 갈루아 이론이나 정수론, 기하학, 미분방정식론 등에서 다양한 군의 사례가 발견되고, 그에 따라 추상군의 개념이 주의를 끌고 본격적으로 사용되게 된다.

추상군의 개념은 이 때부터 고유한 수학적 목적을 가지고 의식적으로 사용되기 시작했다:

- 전혀 비슷해 보이지 않는 다양한 구조들 사이에서 군의 개념으로만 포착할 수 있는 유사성이 발견되고 주의를 끌기 시작했다.
- 서로 다른 다양한 맥락에 폭넓게 적용될 수 있는 일반 이론이 정교하고 세부적으로 만들어지게 되었다.
- 주어진 현상에 접근하는 유용한 방법론을 제공했다.(가령, \\(x\\)가 \\(y\\)라는 성질을 갖는 것은 \\(x\\)에 내포된 \\(z\\)나 \\(v\\)나 \\(w\\)라는 고유한 특징 때문이 아니라 그게 가지는 군의 구조 때문이다...)

군 개념 자체도 수학 자체의 요구에 부합하도록 점진적으로 재정의되어갔다.
가령, 원래 소거 법칙으로 이해되던 것이 무한군의 개념이 필요하게 되자 역원의 존재를 군의 정의에 포함시키는 방식으로 개정된다.
1920년대에 이르면 군론이 물리학에 도입되고 지금은 중심적인 주제가 되어있다.

## 2. 응용의 문제: Euclidean rescue

위와 같은 이야기는 전체의 한 측면일 뿐이다.
다른 측면의 이야기는 정반대로 물리 세계에 대해 수학이 갖는 의미에 대한 재검토에서 시작된다.
이 이야기는 기하학에서 가장 잘 드러난다:

>기하학의 진실성을 의심하라! (가우스. 클라인, 1972, p. 872에서 재인용.)

1800년에 이르러 유클리드의 평행선 공리는 증명될 수 없으며, 다른 공리로 대치해도 논리적으로 일관된 기하학을 구성할 수 있다는 사실이 밝혀졌다. 그럼에도 불구하고 실제 공간에 대해서는 여전히 유클리드 기하 만이 참된 이론이었다.

여기서 가우스가 등장한다.
가우스는 실제 공간이 유클리드 기하로 이루어져 있는지를 직접 테스트해보려고 했다.
그는 세 개의 산봉우리가 만드는 삼각형의 내각의 크기를 직접 쟀다.
실측한 내각의 크기는 오차 범위에서 180도와 일치했다.
갈릴레오의 피사 사탑 실험과 마찬가지로 그냥 전해오는 전설이다.
그러나 가우스가 물리 세계에 유클리드 기하가 아닌 다른 기하학이 적용될 수도 있다는 생각을 하고 있었던 것 만큼은 틀림없는 사실이다.[^6]
가우스는 자기 학생이었던 리만의 교수 자격 시험에 기하학의 토대를 주제로 정해 주었다.
아인슈타인이 그의 친구였던 수학자 그로스만에게 일반상대론의 수학적 기술에 관해 문의했을 때 그로스맘이 추천한 것이 바로 그 리만 기하학이었다.
일반 상대론의 성공은 적어도 물리적 세게에서는 유클리드 기하만이 참이라는 생각을 무너뜨렸다.

[^6]: 유클리드 기하가 특권적 지위를 가질 이유가 없다는 점에서. 이건 굉장히 발전된 생각.

유클리드 공간이 물리적 공간에 대한 참된 기술이 아니라는 사실이 유클리드 기하가 틀렸다는 것을 의미하지 않는다.
수학자들은 물리적 공간과 추상적 공간을 구별하기 시작했다.
수학은 다양한 종류의 추상적 구조를 제공하는 창고다.
자연과학자들은 그 중에서 적당한 것을 자유롭게 골라서 세계를 표현하는 도구로 사용한다.

수학은 경험 세계와의 일치 여부에 따라 맞거나 틀리게 돠는 것이 아니다.
수학은 물리적인 것과 다른 고유의 추상적 세계에 산다.
그렇지만 갈릴레오의 오랜 통찰은 여전히 진실이다. 자연이라는 책은 여전히 수학이라는 언어로 쓰여져 있다.
수학이 자연만 기술하는 것이 아닐 뿐이다.