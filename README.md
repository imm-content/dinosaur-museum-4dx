# 공룡박물관 4DX | Dinosaur Museum 4DX

웹 브라우저에서 관람하는 3D 공룡 전시·체험관입니다. Three.js로 GLB 공룡 모델을 불러오고, 공룡의 움직임·입체 음향·카메라 진동·운석 연출을 결합했습니다. **실제 바람·물·좌석 진동 장치가 없는 웹 기반 ‘4DX 스타일’ 체험**입니다.

## 자연환경 배경 업데이트

기존 11개 GLB와 4개 전시관을 유지하면서 인공 원형 전시대를 제거하고 자연 지면 텍스처 및 사진풍 원경 4장을 추가했습니다. **일반 사진은 360도 파노라마가 아니므로 카메라를 돌릴 때 완전한 입체 숲처럼 보이지 않습니다.** 공룡은 Three.js 3D 객체로 유지됩니다.

배경 이미지 파일 4개를 반드시 `assets/backgrounds/`에 업로드하세요.

| 전시관 | 배경 파일 |
|---|---|
| 제1관 시간의 문 | `forest-entrance.jpg` |
| 제2관 초식공룡의 숲 | `herbivore-meadow.jpg` |
| 제3관 포식자의 계곡 | `predator-valley.jpg` |
| 제4관 멸종의 순간 | `extinction-wetland.jpg` |

백악기 풍경을 상상하여 생성한 시각 자료로, 실제 백악기 특정 장소를 과학적으로 복원한 이미지는 아닙니다.

## 실행

1. GitHub 저장소 `imm-content/dinosaur-museum-4dx` 루트에 `index.html`, `README.md`를 업로드합니다.
2. 루트의 `assets/` 폴더에 아래 표의 파일명 그대로 GLB 모델 11개를 배치합니다.
3. Settings → Pages → Deploy from a branch → `main` / `(root)` → Save.
4. 배포 주소: `https://imm-content.github.io/dinosaur-museum-4dx/` (Pages 활성화 후).

로컬에서는 HTML 파일을 더블클릭하기보다 VS Code Live Server 또는 `python -m http.server 8000`을 사용하세요.

## 기본 모델

| 파일명 | 역할 |
|---|---|
| `tyrannosaurus-rex.glb` | 티라노사우루스 |
| `triceratops.glb` | 트리케라톱스 |
| `stegosaurus.glb` | 스테고사우루스 |
| `brachiosaurus.glb` | 브라키오사우루스 |
| `jurassic_park_the_game_-_pteranodon.glb` | 익룡 |
| `pj_king_kong_-_brontosaurus.glb` | 브론토사우루스 |
| `pj_king_kong_-_vastatosaurus_rex_juvenille.glb` | 바스타토사우루스 |
| `jurassic_park_the_game_-_triceratops.glb` | 트리케라톱스 대체 모델 |
| `t_rex_with_rig.glb` | 티라노사우루스 대체 모델 |

`assets/sizeover/`는 이번 버전에서도 로드하지 않습니다. 일부 GLB는 제작자가 애니메이션을 포함하지 않았을 수 있습니다. 이때 전체 몸체의 가벼운 움직임을 코드로 연출합니다. 실제 모델의 방향·원점·애니메이션 상태는 모델별로 다르므로 브라우저에서 확인 후 조정할 수 있습니다.

## 추가 모델 (GitHub 업로드 완료)

| 로컬에서 사용할 파일명 | 역할 | 원본 파일 |
|---|---|---|
| `trex-jp.glb` | 포식자의 계곡: 티라노사우루스 실감 특별전 | 36,132KB |
| `protoceratops.glb` | 초식공룡의 숲: 프로토케라톱스 | `protoceratops_andrewsi_nhmw-geo-...` (원본 이름이 길어 변경) |

**등록 완료:** 신규 두 파일은 `assets/protoceratops.glb`, `assets/trex-jp.glb`로 GitHub `main` 브랜치에 등록되었습니다. 기존 9개 GLB의 이름과 경로는 변경하지 않습니다.

대용량 GLB 2개는 PowerShell Git으로 이미 업로드했습니다. 향후 파일 교체 시에도 Git을 사용하세요. GitHub Pages 배포 용량 및 브라우저 로딩 속도에 주의하세요. 파일을 공개 저장소에 올리기 전 원본 모델의 배포/상업 이용 허가를 확인해야 합니다.

## 조작법

- 전시관 선택: 화면의 전시 버튼
- 시점 회전: 마우스 드래그 / 손가락 드래그
- 확대·축소: 마우스 휠 / 두 손가락 핀치
- 공룡 선택: 공룡 클릭 또는 하단 카드
- 체험 버튼: 공룡 포효 / 운석 충돌
- 음향 및 한국어 음성 안내: 상단 버튼으로 켜고 끄기

## 기능

- 전시관 4개: 환영홀, 초식공룡, 육식공룡, 멸종 체험
- 여러 공룡 GLB의 비동기 로드, 개별 로드 실패 안내
- GLB 내장 애니메이션 자동 재생(있는 경우)
- 3D 공간에 배치된 전시대·조명·명판·환경, 관람 카메라 이동
- Web Audio 합성 효과음, 브라우저 음성 합성 내레이션(지원 기기에서)
- 화면 흔들림·섬광·운석 낙하 등 시각적 효과(강도 조절 가능)
- 반응형 모바일/PC 화면, 움직임 최소화 설정 존중

## 참고 사항

공룡 모델의 **저작권과 재배포·상업적 이용 허용 여부는 파일별 원 출처에서 확인**해야 합니다. 전자책이나 공개 GitHub에 모델을 포함하려면 해당 라이선스를 준수하고, 필요하면 출처·저작자·라이선스 파일을 별도로 기재하세요. 본 예제의 HTML 코드와 GLB 모델의 권리는 별개입니다.

인터넷 연결이 필요합니다(Three.js CDN). 첫 로딩 시 3D 파일 다운로드에 시간이 걸릴 수 있습니다. 휴대전화에서는 성능에 따라 모델 수를 줄이는 것이 좋습니다.

## 이번 HTML 수정 사항

- `index.html`에 `assets/protoceratops.glb`와 `assets/trex-jp.glb`를 연결했습니다.
- 기존 9개 GLB의 파일명, 전시 위치, 동작 코드는 유지합니다.
- 두 신규 모델은 각각 초식공룡의 숲과 포식자의 계곡에 배치되며, 총 11개 모델의 로딩을 시도합니다.
- 수정된 `index.html`과 `README.md`만 저장소 루트에 반영하면 됩니다.
