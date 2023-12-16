
---
SLAM(Simultaneous Localization And Mapping)은 동시적 위치추정 및 지도 작성 기술이다. SLAM은 로봇이나 이동체가 알려지지 않은 환경에서 자신의 위치를 추정하면서 동시에 환경의 지도를 작성하는 기술이며, 컴퓨터 비전, 로봇학,. 증강 현실, 가상 현실 등 다양한 응용 분야에서 사용된다.
## Goal
- 로봇이 초기에 위치와 지도를 알지 못하는 상태에서, 카메라나 센서를 사용하여 카메라의 위치 및 지도의 구조를 동시에 복원하는 것
## Mapping
- 로봇이 있는 환경의 지도를 구축한다.
- 초기에는 지도에 대한 정보가 없으며, 로봇의 이동에 따라 환경의 구조를 추정하여 지도를 만든다
## Localization
- 로봇이 환경에서 이동할 때, 현재 위치와 방향을 추정하여 지도를 기반으로 환경을 탐색한다.

이를 수행하기 위해 Parallel Tracking and Mapping이 사용된다.

---
# Visual SLAM
### Early SLAM systems (1986~)
- Computer visions and sensors (e.g. IMU, laser, etc.)
- One of the most important algorithms in robotics

### Visual SLAM
- Using cameras only, such as stereo view
- Mono SLAM (single camera) developed in 2007 (Davidson)

## Kudan MonoSLAM
![KudanSLAM: Meeting room (youtube.com)](https://www.youtube.com/watch?v=g2SFJGDz9cQ)

---
# How SLAM Works

## Tracking a set of points through successive camera frames
- 연속된 카메라 프레임 간에 특정 지점 들을 추적한다.
- 이는 객체나 환경의 특징을 나타내는 키 포인트 또는 특징점들을 의미한다.

## Using these tracks to traingulate their 3D position
- 추적된 특징점들의 이동을 기반으로 이를 삼각화하여 3D 공간에서의 위치를 계산한다.
- 이로써 각 특징점의 3D 좌표를 얻을 수 있다.

## Simultaneously use the estimated point locations to calculate the camera pose which could have observed them
- 추정된 3D 점들의 위치를 사용하여 각 프레임에서의 카메라의 위치와 방향, 즉 카메라 포즈를 계산한다.
- 이는 카메라의 움직임을 추정하는 데 사용된다.

## By observing enough points can solve for both structure and motion (camera path and scene structure)
- 충분한 수의 특징점을 관찰함으로서 SLAM은 구조(환경의 3D 구조)와 움직임(카메라의 이동 및 회전)을 모두 추정할 수 있다. 
- 이를 통해 로봇이나 이동체가 환경을 이해하고 그 동안의 움직임을 추적할 수 있다.

---
# Framework of Traditional VSLAM

![[Framework of Traditional VSLAM.png]]

---
# Evolution of SLAM Systems

## MonoSLAM (Davisdon, 2007)
- Real-time SLAM from a single camera
![Object tracking with monoSLAM: Ashmolean Gallery (youtube.com)](https://www.youtube.com/watch?v=saUE7JHU3P0)

## PTAM (Klein, 2007)
- First SLAM implementation on mobile phone

## FAB-MAP (Fast Apperance Based Mapping, Cummins, 2008)
- Probabilistic localization and mapping

## DTAM (Dense Tracking And Mapping, Newcombe, 2011)
- 3D surface reconstruction from every pixel in an image

## Deep learning-based SLAM systems (2010s - present)
- Use machine learning algorithms to extract features from sensor data and to build maps

---
# LSD-SLAM (Eagel 2014)

- Large-Scale Direct monocular SLAM technique
- LSD-SLAM은 큰 규모의 환경에서 단일 카메라를 사용하여 SLAM을 수행한다. 이는 로봇이나 이동체가 매우 넓은 영역을 이동하면서 환경을 이해하고 지도를 작성할 수 있음을 의미한다.
- 카메라 추적 및 지도 작성에 이미지 강도(Image Intensity)를 사용한다. 이는 주변 환경의 명암을 활용하여 카메라의 움직임을 추적하고 지도를 작성한다.
- 카메라 추적은 직접적인 이미지 정렬(direct image alignment)을 사용한다. 이는 특징이나 키포인트를 사용하지 않고도 이미지 자체의 명암을 활용하여 카메라의 상대적인 움직임을 추정한다
- 지도 작성에서는 반밀도(semi-dense)의 깊이 맵을 추정한다. 이는 환경의 3D 구조를 비교적 밀도 높게 표현하는 방식이다.
- 매우 큰 규모의 환경에서도 효과적으로 추적이 가능하며, 실시간으로 CPU 및 스마트폰에서 실행될 수 있다.

![LSD-SLAM: Large-Scale Direct Monocular SLAM (ECCV '14) (youtube.com)](https://www.youtube.com/watch?v=GnuQzP3gty4)

---
# Application of SLAM Systems

## Many possible applications
- Augmented Reality camera tracking
- Mobile robot localization
- Real world navigation aid
- 3D scene reconstruction
- 3D object reconstruction
- ...

## Assumptions
- Camera moves through an unchanging scene
- Not suitable for person tracking, gesture recognition

---
# Hybrid Tracking

- Combining several tracking modalities together

## Combining Sensors and Vision

### Sensors
- 센서는 종종 노이즈가 있는 출력을 생성할 수 있다. 이는 사용자의 위치나 주변 환경의 정보에 불안정성을 초래할 수 있다. 이러한 불안정성은 객체의 떨림 현상(Jittering)으로 이어질 수 있다. 
- 센서의 출력은 항상 정확하지 않을 수 있다. 잘못된 위치 정보가 제공될 수 있으며 이는 증강 객체의 잘못된 배치로 이어질 수 있다.
- 센서는 사용자가 세계 어디에 있는지 및 사용자가 어떤 것을 보고 있는지 에 대한 첫 번째 정보를 제공한다. 이는 초기 위치 정보를 얻고 사용자의 시선 방향을 파악하는 데 도움이 된다.

### Vision
- 컴퓨터 비전은 일반적으로 더 정확한 결과를 제공할 수 있다. 이는 안정적이며 올바른 증강을 생성할 수 있게 해준다.
- 비전을 올바른 키포인트 데이터베이스를 선택해야 한다. 키포인트는 이미지에서 특정한 지점이나 특징을 나타내며, 이를 사용하여 객체를 추적한다.
- 비전을 로컬 좌표 프레임(online-generated model)을 전역 좌표 프레임(world coordinate)에 등록해야 한다. 이는 로컬에서 추적된 정보를 전체 세계 좌표계로 매핑하는 과정을 나타낸다.

## Outdoor AR Tracking System
![[Outdoor AR Tracking System.png]]

---
# Types of Sensor Fusion
## Complemtary (보완적 센서 퓨전)
### Combine sensors with different degrees of freedom (자유도가 다른 센서 결합)
- 이 방법은 서로 다른 자유도를 가진 센서를 결합한다.
- 예를 들어, 위치만 측정하는 센서와 방향(orientation)만 측정하는 센서를 결합할 수 있다.
### Sensors must by synchronized (or require inter-/extrapolation)
- 센서들은 동기화되어야 하거나 상호/외삽이 필요하다.
- 데이터의 동기화가 중요하며, 센서 간의 시간적 불일치를 보정하기 위해 상호/외삽 기술이 사용될 수 있다.
### Example
- 위치 정보만 측정하는 센서와 방향 정보만 측정하는 센서를 결합할 수 있다.
- 자이로스코프나 자기계 등과 같이 직교하는 1차원 센서들을 보완적으로 사용하는 것도 가능하다.

## Competitive (경쟁적 센서 퓨전)
### Different sensor types measure the same degree of freedom
- 이 방버은 서로 다른 유형의 센서가 동일한 자유도를 측정할 때 사용된다.
### Redundant sensor fusion: Use worse sensor only if better sensor is unavailable
- 여러 센서가 동일한 정보를 제공하는 경우, 더 좋은 센서를 사용하다가 이용할 수 없을 때 정확한 센서를 사용한다.
### Statistical sensor fusion
- 통계적인 방법을 사용하여 센서들의 측정값을 통합한다.

---
# Example: Outdoor Hybrid Tracking

- Combine computer vision and inertial gyroscope sensors
- Both correct for each other
	- Inertial gyro
		- provides frame-to-frame prediction of camera, orientation, fast sensing
		- Drifts over time
	- Computer vision
		- Natural features tracking, corrects for gyro drift
		- Slower, less accurate

## Robust Outdoor Tracking
### Hybrid Tracking
- Computer vision
- GPS
- inertial
