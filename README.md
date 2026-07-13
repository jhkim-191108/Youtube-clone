# ✈️ First Class | YouTube Clone Coding

> **이스트소프트 오르미 프론트엔드 과정 1조 'First Class'의 유튜브 클론 코딩 프로젝트입니다.**

<br />

## 📌 프로젝트 개요

- **작업 기간:** 2026.07.07 ~ 2026.07.15
- **주요 특징:** 모바일과 태블릿, 데스크탑을 모두 지원하는 **100% 반응형 웹 (Responsive Web Design)**

<br />

## 🛠️ 기술 스택 & 툴

<p>
  <img src="https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white">
  <img src="https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white">
  <img src="https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white">
  <img src="https://img.shields.io/badge/figma-%23F24E1E.svg?style=for-the-badge&logo=figma&logoColor=white">
</p>

<br />

## 💻 주요 페이지

- **🏠 Home 페이지:** 유튜브 메인 피드 및 영상 썸네일 리스트
- **👤 Channel 페이지:** 유튜버 채널 대표 영상 및 업로드 영상 목록
- **📺 Video 페이지:** 영상 재생 화면 및 추천 영상, 댓글 영역

<br />

## ✨ 주요 기능

- **🗂️ 탭 (Tab):** Channel 페이지의 메뉴 탭, Video 페이지의 관련 동영상 리스트 탭
- **🪟 모달 (Modal):** SUBSCRIBES 버튼 클릭 시 모달 창
- **🔽 드롭다운 (Dropdown):** Video 페이지의 댓 정렬 기준 선택 창

<br />

## 📱 반응형 Breakpoints

- **🖥️ Desktop:** 기본 스타일 적용
- **📟 Tablet:** `1024px` 이하
- **📱 Mobile:** `768px` 이하

<br />

## ⚙️ 팀 규칙

### 1. 코드 규칙

- **HTML:** 구역별 상단 **설명 주석** 필수
- **접근성:** `<input>` + `<label>` 세트 구성 | `<img>` 태그 **`alt` 속성** 필수
- **CSS:** 클래스명은 **`kebab-case`** | ID명은 **`camelCase`** | 모든 단위는 **`rem`** 사용
- **이미지:** `images/` 내 **페이지별 폴더** 분리 관리 | 아이콘은 `icon-`, 버튼은 `btn-` 접두어 사용

### 2. Git

- **브랜치 흐름:** `개인 브랜치` ➡️ `develop` (충돌 해결) ➡️ 최종 `main` 머지
- **⚠️ develop 머지 순서:** 충돌 방지를 위해 순서를 엄격히 준수. <br />
  &emsp;&emsp;🏃‍♂️ **김내현** ➡️ **김지훈** ➡️ **정다혜** 순으로 진행
- **데일리 싱크:** 매일 작업 시작 전, `develop` 최신 코드를 내 브랜치에 가져와서(`merge`) 진행
- **소통 & 커밋:** 공통 영역 수정 시 **사전 논의 필수** | 커밋 메시지는 **의미 있는 내용**으로 명확히 작성

<br />

## 🌿 브랜치

- `main_header` : 상단 공통 헤더, 사이드바 및 Home 페이지 작업
- `video` : 비디오 상세 페이지 레이아웃 및 스타일링
- `channel` : 채널 상세 페이지 레이아웃 및 스타일링

<br />

## 📁 폴더 구조

```text
├── 📄 index.html         # 홈 페이지
├── 📄 video.html         # 비디오 상세 페이지
├── 📄 channel.html       # 채널 상세 페이지
├── 📂 css
│   ├── 📄 reset.css      # 공통 스타일 reset
│   ├── 📄 common.css     # 공통 스타일 ( font, root, modal )
│   ├── 📄 header.css     # 공통 헤더 스타일
│   ├── 📄 main.css       # 홈 스타일
│   ├── 📄 video.css      # 비디오 스타일
│   └── 📄 channel.css    # 채널 스타일
└── 📂 images             # 이미지 리소스
```

<br />

## 👨‍👩‍👦 팀 소개

|   포지션    |    이름    | 담당 역할 (예시)                                                        |
| :---------: | :--------: | :---------------------------------------------------------------------- |
| **👑 팀장** | **정다혜** | `video` 프로젝트 진척 상황 관리, Git, 회의록 정리, Video 페이지 작업    |
| **🧑‍💻 팀원** | **김내현** | `channel` 회의록 정리, Channel 페이지 작업                              |
| **🧑‍💻 팀원** | **김지훈** | `main_header` 회의록 정리, Home 페이지 작업, Header 작업, SideMenu 작업 |

<br />

## 🔗 관련 링크

- [🎨 Figma 디자인 원본 보러가기](https://www.figma.com/design/hF0mWmuYpECZ1bclHkTuPb/%EC%83%98%ED%94%8C%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8-Youtube-%ED%81%B4%EB%A1%A0%EC%BD%94%EB%94%A9?node-id=0-1&p=f&t=RX8p9smhe2txzra9-0)
- [🚀 GitHub Pages 배포 링크](추후 추가 예정)

---

_This project is created by First Class._
