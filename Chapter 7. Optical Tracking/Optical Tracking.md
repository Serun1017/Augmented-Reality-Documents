
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

- Keypoint (주요점)
- Descriptors (기술자)

---
# Common AR Optical Tracking Types
## [[Marker Tracking]]

- 마커 트래킹은 이미지 기반 마커나 마커 패턴을 사용하여 가상 콘텐츠를 추적하는 기술이다. 이러한 마커는 주로 인식 가능한 패턴이며, 카메라 이를 감지하여 해당 위치에 가상 객체를 표시한다.

![[Marker-based AR.jpg]]
## [[Markerless Tracking]]

- 마커리스 트래킹은 이미지 기반 마커 없이도 현실 세계의 특징을 사용하여 가상 콘텐츠를 추적하는 기술이다. 이를 위해 실제 환경에서 이미 알려진 특징을 사용하여 위치를 추적하고 가상 객체를 배치한다.

![[Image Tracking AR.png]]
## Unprepared Tracking

- Unprepared Tracking은 알려진 특징이나 마커 없이도 알려지지 않은 환경에서 가상 객체를 추적하는 기술이다.
- Simultaneous Localization and Mappint (SLAM)과 같은 기술을 사용하여 카메라 및 센서 데이터를 활용하여 실시간으로 환경을 모델링하고 가상 객체를 배치한다.

![[Markerless AR.png]]

---
# Marker vs. Natural Feature Tracking

## Marker Tracking
- Markers can be an eye-catcher
- Tracking is less demanding
- The environment must be instrumented
- Markers usually work only when fully in view

## Natural Feature Tracking
- Natural feature targets might catch the attention less
- Natural feature targets are potentially everywhere
- Natural feature targets also work if partially in view

---
# Visual Tracking Approaches

## Marker-based tracking with artificial features
- Make an model before tracking
- eg. marker

## Model-based tracking with natural features
- Acquire a model before tracking
- eg. poster

## Simultaneous localization and mapping
- Build a model while tracking it

---
# Edge/Model Based Tracking

## RAPiD

![1999 Real-time 3D model tracker (youtube.com)](https://www.youtube.com/watch?v=Z1J0VLizVDs)
1. Based on a CAD model of the structure
2. The CAD model is rendered from a predicted viewpoint
3. Identify the edges of the model that are expected to be visible
4. The search is conducted from each sample point for an intensity discontinuity in the video image
5. A change in the pose is computed which minimizes these errors

---
# Model Based Tracking

- Tracking from 3D Object shape
- Eg. OpenTL

![Model plane tracking using contours and stereo camera setup - YouTube](https://www.youtube.com/watch?v=laiykNbPkgg&feature=youtu.be)

![3D Face and gaze tracking (youtube.com)](https://www.youtube.com/watch?v=WIoGdhkfNVE)

## How to Create Model Target
![Vuforia Engine: How to Create Model Targets (youtube.com)](https://www.youtube.com/watch?v=jbaUDMvv2Zw)

---
# Tracking from an Unknown Environment

## [[SLAM|SLAM (Simultaneously Localize And Map the environment)]]

SLAM(Simultaneous Localization And Mapping)은 동시적 위치추정 및 지도 작성 기술이다. SLAM은 로봇이나 이동체가 알려지지 않은 환경에서 자신의 위치를 추정하면서 동시에 환경의 지도를 작성하는 기술이며, 컴퓨터 비전, 로봇학,. 증강 현실, 가상 현실 등 다양한 응용 분야에서 사용된다.

---
# Feature-Based vs. Direct Method
## Feature-Based
- Feature-Based Method는 주로 이미지의 모서리나 코너 주변의 작은 패치를 사용한다.
- 주로 코너와 같은 특징점을 사용하여 추적 및 재구성을 수행한다.
- 연산이 빠르며 빠른 추적이 가능하다.
- 유연하게 이상치(outliers)를 후퇴적으로 제거할 수 있다.
- 모델이나 시스템의 불일치에 대해 강건하다.
- 상대적으로 덜 완전한 정보에 기반하여 결정된다.
- 초기화에 대한 강한 의존성이 없다.

## Direct Method
- 전체 이미지 정보를 사용한다.
- 전체 이미지를 사용하여 추적하고 재구성한다.
- 연산이 느리지만 병렬 처리에 적합하다.
- 후퇴적으로 이상치를 제거하기 어렵다.
- 모델이나 시스템의 불일치에 대해 강건하지 않다.
- 더 완전한 정보에 기반하여 결정된다.
- 초기화에 좋은 정보가 필요하다.

![[Feature-Based vs. Direct Method.png]]