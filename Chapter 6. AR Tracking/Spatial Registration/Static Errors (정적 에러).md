
---
Static Errors (정적 에러)는 증강 현실 (AR) 시스템에서 가상 객체와 현실 세계를 정확하게 정렬하는 과정에서 발생할 수 있는 고정된 에러 또는 오차를 나타낸다. 이러한 정적 오차는 시스템 구성과 보정 단계에서 발생할 수 있으며, 사용자 경험을 저해하거나 왜곡 시키는 원인이 될 수 있다.

---
# Static Errors (정적 에러)
## Optical Distortions (in HMD)

- HMD(Head-Mounted Display)의 렌즈나 광학 시스템 내에서 발생하는 왜곡은 가상 콘텐츠의 외관을 왜곡 시키고, 정확한 정렬을 방해할 수 있다.

![[Static Errors_Distortion.png]]
## Mechnical Misalignments

- 하드웨어 구성 요소, 특히 HMD의 부품 간의 미세한 정렬 오류나 물리적 오차는 정확한 정렬을 방해할 수 있다.
## Track Errors

- AR 시스템 내의 추적 센서나 카메라 시스템의 오차는 가상 콘텐츠의 정확한 위치를 결정하는 데 영향을 미칠 수 있다.
## Incorrect Viewing Parameters

- 가상 콘텐츠를 표시하는 데 사용되는 시간 매개 변수의 부정확한 설정은 정확한 정렬을 방해할 수 있다.
- 시각 매게 변수
  - Field of View (시야각)
  - Center of Projection (투영 중심)
  - Interpupillary Distance (눈 사이의 거리) 등

---
# Reducing Static Errors

## Distortion Compensation (왜곡 보정)

- 렌즈 또는 디스플레이 내에서 발생하는 광학 왜곡을 보상하는 기술을 사용한다.
- 이를 통해 가상 콘텐츠가 실제 세계와 정확하게 정렬되도록 한다.
## Manual Adjustments (수동 조정)

- 사용자에게 수동으로 AR 및 VR 콘텐츠를 정렬하도록 지시한다.
- 이것은 사용자가 개입하여 정적 에러를 보정할 수 있게 한다.
## View-Based or Direct Measurments (시야 기반 또는 직접적인 측정)

- 사용자에게 눈 위치를 직접 측정하도록 요청하여 정확한 위치 정보를 제공하고 가상 콘텐츠를 정렬한다.

![[Static Errors_View-Based Calibration(Azuma 94).png]]
## Camera Callibration (카메라 보정, 비디오 AR)

- 카메라 속성을 측정하고 분석하여 정적 에러를 보정하는 기술을 사용한다.
- 이는 비디오 AR(카메라 영상을 기반으로 하는 AR)에서 주로 사용된다.

