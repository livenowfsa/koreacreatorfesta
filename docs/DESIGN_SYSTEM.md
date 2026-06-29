# Creator Square — 디자인 시스템

2026 크리에이터 미디어 대전 웹사이트용 기본 토대. 포스터에서 추출.

---

## 1. 컬러

### Spectrum (미디어 카테고리 포인트)
| 이름 | HEX | 용도 |
|---|---|---|
| Magenta | `#E12C84` | 영상 / 주요 강조 |
| Rose | `#EC6FA9` | 보조 핑크 |
| Violet | `#6F4DA8` | 방송 |
| Royal | `#2C6FD6` | 게임 / 링크 |
| Sky | `#4FA3E8` | 보조 블루 |
| Teal | `#18B6C9` | 음악 |
| Green | `#3FB44A` | 사진 |
| Lime | `#AECE3C` | 웹툰 |

### 그라데이션
- **Brand**: `linear-gradient(120deg, #6B3FA0, #2C6FD6)` — 로고, 주요 버튼
- **Full Spectrum**: `linear-gradient(120deg,#E12C84,#6F4DA8,#2C6FD6,#18B6C9,#3FB44A,#AECE3C)` — 히어로, 구분선
- **Pastel BG**: `linear-gradient(135deg,#FBE0EE 0%,#EDE2F6 32%,#DCE8F8 66%,#EAF3FC 100%)` — 페이지 배경

### 뉴트럴 / 잉크
| 이름 | HEX | 용도 |
|---|---|---|
| Ink | `#2B1E55` | 제목·본문 |
| Muted | `#6E6790` | 보조 텍스트 |
| Line | `#EDE7F6` | 구분선·면 |
| Surface | `#FFFFFF` | 카드 |

> 카테고리 칩은 스펙트럼 컬러 + 옅은 배경 쌍으로. 예: 영상 `#E12C84` / `#FBE4F0`, 게임 `#2C6FD6` / `#E3EDFC`.

---

## 2. 타이포그래피

**Pretendard** 단일 패밀리 (한글·영문·숫자 통합).
CDN: `https://cdn.jsdelivr.net/gh/orioncactus/pretendard@v1.3.9/dist/web/static/pretendard.css`

| 역할 | 굵기 / 크기 | letter-spacing |
|---|---|---|
| Display | 800 / 64px | -0.02em |
| Heading | 800 / 32px | -0.01em |
| Subhead | 700 / 22px | 0 |
| Body | 400 / 17px (line 1.7) | 0 |
| Caption | 600 / 13px | 0.02em |

위계는 **굵기 대비(800 ↔ 400)** 로. 색보다 굵기 먼저.

---

## 3. 형태 / 스페이싱

- **라운드**: 카드 20px, 인풋/태그 12px, 버튼 999px(풀 라운드)
- **그림자**: `0 18px 50px rgba(80,50,140,0.10)` (카드), `0 10px 24px rgba(72,80,200,0.30)` (주요 버튼)
- **섹션 간격**: 30px / 카드 내부 패딩 40–44px
- **컨테이너 폭**: max 1120px

---

## 4. 컴포넌트

- **Primary 버튼**: Brand 그라데이션 + 풀라운드 + 그림자
- **Secondary 버튼**: 솔리드 Magenta
- **Outline 버튼**: 흰 배경 + 2px Violet 보더
- **Ghost 버튼**: `#F3EEFA` 배경, 보더 없음
- **태그**: 스펙트럼 컬러 텍스트 + 옅은 배경, 풀라운드
- **카드**: 상단 그라데이션 썸네일 영역 + 하단 흰 본문, 태그 → 제목 → 설명 순서

---

## 5. 시그니처 모티프 (포인트로만, 절제)

- **글리치 워드마크**: `text-shadow: 2.5px 0 rgba(225,44,132,.55), -2.5px 0 rgba(44,111,214,.55)` + 미세 떨림
- **하프톤 도트**: `radial-gradient(circle, rgba(C,.5) 2px, transparent 2.2px); background-size:16px 16px` + 방향 마스크
- **파스텔 그라데이션 배경**
- **스파클(✦) 액센트**: 스펙트럼 컬러로 여백에
- **3D 미디어 오브제**: 헤드폰·게임패드·카메라·스피커·TV — PNG, 카테고리 컬러와 매칭

---

## 6. 행사 정보 (상수)

- 일시: 2026. 8. 28.(금) ~ 29.(토)
- 장소: 서울 마곡 코엑스 1F 전시장 & 마곡광장
- 주최: 방송미디어통신위원회 / 주관: 한국전파진흥협회(RAPA)
