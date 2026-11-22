# 살아있는 공룡박물관 4DX — 백악기 사진 배경 버전

GitHub Pages: https://imm-content.github.io/dinosaur-museum-4dx/

## 이번 수정의 핵심

기존의 만화풍 삼각형 나무, 바위, 인공 전시대 및 색칠된 지면을 **제거**했습니다. 전시관마다 실제 저장소에 업로드된 백악기 풍경 PNG를 **화면 전체 사진 배경**으로 보여주며, 투명한 Three.js 캔버스 위에 기존 GLB 공룡 11종을 표시합니다.

| 전시관 | 배경 경로 |
|---|---|
| 01 시간의 문 | `assets/backgrounds/cretaceous-forest.png` |
| 02 초식공룡의 숲 | `assets/backgrounds/cretaceous-waterfall.png` |
| 03 포식자의 계곡 | `assets/backgrounds/cretaceous-meadow.png` |
| 04 멸종의 순간 | `assets/backgrounds/cretaceous-volcano.png` |

**중요:** 배경은 2D 이미지입니다. 공룡은 실제 3D GLB로 회전·확대할 수 있지만, 카메라 회전으로 배경의 다른 면이 보이거나 사진 속 나무 뒤로 공룡이 들어가지는 않습니다. 사진과 3D 모델 사이에 시점·지면·그림자 차이가 남을 수 있습니다. 완전한 360도 자연환경을 위해서는 별도의 3D 지형·식생 에셋 또는 360도 파노라마가 필요합니다.

## 공룡 모델 11개 (파일명 유지)

| 모델 | GLB 파일명 |
|---|---|
| 브라키오사우루스 | `brachiosaurus.glb` |
| 트리케라톱스 | `triceratops.glb` |
| 스테고사우루스 | `stegosaurus.glb` |
| 티라노사우루스 | `tyrannosaurus-rex.glb` |
| 프테라노돈 | `jurassic_park_the_game_-_pteranodon.glb` |
| 브론토사우루스 | `pj_king_kong_-_brontosaurus.glb` |
| 바스타토사우루스 (영화 속 가상 공룡) | `pj_king_kong_-_vastatosaurus_rex_juvenille.glb` |
| 트리케라톱스 특별전 | `jurassic_park_the_game_-_triceratops.glb` |
| 티라노사우루스 특별전 | `t_rex_with_rig.glb` |
| 프로토케라톱스 | `protoceratops.glb` |
| 티라노사우루스 실감 특별전 | `trex-jp.glb` |

기존 GLB 파일은 모두 `assets/`에 두며, 이름을 바꾸지 않습니다. 내부 애니메이션이 있으면 자동 재생합니다. 일부 모델은 애니메이션이 없을 수 있습니다.

## 주요 기능

- 4개 전시관 전환, 11개 공룡 카드 선택, 공룡 클릭
- 마우스 드래그/휠 또는 터치로 3D 공룡 시점 조절
- 포효 합성 효과음, 카메라 흔들림, 운석 낙하/섬광
- 한국어 음성 안내 (브라우저 TTS)
- 효과음·음성·진동 켜기/끄기

실제 4DX 극장의 물리적 바람·물·좌석 진동은 구현되지 않은 **웹 기반 4DX 스타일 체험**입니다.

## GitHub 반영

이미 배경 PNG 4장과 GLB 11개가 저장소에 있다면, **루트의 `index.html`과 `README.md` 두 파일만 교체**하면 됩니다. GitHub 웹에서 파일별로 편집·업로드하거나, 로컬 복제 저장소에서 다음 명령어를 사용하세요.

```powershell
cd C:\Users\82106\dinosaur-museum-4dx-git
git add index.html README.md
git commit -m "Use photographic Cretaceous backgrounds"
git push origin main
```

반영 후 `Ctrl+F5`로 강력 새로고침합니다. 배경 파일 경로와 대소문자는 정확히 일치해야 합니다.

## 참고 및 권리

백악기 이미지는 상상 기반 생성 이미지이며, 특정 시대·지역의 엄밀한 과학적 복원은 아닙니다. 각 GLB 모델의 원저작자 라이선스와 공개 재배포·상업적 이용 조건을 별도로 확인하세요.
