---
title: "1. 동시성(simultaneity)의 정의"
date: 2019-09-22T16:47:27+09:00
categories:
    - 표현
tags:
    - sr
    - Einstein
keywords:
inspired:
motivation:
draft: false
---


# I. 운동학 (Kinematic Part)


## &sect;1. 동시성(simultaneity)의 정의



뉴턴 역학의 방정식들이 1차 근사에서 들어맞는 좌표계를 생각하자.
논의를 보다 엄밀하게 하고 다음에 도입할 다른 좌표계와 구별하기 위해 이 좌표계를 "정지 좌표계(stationary system)''라고 부르자.

질점이 이 좌표계에 대해 멈춰있으면, 일관된 측정 기준을 주고 유클리드 기하의 방법을 사용해서 그 좌표계를 기준으로 한 위치를 정의할 수 있고, 이를 데카르트 좌표로 나타낼 수 있다.

만약 질점의 운동을 기술(describe)하고 싶으면 그 좌표를 시간의 함수로 나타내면 된다.
이 때, 이와 같은 수학적 기술이 물리적 의미를 가지려면 "시간''이 무엇을 가리키는지 아주 명확해야 한다는 점을 유의해야 한다.
시간이 포함된 모든 판단은 사건의 동시성(simultaneous events)에 관한 판단이라는 점에 주목해야 한다.
예를 들면, "그 기차가 7시에 여기 도착한다''라고 말할 때, 실은 "내 시계의 짧은 바늘이 7자를 가리키는 것과 기차가 도착하는 것은 동시적 사건이다.''라고 말하고 있는 것이다.[^2]

[^2]:거의 같은 장소에서 발생한 두 사건의 동시성이라는 개념이 엄밀하지 않다는 점은 여기서 논하지 말자. 그것은 개념의 추상화를 통해서만 제거할 수 있다.

"시간''이라는 용어 대신 "내 시계의 짧은 바늘 방향''을 사용하면 "시간''의 정의와 관련된 문제가 모두 해결된 것으로 생각할 수도 있다.
사실, 오직 시계가 위치해 있는 곳의 시간만 정의할 때는 이걸로 충분하다.
그러나 서로 다른 장소에서 발생하는 사건들을 시계열로 연결하거나, 또는 (결국 같은 말이지만) 시계로부터 멀리 떨어진 곳에서 발생하는 사건들 각각의 시간을 측정할 때는 이것 만으로는 충분하지 않다.

물론,
시계를 가진 관찰자의 위치를 좌표 원점으로 삼아 시간 값을 결정하기로 하고,
측정할 사건이 방출한 빛 신호가 빈 공간을 가로질러 그에게 도착했을 때의 바늘 위치를 대응시킬 수도 있다.
그러나 경험이 말해주듯 이 방식은 시계를 가진 관찰자의 위치에 따라 시간이 달라진다는 단점이 있다.
다음과 같은 추론을 통해 훨씬 더 적절한 결정 방법을 얻을 수 있다.

공간의 점 \\(A\\)에 시계가 있으면 \\(A\\)에 바로 인접해 있는 사건에 대해서는 \\(A\\)에 있는 관찰자가 사건 발생 순간의 시계 바늘 위치를 보고 시간 값을 결정할 수 있다.
만약 \\(A\\)의 시계와 모든 면에서 똑같은 시계가 공간의 다른 점 \\(B\\)에도 있다면 \\(B\\)에 있는 관찰자는 \\(B\\) 바로 인근에서 발생하는 사건의 시간 값을 결정할 수 있다.
그러나 \\(A\\)에서 발생한 사건과 \\(B\\)에서 발생한 사건의 시간을 비교하려면 추가적인 가정이 필요하다.
지금까지는 "\\(A\\) 시간''과 "\\(B\\) 시간''을 정의했을 뿐이다.
\\(A\\)와 \\(B\\)에 공통인 "시간''은 아직 정의하지 않았다.
그럴려면 빛이 \\(A\\)에서 \\(B\\)까지 가는 데 걸리는 "시간''과 \\(B\\)에서 \\(A\\)까지 가는 데 걸리는 "시간''이 같다는 **정의**\\(\\)를 주어야 한다.
광선이 "\\(A\\) 시간'' \\(t\_A\\)에 \\(A\\)에서 \\(B\\)를 향해 출발해서 "\\(B\\) 시간'' \\(t\_B\\)에 \\(B\\)에서 \\(A\\)를 향해 반사되고, "\\(A\\) 시간'' \\(t'\_A\\)에 다시 \\(A\\)에 도착했다고 하자.

정의에 의해, 다음 조건을 만족할 때 두 시계는 동기화(synchronize)된다.
\\[
t\_B-t\_A=t'\_A-t\_B
\\]

이와 같은 정의가 모순이 없으며 임의의 갯수의 점들 사이에서도 이 정의에 따른 동기화가 가능하다고 가정한다.
또,
다음 관계가 보편적으로 성립한다고 하자.


1. \\(B\\)의 시계가 \\(A\\)의 시계와 동기화되면 \\(A\\)의 시계는 \\(B\\)의 시계와 동기화된다.
2. \\(A\\)의 시계가 \\(B\\)의 시계와 동기화되고 \\(C\\)의 시계와도 동기화되면 \\(B\\)와 \\(C\\)의 시계도 서로 동기화된다.

지금까지 가상적인 물리 실험을 통해, 서로 다른 장소에 있으며 서로에 대해 정지해 있는 시계가 동기화된다는 말에 의미를 주었고, 이를 통해 "동시(simultaneous)'', 즉 "동기화''와 "시간''에 관한 분명한 정의를 얻었다.
한 사건의 "시간''은 그 사건과 같은 위치에 있는 정지 시계(stationary clock)에 의해 동시에 발생하는 사건이다. 이 시계는 다른 특정한 정지 시계와 동기화되어 있어야 하며, 모든 시간 측정은 동기화된 측정이다.






경험적 사실에 따라,
\\[
\frac{2AB}{t'\_A-t\_A}
\\]
가 보편 상수---빈 공간에서의 빛의 속도---라고 가정하자.

시간을 정지 좌표계에서 정지해 있는 시계를 이용해서 정의한다는 사실이 중요하다.
정지 좌표계에 맞추어 정의되었으므로, 이 시간을 "정지 좌표계의 시간''이라고 부르자.

