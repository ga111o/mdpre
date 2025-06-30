# GitHub Markdown Presenter

GitHub Pages 기반의 마크다운 프레젠테이션 웹 서비스입니다. Marp의 장점은 유지하면서 단점을 보완한 웹 기반 프레젠테이션 도구입니다.

## 🎯 주요 기능

- **GitHub API 연동**: 리포지토리의 마크다운 파일을 자동으로 탐지하고 슬라이드로 변환
- **실시간 프레젠테이션**: 부드러운 슬라이드 전환과 키보드 단축키 지원
- **반응형 디자인**: 모바일, 태블릿, 데스크톱 모든 환경에서 최적화
- **다중 테마**: 기본, 다크, 학술용 테마 지원
- **커스터마이징**: 폰트 크기 조정 및 테마 변경
- **전체화면 모드**: F11 키 또는 버튼으로 전체화면 프레젠테이션

## 🚀 시작하기

### 로컬 개발 환경

1. 리포지토리 클론
```bash
git clone https://github.com/username/github-markdown-presenter.git
cd github-markdown-presenter
```

2. 로컬 서버 실행
```bash
# Python을 사용한 방법
python -m http.server 8080

# 또는 Node.js가 설치된 경우
npm run dev
```

3. 브라우저에서 `http://localhost:8080` 접속

### GitHub Pages 배포

1. GitHub에 리포지토리 생성 및 코드 푸시
2. Repository Settings > Pages에서 Source를 "Deploy from a branch" 선택
3. Branch를 "main" 선택 후 Save
4. 배포된 URL로 접속

## 📖 사용 방법

### 마크다운 슬라이드 작성

슬라이드는 `---`로 구분합니다:

```markdown
# 첫 번째 슬라이드
이것은 첫 번째 슬라이드입니다.

---

# 두 번째 슬라이드
- 리스트 아이템 1
- 리스트 아이템 2

---

## 코드 블록 예제
```javascript
function hello() {
    console.log("Hello, World!");
}
```

### 프레젠테이션 로드

1. GitHub 리포지토리 URL 입력
2. 폴더 접두사 지정 (선택사항)
   - 예: `slides`, `presentation`, `docs`
3. "프레젠테이션 로드" 버튼 클릭

### 키보드 단축키

- `←` `→` `↑` `↓` `Space`: 슬라이드 이동
- `Home`: 첫 번째 슬라이드로
- `End`: 마지막 슬라이드로
- `F11`: 전체화면 토글
- `ESC`: 전체화면 종료

## 🎨 테마

### 기본 테마
- 깔끔한 흰색 배경
- 블루 액센트 컬러
- 읽기 쉬운 타이포그래피

### 다크 테마
- 어두운 배경으로 눈의 피로 감소
- 높은 대비로 가독성 향상

### 학술용 테마
- 논문 발표에 적합한 디자인
- 보수적인 색상 조합
- 정돈된 레이아웃

## 🛠 기술 스택

- **프론트엔드**: Vanilla JavaScript + Tailwind CSS
- **마크다운 파서**: Marked.js
- **코드 하이라이팅**: Prism.js
- **API**: GitHub REST API
- **배포**: GitHub Pages

## 📁 프로젝트 구조

```
github-markdown-presenter/
├── index.html              # 메인 HTML 파일
├── assets/
│   ├── css/
│   │   └── style.css       # 커스텀 CSS 스타일
│   └── js/
│       └── app.js          # 메인 JavaScript 애플리케이션
├── themes/                 # 테마 파일들 (향후 확장용)
├── components/             # 재사용 가능한 컴포넌트 (향후 확장용)
├── package.json           # 프로젝트 설정
└── README.md              # 프로젝트 문서
```

## 🔧 커스터마이징

### CSS 변수를 통한 테마 커스터마이징

```css
.theme-custom {
    --bg-primary: #your-color;
    --bg-secondary: #your-color;
    --text-primary: #your-color;
    --text-secondary: #your-color;
    --border-color: #your-color;
    --accent-color: #your-color;
}
```

### JavaScript를 통한 기능 확장

`GitHubMarkdownPresenter` 클래스를 확장하여 새로운 기능을 추가할 수 있습니다.

## 🤝 기여하기

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 라이선스

이 프로젝트는 MIT 라이선스 하에 배포됩니다. 자세한 내용은 [LICENSE](LICENSE) 파일을 참조하세요.

## 🐛 이슈 및 피드백

버그 리포트나 기능 요청은 [Issues](https://github.com/username/github-markdown-presenter/issues) 페이지를 이용해 주세요.

## 🙏 감사의 말

- [Marked.js](https://marked.js.org/) - 마크다운 파싱
- [Prism.js](https://prismjs.com/) - 코드 문법 강조
- [Tailwind CSS](https://tailwindcss.com/) - 유틸리티 CSS 프레임워크
- [GitHub API](https://docs.github.com/en/rest) - 리포지토리 데이터 접근