# 2026 크리에이터 미디어 대전

영상 · 방송 · 게임 · 음악 · 사진 · 웹툰 — 미디어 크리에이터와 팬이 모이는 페스티벌 공식 웹사이트.

**🌐 배포 주소:** https://livenowfsa.github.io/koreacreatorfesta/

- **일시:** 2026. 8. 28.(금) ~ 29.(토)
- **장소:** 서울 마곡 코엑스 1F 전시장 & 마곡광장

---

## 페이지 구성

| 카테고리 | 파일 |
|---|---|
| 메인 | `index.html` |
| 행사 소개 | `about.html` (행사개요 · 오시는 길 · 지난 행사) |
| 프로그램 | `program.html` (시간표 ⇄ 상세 프로그램 토글, Day 전환) |
| 참가기업 | `companies.html`(참가안내) · `companies-list.html`(기업리스트) |
| 참관객 | `register.html`(사전등록 안내) · `register-form.html`(사전등록) |
| 크리에이터 | `creators.html`(리스트) · `creators-register.html`(사전등록) |
| 고객지원 | `support-center.html`(공지사항) · `support-faq.html`(FAQ) · `support-qna.html`(Q&A) |

상단 내비게이션의 카테고리는 첫 번째 탭 페이지로 연결되며, 카테고리 내부 탭은 세그먼트 컨트롤로 개별 페이지를 오갑니다.

## 기술 / 구조

- **순수 정적 HTML** — 빌드 도구·프레임워크 없음. 페이지별 인라인 스타일 + 페이지 상단 `<style>`.
- 폰트: [Pretendard](https://github.com/orioncactus/pretendard) (CDN)
- 동적 요소(프로그램 시간표·리스트, 기업/크리에이터 그리드 등)는 페이지 하단 바닐라 JS로 렌더링.
- 모든 경로가 **상대경로**라 GitHub Pages 하위 경로에서도 정상 동작.

```
.
├── index.html              # 메인
├── about / program / companies* / register* / creators* / support* .html
├── assets/
│   ├── images/             # 로고, 키비주얼, 아이콘, 장식 등
│   └── fonts/
├── docs/                   # DESIGN_SYSTEM.md, 기획 자료
├── legacy/                 # 이전 버전 참고용
└── CLAUDE.md               # 작업 규칙(디자인 시스템 요약)
```

## 로컬 실행

설치 없이 정적 서버로 띄웁니다.

```bash
python -m http.server 8000
# → http://localhost:8000
```

## 디자인 시스템

포스터 기반의 스펙트럼 컬러, 파스텔 그라데이션 배경, 하프톤 도트, 글리치 워드마크, Pretendard를 사용합니다.
세부 규칙은 [`docs/DESIGN_SYSTEM.md`](docs/DESIGN_SYSTEM.md) 및 [`CLAUDE.md`](CLAUDE.md) 참고.

핵심 원칙
- 카드 구분은 **1px 보더** 우선, 그림자는 실제로 떠 있는 요소(고정 헤더·CTA·모달)에만 최소한으로.
- 연한 색 음영은 **연회색**으로 통일, 좌측 컬러 액센트 바·과한 그라데이션 지양.
- 호버 효과는 실제 동작이 있는 요소(링크·버튼·탭)에만.

## 배포

`main` 브랜치 루트에서 GitHub Pages로 서빙됩니다. 수정 후 푸시하면 자동 재빌드됩니다.

```bash
git add -A && git commit -m "..." && git push
```
