
---
Spatial Registration (공간 등록)은 증강 현실 (AR)에서 각 요소의 상대적인 위치를 정의하는 프로세스를 나타낸다. 이것은 AR 환경 내에서 다양한 요소의 위치와 방향을 결정하는 것을 의미한다. 이러한 요소에는 사용자, 사용자의 눈, 주변 환경(예: 테이블, 방, 건물), 물체 등이 포함된다.

Spatial Registration은 AR 환경에서 가상 및 현실의 위치 및 방향을 정확하게 결정하는 핵심 단계로, AR 경험의 정확성과 현실감을 보장하는 데 중요하다.

---
# Calibration (보정)

Spatial Registration은 AR 시스템의 초기 설정 단계에서 보통 보정(Calibration) 과정을 포함한다. 보정은 AR 장치와 환경 간의 관계를 정확하게 맞추기 위해 필요한 작업 중 하나 다. 이것은 각 요소가 AR 환경 내의 WCS, HCS, ECS와 같은 공통 좌표 체계에 대한 상대적인 위치를 정확하게 파악하기 위해 수행된다.

- WCS (World Coordinate System, 전역 좌표계)
- HCS (Head Coordinate System, 머리 좌표계)
- ECS (Eye Coordinate System, 눈 좌표계)

![[AR Tracking_Spatial Registration.png]]

---
# 3D/6D Tracking (6 자유도)

Position (위치)
- 1DOF : 앞, 뒤 이동 (Y 수직)
- 2DOF: 좌, 위 이동 (X 수평)
- 3DOF: 상, 하 운동 (Z 깊이)

Orientation (회전, 기울기)
- 4DOF: 앞, 뒤 기울기 (Pitch)
- 5DOF: 좌, 우 기울기 (Roll)
- 6DOF: 좌, 우 회전 (Yaw)

![[Spatial Registration_6DOF.jpg]]

---
# Registration Problem

증강 현실(AR)은 가상 콘텐츠와 실제 세계 객체가 사용자의 시야 내에서 정확하게 정렬되는 것을 보장해야 한다. 이를 Registration Problem 이라 한다.

만약 정렬이 제대로 이루어지지 않으면 다음의 문제가 발생할 수 있다.
- 환상의 파괴
- 현실감 상실
- 효과성 감소

## Source of Registration Errors

- [[Static Errors (정적 에러)]]
- [[Dynamic Errors (동적 에러)]]

---
