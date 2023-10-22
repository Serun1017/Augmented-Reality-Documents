
---
# Local Object Coordinate

Local Object Coordinate는 개발 가상 물체에 대한 지역 좌표계이다. 각 가상 물체는 자체의 지역 좌표계를 가짐, 이 좌표계는 해다 물체의 위치와 방향을 정의한다.

## Model Transformation

- 가상 물체의 위치, 방향 및 크기를 정의하고 Local Object Coordinate를 Global World Coordinates로 변환하는 프로세스이다.

---
# Global World Coordinates

Global World Coordinates는 AR 환경에서 모든 물체에 대한 공통 기준점을 제공한다. 이는 전역 좌표계로 모든 물체의 위치와 방향을 현실 세계와 관련하여 정의한다.

## View Transformation

- 가상 물체의 움직임, Observer의 움직임에 따라 변하는 가상 물체의 좌표를 Global World Coordinate에서 Eye Coordinate에 맞도록 편환하는 프로세스이다.

---
# Eye Coordinates

Eye Coordinates는 카메라 및 디스플레이와 관련이 있으며, 사용자의 시각을 기반으로 좌표를 정의한다. 이 좌표계는 카메라와 디스플레이를 포함한 장치의 위치와 방향을 정의한다.

## Perspective Transformation

- Perspective Transformation은 AR 장치 (예: 카메라 렌즈)와 사용자의 눈 위치에 관한 정보를 고려하여 Eye Coordinate를 디스플레이에 맞도록 변환한다. 이 과정은 원근 효과를 적용하고 가상 객체를 화면에서 올바르게 보이도록 조정한다.

![[AR Tracking_Coordinate Systems.png]]