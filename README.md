# NIKKE ALL SITE

모바일 게임 **승리의 여신: 니케**를 더 편하게 즐기기 위한 유용한 사이트·도구를 한 페이지에 모아 둔 정적 웹 허브입니다.

## 바로가기

| 서비스 | URL |
|--------|-----|
| **Vercel (메인)** | https://nikkeallsite.vercel.app |
| **GitHub Pages** | https://saintpark90.github.io/NikkeAllSite/ |
| **저장소** | https://github.com/saintpark90/NikkeAllSite |

## 주요 기능

- **사이트 카드 모음** — 계산기, 시뮬레이션, DB, 위키, 공식 커뮤니티 등 30개 이상의 외부 사이트를 카드 형태로 정리
- **썸네일 미리보기** — 각 사이트 썸네일 클릭 시 해당 페이지로 이동
- **카테고리 필터** — 공식, 계산기, 시뮬레이션, 성장, DB, 위키, 정보, 랭킹, 시트, 종합, 유틸
- **검색** — 사이트 이름·설명·URL 키워드로 실시간 필터링
- **격자 / 목록 보기** — 카드형 또는 한 줄 목록형 레이아웃 전환
- **즐겨찾기(★)** — 자주 쓰는 사이트를 상단에 고정 (`localStorage` 저장)
- **라이트 / 다크 모드** — 테마 전환 및 설정 유지

## 포함 카테고리 예시

| 카테고리 | 내용 |
|----------|------|
| 공식 | 공식 홈페이지, BlablaLink, 네이버 게임 라운지 |
| 계산기 | 덱 빌더, PVP 프레임 계산, 전투력 패널티, 버프 계산기 |
| 시뮬레이션 | 오버로드 최적화·모듈작, 가챠 시뮬, 딜량 계산 |
| 성장 | 코더 수급, 소장품(애장품) 강화 최적화 |
| DB / 위키 | 라이브2D·일러스트 DB, 팬덤 위키 |
| 정보 | 상담 족보, 스킬 검색, 유실물 정리 |
| 랭킹 | 솔로·유니온 레이드 랭커 벤치마크 |
| 시트 | 유레 결산, 상담 족보 구글 시트 |
| 종합 | Prydwen, Loot & Waifus, nikke.gg 등 |
| 유틸 | 폰트·이미지 생성기, 리세마라용 임시 이메일 |

## 프로젝트 구조

```
NikkeAllSite/
├── index.html              # 메인 페이지 (사이트 목록)
├── power-penalty.html      # 전투력 패널티 계산기 (내장 도구)
├── penalty-data.js         # 패널티 계산 데이터
├── assets/
│   └── logo.png            # 헤더 로고
└── .github/workflows/
    └── pages.yml           # GitHub Pages 자동 배포
```

## 로컬에서 실행

별도 빌드 없이 정적 파일만 있으면 됩니다.

```bash
# 저장소 클론
git clone https://github.com/saintpark90/NikkeAllSite.git
cd NikkeAllSite

# 브라우저에서 index.html 열기
# 또는 간단한 로컬 서버 (선택)
npx serve .
```

## 배포

- **Vercel** — `main` 브랜치 push 시 자동 배포 (`nikkeallsite.vercel.app`)
- **GitHub Pages** — `.github/workflows/pages.yml` 워크플로우로 `main` push 시 배포

## 기여 / 수정

사이트 목록은 `index.html` 내 `SITES` 배열에서 관리합니다. 새 사이트를 추가할 때는 `cat`, `title`, `desc`, `url` 필드를 맞춰 넣으면 됩니다.

```js
{ cat: "계산기", title: "사이트 이름",
  desc: "사이트 설명",
  url: "https://example.com/" }
```

썸네일 캡처가 실패하는 사이트는 `noThumb: true`를 추가할 수 있습니다.

## 업데이트 로그 (배포 시 갱신)

GitHub에 배포할 때마다 `index.html` 스크립트의 `FOOTER_INFO.changelog` 객체를 함께 수정합니다.

```js
changelog: {
  title: "최종 업데이트 · YYYY.MM.DD",
  body: "· 변경 사항 1\n· 변경 사항 2"
}
```

## 면책

이 프로젝트는 개인·커뮤니티 정리용 페이지이며, **SHIFT UP / Proxima Beta** 및 각 외부 사이트 제작자와 공식적으로 제휴된 것이 아닙니다.  
링크된 사이트의 저작권·콘텐츠는 해당 제작자에게 있으며, 썸네일은 자동 캡처되므로 실제 화면과 다를 수 있습니다.
