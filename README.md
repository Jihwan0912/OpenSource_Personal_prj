# 안구건조증 예방 프로그램

## 사용자의 안구 건강을 보조하는 것을 목표로 하는 프로젝트입니다.
---------------------------------
### 작동 방식
- 카메라를 통해 사용자의 얼굴과 눈을 인식
- 사용자의 눈깜박임을 감지
- 눈깜박임의 횟수가 기준치보다 적으면  팝업창을 출력
--------------------------------
### 활용 라이브러리
- OpenCV
    - Haar Cascade 객체 검출기를 사용해 사용자의 **얼굴**을 인식
```python
import cv2
face_cascade_name = './haarcascade_frontalface_default.xml'
```

- dlib
    - 사용자의 얼굴에서 **눈**을 인식
```python
import dlib
predictor_file = './shape_predictor_68_face_landmarks.dat'
```

- EAR 알고리즘
    - 인식한 눈의 종횡비를 계산하고, 이를 토대로 **눈깜박임**을 인식

