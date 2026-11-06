# 임승현 개인 포트폴리오 사이트

게임 개발을 공부하는 임승현의 개인 소개 웹사이트입니다. Hugo와 PaperMod 테마로 만들고, GitHub Actions로 배포합니다.

- 사이트 주소: https://hechi15.github.io/First-portfolio/
- 저장소: https://github.com/hechi15/First-portfolio

## 사이트 구성

| 페이지 | 내용 |
| --- | --- |
| 홈 | 이름, 짧은 소개, 학과, 관심 분야 |
| 개인 소개 | 관심 분야와 이유, 학습 목표, 역량, 앞으로의 계획 |
| 프로젝트 | 프로젝트 개발 목적, 역할, 코드, 과정, 결과, 회고 |

## 사이트 구조와 수정 위치
- `site/content/_index.md`: 이름과 소개 문장
- `site/content/about.md`: 관심 분야·학습 목표·역량
- `site/content/project.md`: 프로젝트 활동 설명 및 회고
- `site/pages.json`: 우상단 메뉴 이름과 순서, 사이트 제목
- `site/static/images/`: 페이지에 넣는 이미지 파일
- `.github/workflows/hugo-pages.yml`: GitHub에 올리면 사이트를 자동으로 빌드하고 배포하는 설정 파일
- `site/assets/css/extended/custom.css`: 사이트 모양을 바꾸는 CSS 파일

## 스타일(CSS) 수정

테마 기본 모양 위에 `site/assets/css/extended/custom.css`로 아래 꾸밈을 추가했습니다.

| 꾸밈 | 효과 |
| --- | --- |
| 키보드 포커스 표시 | Tab 키로 이동할 때 현재 위치를 파란 굵은 테두리로 보여 줍니다. |
| 이미지 테두리 | 프로젝트 화면 이미지에 테두리와 그림자를 넣어 배경과 구분합니다. |
| 표 선 색상 | 라이트 모드는 검은 선, 다크 모드는 흰 선으로 표의 칸을 또렷하게 합니다. |

## 출처
- 테마: [PaperMod](https://github.com/adityatelange/hugo-PaperMod) (MIT License). 원본 라이선스 파일은 그대로 유지했습니다.
- 정적 사이트 생성기: [Hugo](https://gohugo.io/)
- 배포 설정: 수업에서 제공한 GitHub Pages 배포 스크립트(`.github/pages_build.py`)와 워크플로를 사용했습니다.

### 작업 과정

| 부분 | 작성 방식 |
| --- | --- |
| 홈, 개인 소개, 프로젝트, 회고의 글 | 직접 작성했고, 문장 정리에 AI의 도움을 받았습니다. |
| 프로젝트 페이지의 코드 | 팀 프로젝트에서 내가 맡은 아이템 파트의 일부이며, 개발 중 AI의 조언을 활용했습니다. |
| 메뉴·제목 설정, README | 직접 입력하고 수정했으며, README 작성에 대해 구글링, 문장 정리에 AI의 도움을 받았습니다.|
| 테마와 배포 설정| 사이트의 테마와 GitHub 배포 설정은 수업에서 제공한 것을 활용하였습니다.|

## 수정 후 재배포하기

1. 위의 "사이트 구조와 수정 위치"를 보고 내용을 수정한 뒤 저장합니다.
2. 변경내용을 커밋하고 `main` 브랜치에 올립니다.

   ```bash
   git add 고친파일
   git commit -m "변경 내용 설명"
   git push
   ```

3. 저장소의 **Actions** 탭에서 가장 위 실행이 초록 체크(성공)가 될 때까지 기다립니다.
4. 사이트 주소(https://hechi15.github.io/First-portfolio/)를 열고 Ctrl+F5로 새로고침해서 바뀐 내용을 확인합니다.

## 내 컴퓨터에서 실행하기

### 준비물

- Git
- Hugo extended 0.167.0 ([설치 파일 받기](https://github.com/gohugoio/hugo/releases/tag/v0.167.0))

설치 후 아래 명령으로 버전을 확인합니다. 결과에 `v0.167.0`과 `extended`가 보이면 됩니다.

```bash
hugo version
```
### 실행 순서

1. 저장소를 받고 `site` 폴더로 이동합니다.

   ```bash
   git clone https://github.com/hechi15/First-portfolio.git
   cd First-portfolio/site
   ```
   - 혹은 저장소 내 site 폴더로 직접 이동하여 git bash를 사용하는 방법도 가능합니다.

2. 로컬 서버를 실행합니다.

   ```bash
   hugo server --config pages.json --theme template --themesDir themes
   ```
    - VS Code를 사용한다면 VS Code 터미널에서 `cd site`로 이동한 뒤 같은 명령을 입력해도 됩니다.

3. 브라우저에서 http://localhost:1313/First-portfolio/ 를 엽니다.

### 빌드만 확인하기

- 변경 내용을 `main`에 push한 뒤 저장소의 **Actions** 탭에서 "Deploy Hugo to GitHub Pages" 실행이 초록 체크(성공)인지 확인해도 됩니다.