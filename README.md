# First Class | YouTube Clone

이스트소프트 오르미 프론트엔드 15기 1조 **First Class**의 YouTube 클론 코딩 프로젝트입니다.  
HTML/CSS만으로 데스크탑·태블릿·모바일 반응형 레이아웃을 구현했습니다.

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/docs/Web/CSS)
[![Figma](https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white)](https://www.figma.com/)

**[Live Demo](https://jungdahye.github.io/YouTube_First_Class/)** · **[Figma](https://www.figma.com/design/hF0mWmuYpECZ1bclHkTuPb/%EC%83%98%ED%94%8C%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8-Youtube-%ED%81%B4%EB%A1%A0%EC%BD%94%EB%94%A9?node-id=0-1)**

---

## 프로젝트 개요

| 항목 | 내용 |
| --- | --- |
| 기간 | 2026.07.07 ~ 2026.07.15 |
| 인원 | 3인 (정다혜, 김내현, 김지훈) |
| 기술 | HTML5, CSS3 (JavaScript 없이 구현) |
| 특징 | 100% 반응형, CSS `:has()` / checkbox hack으로 인터랙션 처리 |

---

## 담당 파트 — 김지훈

공통 레이아웃과 홈 페이지를 담당했습니다. 헤더·사이드바는 `index.html`, `channel.html`, `video.html`에서 함께 사용합니다.

| 구분 | 파일 | 내용 |
| --- | --- | --- |
| 홈 | `index.html`, `css/main.css` | 메인 피드, 카테고리 칩, 영상 카드 그리드 |
| 공통 헤더 | `css/header.css` | 로고, 검색, 알림/프로필 드롭다운, 모바일 검색 |
| 공통 사이드바 | `css/header.css` | 햄버거 토글, 해상도별 사이드바 전환 |

### 공통 헤더

- 검색창 포커스 시 검색 히스토리 노출 (`:focus-within`)
- 알림·프로필 드롭다운을 **checkbox + label**로 열고 닫음 (JS 없음)
- 768px 이하에서 검색창을 숨기고, 검색 아이콘 클릭 시 전체 검색 UI로 전환
- 480px 이하에서 업로드·앱 아이콘을 숨겨 헤더가 가로로 넘치지 않도록 처리
- flex `min-width: 0`으로 중간 너비에서도 검색창이 아이콘을 밀어내지 않게 조정

### 공통 사이드바

- **Desktop:** 240px 고정, 햄버거 클릭 시 70px 아이콘 모드
- **Tablet (≤1024px):** 기본 70px, 햄버거 클릭 시 240px 오버레이 + 딤드
- **Mobile (≤768px):** 기본 숨김, 햄버거 클릭 시 왼쪽에서 슬라이드
- Video 페이지는 모든 해상도에서 모바일과 같은 드로어 방식 (`:has(#CheckBox:checked)`)

### Home (`index.html`)

- 카테고리 칩 가로 스크롤, 영상 카드 `grid` + `minmax(min(100%, 300px), 1fr)`
- 썸네일 16:9, 재생 시간 뱃지, 채널 아바타·제목·조회수 카드
- 제목 2줄 말줄임 (`-webkit-line-clamp`), 좁은 화면에서 카드 hover scale 제거

---

## 페이지 구성

| 페이지 | 설명 | 담당 |
| --- | --- | --- |
| [Home](./index.html) | 메인 피드, 카테고리, 영상 썸네일 리스트 | 김지훈 |
| [Channel](./channel.html) | 채널 배너, 구독, HOME/VIDEOS 탭, 업로드 목록 | 김내현 |
| [Video](./video.html) | 영상 재생, 추천 영상, 댓글, 공유 모달 | 정다혜 |

---

## 주요 기능

- **사이드바 토글:** 해상도별로 접기 / 아이콘 모드 / 모바일 드로어
- **검색:** 데스크탑 인라인 검색, 모바일 전체 검색, 최근 검색어
- **드롭다운:** 헤더 알림·프로필, Video 페이지 댓글 정렬
- **탭:** Channel HOME / VIDEOS, Video 관련 영상 All / From channel
- **모달:** 구독 버튼, 공유하기 (`:target`)

---

## 반응형 Breakpoints

| 구간 | 너비 | 레이아웃 |
| --- | --- | --- |
| Desktop | 1025px 이상 | 사이드바 240px + 메인 |
| Tablet | 1024px 이하 | 사이드바 70px 아이콘 모드 |
| Mobile | 768px 이하 | 사이드바 숨김, 햄버거 드로어, 모바일 검색 |

---

## 폴더 구조

```text
├── index.html          # 홈 (담당: 김지훈)
├── channel.html        # 채널 (담당: 김내현)
├── video.html          # 영상 상세 (담당: 정다혜)
├── css
│   ├── reset.css       # 리셋
│   ├── common.css      # 폰트, 컬러 변수, 모달
│   ├── header.css      # 공통 헤더 / 사이드바 (담당: 김지훈)
│   ├── main.css        # 홈 (담당: 김지훈)
│   ├── channel.css     # 채널
│   └── video.css       # 영상 상세
└── images              # 페이지별 이미지
```

로컬에서 확인하려면 `index.html`을 브라우저로 열면 됩니다.

---

## 팀 소개

| 포지션 | 이름 | 담당 |
| :---: | :---: | --- |
| 팀장 | 정다혜 | Video 페이지, Git, 일정·회의록 |
| 팀원 | 김내현 | Channel 페이지, 회의록 |
| 팀원 | **김지훈** | **공통 헤더, 공통 사이드바, Home 페이지** |

### 협업

- 브랜치: `개인 브랜치` → `develop` → `main`
- 공통 영역(헤더/사이드바) 수정 시 사전 공유
- CSS 클래스 `kebab-case`, 이미지 `alt` 필수, 인터랙션은 `input` + `label`

---

## 링크

- [GitHub Pages](https://jungdahye.github.io/YouTube_First_Class/)
- [Figma 디자인](https://www.figma.com/design/hF0mWmuYpECZ1bclHkTuPb/%EC%83%98%ED%94%8C%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8-Youtube-%ED%81%B4%EB%A1%A0%EC%BD%94%EB%94%A9?node-id=0-1)
