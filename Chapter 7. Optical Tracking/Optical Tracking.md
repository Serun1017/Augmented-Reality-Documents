
---
Optical Tracking (광학 추적)은 증강 현실(AR)에서 사용되는 중요한 기술 중 하나이며, 다음과 같은 이유로 AR 디바이스에서 광학 추적을 사용하는 것이 유용하다.

## Many AR Devices have Cameras

많은 AR 디바이스 (예: 스마트폰, 태블릿, 비디오 시각 투과(VST) 디스플레이)는 내장 카메라를 가지고 있다. 이러한 카메라는 주변 환경을 촬영하고 비디오 스트림을 생성하는 데 사용된다.
## Provide precise alignment between video and AR overlay

광학 추적을 사용하면 비디오 스트림과 AR 오버레이를 픽셀 수준에서 정확하게 정렬할 수 있다. 이것은 실제 세계에서 촬영된 환경과 가상 콘텐츠를 정확하게 일치시키는 데 도움이 된다.
## Computer Vision is a well-established discipline

컴퓨터 비전은 이미 오랜 기간 동안 연구되어 왔으며 더 많은 연구와 개발로 발전해왔다. 따라서 컴퓨터 비전 기술을 사용하여 AR 환경에서 시각적 특징을 추적하는 것은 실용적이며 정확한 방법이다.

---
# [[Visual Feature (시각적 특징)]]

- [[Keypoint (주요점)]]
- [[Descriptors (기술자)]]

---
# Common AR Optical Tracking Types
## [[Marker Tracking]]

- 마커 트래킹은 이미지 기반 마커나 마커 패턴을 사용하여 가상 콘텐츠를 추적하는 기술이다. 이러한 마커는 주로 인식 가능한 패턴이며, 카메라 이를 감지하여 해당 위치에 가상 객체를 표시한다.

![[Marker-based AR.jpg]]
## Markerless Tracking

- 마커리스 트래킹은 이미지 기반 마커 없이도 현실 세계의 특징을 사용하여 가상 콘텐츠를 추적하는 기술이다. 이를 위해 실제 환경에서 이미 알려진 특징을 사용하여 위치를 추적하고 가상 객체를 배치한다.

![[Image Tracking AR.png]]
## Unprepared Tracking

- Unprepared Tracking은 알려진 특징이나 마커 없이도 알려지지 않은 환경에서 가상 객체를 추적하는 기술이다.
- Simultaneous Localization and Mappint (SLAM)과 같은 기술을 사용하여 카메라 및 센서 데이터를 활용하여 실시간으로 환경을 모델링하고 가상 객체를 배치한다.

![[Markerless AR.png]]

---
