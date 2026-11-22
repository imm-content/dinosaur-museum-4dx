# 살아있는 공룡박물관 4DX

실제 GLB 모델 11개와 백악기 자연환경 이미지 4개를 이용한 웹 기반 실감형 전시입니다.

## 전시관

1. 시간의 문 — 초식공룡 미리보기 (`cretaceous-forest.png`)
2. 초식공룡의 숲 — 브라키오사우루스, 트리케라톱스, 스테고사우루스, 브론토사우루스, 프로토케라톱스 (`cretaceous-waterfall.png`)
3. 포식자의 계곡 — 티라노사우루스 등과 프테라노돈 (`cretaceous-meadow.png`)
4. 멸종의 순간 — 트리케라톱스 특별전, 리깅된 티라노사우루스, 운석 충돌 (`cretaceous-volcano.png`)

## 조작 방법

- 공룡 클릭: 해당 공룡 선택, 상세 설명 및 카메라 접근
- **공룡 위에서 드래그: 해당 공룡만 회전**
- **공룡이 없는 공간에서 드래그: 카메라 시점 회전**
- 마우스 휠: 확대/축소
- 왼쪽 전시관 메뉴: 관별 공룡만 표시
- 하단 카드: 개별 공룡 선택
- 상단 버튼: 효과음, 음성 안내, 진동 효과, 시점 초기화

## 파일 구조

```text
index.html
README.md
assets/
  *.glb  (공룡 모델 11개)
  backgrounds/
    cretaceous-forest.png
    cretaceous-waterfall.png
    cretaceous-meadow.png
    cretaceous-volcano.png
```

## 구현 참고

Three.js와 GLTFLoader를 사용합니다. 각 공룡은 독립된 3D 객체로 로딩되며, 전시관별 표시 여부를 구분합니다. 원본 GLB에 포함된 애니메이션은 해당 모델의 AnimationMixer로 재생됩니다. 화면 진동은 브라우저 카메라 효과이며 물리적인 4DX 장비 제어는 아닙니다.

사진 배경은 2D 이미지이므로 실제 360도 지형이나 자유보행 환경은 아닙니다. GLB 및 이미지의 배포 라이선스를 별도 확인하십시오.

## 실행

GitHub Pages: https://imm-content.github.io/dinosaur-museum-4dx/
