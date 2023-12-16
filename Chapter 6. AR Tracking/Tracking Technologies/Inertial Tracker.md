
---
Inertial Tracker (관성 트래커)는 가속도계 및 자이로스코프와 같은 관성 센서를 사용하여 사용자의 위치 및 방향을 추적하는 기술이다. 이러한 트래커는 사용자의 움직임과 방향 변화를 감지하고 이 정보를 통해 위치 및 방향을 추정한다.

![[Inertial Tracker.png]]

[![video Label](https://img.youtube.com/vi/KqKa2Gc7lh8/0.jpg)

---
# 장점
## No Transmitter

Inertial Tracker가 사용자의 움직임과 방향을 추적하기 위해 외부 전파 송신기나 송신 장치를 필요로 하지 않는다.
## Cheap

관성 센서는 비교적 저렴하며, 이로 인해 Inertial Tracker 시스템의 비용이 낮을 수 있다.
## Small

Inertial Tracker 장치는 작고 경량이며, 이로 인해 휴대성이 뛰어나다.
## High Frequency

관성 센서는 높은 주파수로 데이터를 수집할 수 있으므로 고속 움직임을 추적하는데 적합하다.
## Wireless

Inertial Tracker는 외부 전파 송신기가 필요하지 않으므로 무선 연결을 지원한다. 이는 휴대성 및 사용자의 자유로운 움직임을 허용한다.

---
# 단점
## Drifts over time (시간에 따른 드리프트)

Inertial Tracker는 시간이 지남에 따라 오차가 누적되는 드리프트 현상을 겪을 수 있다. 이는 정확도를 저하시킬 수 있다.
## Hysteresis Effect (히스테리시스 효과)

일부 관성 센서는 히스테리시스 효과로 인해 이전 움직임에 따라 현재 움직임을 추적하는 데 영향을 줄 수 있다.
## Only 3 DOF

Inertial Tracker는 주로 3 DOF (3 Degrees of Freedom) 정보를 제공하며, 위치와 방향의 일부 측면에서는 제한적일 수 있다.