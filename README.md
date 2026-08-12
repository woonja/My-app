# My-app



# 정운영 — Process Technology · CS Engineer Portfolio

반도체 공정기술 엔지니어 · CS(Customer Service) 엔지니어를 목표로 하는 개인 포트폴리오 웹사이트입니다.
별도 빌드 과정 없이 `index.html` 파일 하나로 동작하는 싱글 페이지 사이트입니다.

## 미리보기

* **컨셉**: 반도체 웨이퍼 · 클린룸에서 착안한 그래파이트(먹색) + 리소그래피 앰버 컬러 조합
* **구성 섹션**: Hero → About → Core Competency Flow(공정 흐름형 역량 소개) → Skills → Projects → Education \& Certifications → Contact
* **폰트**: [Pretendard](https://github.com/orioncactus/pretendard)(본문), [JetBrains Mono](https://www.jetbrains.com/lp/mono/)(라벨·수치)

## 폴더 구조

```
.
├── index.html   # HTML + CSS + JS 전부 포함된 단일 파일
└── README.md
```

## 실행 방법

별도 설치 없이 `index.html`을 브라우저로 열면 바로 확인할 수 있습니다.

```bash
# 방법 1: 더블클릭으로 index.html 열기

# 방법 2: 로컬 서버로 실행 (권장)
python3 -m http.server 8000
# 브라우저에서 http://localhost:8000 접속
```

## 내 정보로 수정하기

`index.html` 안에서 아래 위치를 찾아 본인 정보로 바꾸면 됩니다.

|항목|위치 (섹션)|비고|
|-|-|-|
|이름 / 네비게이션 로고|`<header class="nav">`|`이도윤`, `DY` 뱃지 텍스트|
|헤드라인 · 소개 문구|`<section class="hero">`|`<h1>`, `.hero-sub`|
|이메일 / 전화번호 / GitHub|hero, contact 섹션|`mailto:`, `tel:`, GitHub 링크 총 3곳에 반복 등장|
|자기소개 본문|`<section id="about">`|`.about-body` 안 `<p>` 두 단락|
|전공/목표 직무/관심 공정/위치|`<section id="about">`|`.fact-grid`|
|역량 5단계 설명|`<section id="flow">`|`.flow-node` 5개 (STEP 01\~05)|
|기술 스택 태그|`<section id="skills">`|`.tag-row` 4개 패널|
|프로젝트 3개|`<section id="projects">`|`.project-card` — 기간/제목/설명/태그|
|학력 · 자격증|`<section id="education">`|`.edu-item`, `.cert-list`|
|LinkedIn 등 추가 링크|`<section id="contact">`|`.contact-links`|

> 색상, 아이콘, 문구 톤을 바꾸고 싶다면 `:root` 안의 CSS 변수(`--bg`, `--accent` 등)만 수정해도 전체 톤이 함께 바뀝니다.

## 배포 방법 (GitHub Pages 예시)

1. 이 폴더를 새 GitHub 저장소에 push
2. 저장소 **Settings → Pages** 에서 배포 브랜치를 `main`(또는 `gh-pages`), 폴더를 `/root`로 설정
3. 몇 분 후 `https://\\\[아이디].github.io/\\\[저장소명]/` 주소로 접속 가능

Netlify나 Vercel에 폴더를 그대로 드래그 앤 드롭해도 배포됩니다.

## 기술 스택

* HTML5 / CSS3 (Grid, Flexbox, CSS Variables)
* Vanilla JavaScript (스크롤 리빌 애니메이션, 네비게이션 스크롤 스파이)
* 외부 의존성: Google Fonts(JetBrains Mono), jsDelivr CDN(Pretendard) — 두 CDN 외 별도 라이브러리 없음

## 라이선스

이 코드는 자유롭게 수정·재사용하셔도 됩니다. 사용된 폰트(Pretendard, JetBrains Mono)는 각자의 오픈소스 라이선스를 따릅니다.



