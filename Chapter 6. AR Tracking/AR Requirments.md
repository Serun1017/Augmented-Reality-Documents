
---
# Registration (등록)

- Positioning virtual object wrt real world
  - AR 시스템은 가상 객체의 위치를 현실 세계와 일치 시켜야 한다.
  - 즉, 사용자가 볼 때 가상 객체가 정확한 위치에 나타나야 한다.
- Fixing Virtual object on real object when view is fixed
  - 사용자가 뷰를 고정한 경우, AR 시스템은 가상 객체를 해당 위치에 고정 시켜야 한다.
  - 이것은 사용자가 움직일 때도 가상 객체가 일치하는 위치에 머무르도록 하는 중요한 단계이다.

---
# Calibration (보정)

- Offline measurments
  - AR 시스템은 HMD (Head-Mounted Display) 카메라와 사용자의 눈 간의 상대적 위치 및 관찰 각도와 같은 오프라인 측정을 수행한다.
- Measure camera relative to HMD
  - AR 시스템은 카메라와 HMD 사이의 관계를 측정하여 사용자 시야와 카메라의 관계를 파악한다.

---
# Tracking (추적)

- Continually locating the user's viewpoint when view moving
  - AR 시스템은 사용자의 뷰 포인트를 지속적을 추적하여 사용자의 시야가 이동할 때 가상 객체의 위치와 방향을 조정한다.
- Position (x, y, z). Orientation (r, p, y)
  - AR 시스템은 사용자의 위치와 방향을 계속 추적하여 가상 객체를 정확하게 표시한다.
  - 이 정보는 위치와 방향의 3D 좌표로 표시된다.