# 정병우 웹 퍼블리셔 포트폴리오

GitHub Pages에 바로 업로드할 수 있는 정적 HTML 포트폴리오입니다.

## 파일 구조

```text
nhn-kcp-portfolio-dynamic/
├─ index.html
├─ css/
│  └─ style.css
├─ js/
│  ├─ projects.js
│  └─ main.js
└─ assets/
   └─ portfolio.pdf
```

## 프로젝트 추가/수정 방법

프로젝트 내용은 `js/projects.js`에서만 수정합니다.

1. `window.PORTFOLIO_PROJECTS` 배열 안의 객체를 복사합니다.
2. `id`, `title`, `period`, `role`, `tech`, `summary`, `overview`, `roleItems`, `contributions`, `result`를 수정합니다.
3. `id`는 반드시 중복되지 않게 작성합니다.
4. 이미지가 있으면 `assets/` 폴더에 넣고 `images` 배열에 경로를 추가합니다.

예시:

```js
images: [
  { src: "./assets/project_name-pc.jpg", alt: "프로젝트 PC 화면" },
  { src: "./assets/project_name-mobile.jpg", alt: "프로젝트 모바일 화면" }
]
```

이미지가 없으면 `images: []`로 두면 자동 목업 UI가 표시됩니다.

## GitHub Pages 업로드

1. GitHub 저장소를 생성합니다.
2. 이 폴더 안의 파일을 저장소 루트에 업로드합니다.
3. Settings → Pages → Branch를 `main` / `/root`로 설정합니다.
4. 배포 주소 예시는 `https://아이디.github.io/저장소명/`입니다.

## 수정 필요 사항

`index.html` 하단 Contact 영역에서 아래 값을 실제 정보로 수정하세요.

- `your-email@example.com`
- `https://github.com/your-github-id`


## 이번 버전 변경 내용

- 프로젝트 카드는 `js/projects.js` 데이터 기반으로 자동 생성됩니다.
- 프로젝트 상세의 Screenshots 영역은 원본 HTML 포트폴리오에서 사용한 이미지 파일명을 기준으로 연결했습니다.
- `Publishing Checklist`, `Career Timeline`, `Contact`, `Footer` UI는 `nhn-kcp-portfolio-github-pages.zip` 버전 기준으로 복원했습니다.
- 실제 이미지 파일은 포함되어 있지 않습니다. 제출 전 `img/` 폴더에 원본 이미지 파일을 같은 경로와 파일명으로 복사하세요.
