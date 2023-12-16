
---
Markerless Tracking은 특정한 마커나 태그를 사용하지 않고도 객체 또는 특징점을 식별하고 추적하는 기술이다.

![[Markerless Tracking.png]]

---
# Natural Feature Tracking

Natural Feature Tracking은 주로 환경의 자연 특징점(keypoints)을 활용하여 객체나 장면을 추적하는 데 사용되는 Markerless Tracking의 한 형태이다. 이 방법은 환경에서 미리 정의된 마커 대신에 주변의 고유한 특징을 기반으로 한다. 주로 사용되는 자연 특징점(keypoints)는 이미지에서 찾을 수 있는 고유한 구조나 패턴이며, 주로 다음과 같은 특징이 있다.

1. 고유성(Uniquness)
   - 특징점은 다른 지점들과 비교했을 때 고유하게 식별 가능한 특성을 가지고 있어야 한다.
2. 불변성(Invariance)
   - 특징점은 회전, 크기, 변화, 조명 변화 등에 대해 일정한 특징을 유지하는 것이 중요하다.
3. 견고성(Robustness)
   - 환경의 변화에 대해 강건하게 작동할 수 있어야 한다.

## 단계
### Feature Extraction (특징점 추출)
- 입력 이미지에서 고유한 특징점을 추출한다.
- 이 특징점은 주로 코너난 엣지와 같은 환경의 고유한 구조를 나타낸다. (Edges, Surface Textures, Interest Points)

### Feature Description (특징점 설명)
- 추출된 특징점을 설명하는 특징 벡터를 생성한다.
- 이 특징 벡터는 해당 특징점을 고유하게 식별하는 데 사용된다.

### Matching (매칭)
- 현재 프레임과 이전 프레임에서 추출된 특징점들을 매칭하여 객체 또는 장면의 이동을 추적한다.

### Tracking (추적)
- 매칭된 특징점을 사용하여 객체 또는 장면의 이동을 추적하고 위치를 업데이트 한다.

## Natural Features

1. Detect salient interest points in an image (특이 관심 지점 탐지)
   - salient interest points는 이미지 내에서 두드러지게 나타나는 부분으로, 이미지에서 주목할 만한 특징을 나타낸다.
   - 이 특이 관심 지점은 쉽게 찾을 수 있어야 한다.
   - 뷰포인트가 변경될 때에도 이미지 내의 해당 지점의 위치는 상대적으로 안정적으로 유지되어야 한다.
   - 텍스처가 풍부한 표면에서 더 잘 작동하며, 또는 가장자리 특징을 사용할 수도 있다.
2. Match interest points to tracking model database (관심 지점을 추적 모델 데이터베이스에 매칭)
   - 3D 재구성 결과를 담은 데이터베이스가 존재한다
   - 전체 또는 부분 이미지를 매칭하는 것은 계산 비용이 많이 들기 때문에, 일반적으로 관심 지점은 'Descriptor'로 컴파일 된다.
   - Descriptor은 특이 관심 지점을 설명하는 특징 벡터로, 매칭을 용이하게 만든다.
![[Natural Features.png]]

## Tracking by Keypoint Detection
Tracking by Keypoint Detection은 객체 추적을 위해 키 포인트를 감지하고 이를 사용하여 객체의 운동을 추적하는 기술이다.

### Keypoint Detection (키포인트 감지)
- 이미지나 비디오에서 특정 지점이나 특징을 감지한다. 이 지점은 주로 이미지에서 고유하거나 두드러진 부분으로 선택된다
- 키 포인트는 쉽게 찾을 수 있어야 하며, 이미지 내에서 변하지 않는 특징을 가져야 한다.

### Keypoint Description (키포인트 설명)
- 감지된 키 포인트를 설명하는 특징 벡터를 생성한다. 이 특징 벡터는 키 포인트를 고유하게 식별하고 다른 키 포인트와의 매칭에 사용된다.
- 대표적인 키포인트 설명 알고리즘으로는 SIFT(Scale-Invariant Feature Transform), SURF(Speeded-Up Robust Features), ORB(Oriented FAST and Rotated BRIEF) 등이 있다

### Keypoint Matching (키포인트 매칭)
- 현재 프레임과 이전 프레임에서 감지된 키 포인트들을 매칭하여 객체의 이동을 추적한다
- 키포인트 간의 거리나 유사도를 기반으로 매칭이 이루어진다.

### Object Tracking (객체 추적)
- 매칭된 키 포인트를 사용하여 객체의 운동을 추적한다.

![[Tracking by Keypoint Detection.png]]

## Detection and Tracking
- Tracking 과 Detection은 상호보완적인 관계이다.
- 성공적인 검출 후에는 대상을 점진적으로 추적하다가 대상이 손실 되면 다시 검출을 활성화한다.
![[Detection and Tracking.png]]

---
# Example
## Texture Tracking

![[Texture Tracking.png]]

## Vuforia Texture Tracking

![video Label](https://img.youtube.com/vi/1Qf5Qew5zSU/0.jpg)

