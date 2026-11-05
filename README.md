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
- 'site/content/_index.md': 이름과 소개 문장
- 'site/content/about.md': 관심 분야·학습 목표·역량
- 'site/content/project.md': 프로젝트 활동 설명 및 회고
- 'site/pages.json': 좌상단 메뉴 이름과 순서, 사이트 제목
- 'site/static/images/': 페이지에 넣는 이미지 파일

## 출처
- 테마: [PaperMod](https://github.com/adityatelange/hugo-PaperMod) (MIT License). 원본 라이선스 파일은 그대로 유지했습니다.
- 정적 사이트 생성기: [Hugo](https://gohugo.io/)

### 작업 과정

| 부분 | 작성 방식 |
| --- | --- |
| 홈, 개인 소개, 프로젝트, 회고의 글 | 직접 작성했고, 문장 정리에 AI의 도움을 받았습니다. |
| 프로젝트 페이지의 코드 | 팀 프로젝트에서 내가 맡은 아이템 파트의 일부이며, 개발 중 AI의 조언을 활용했습니다. |
| 메뉴·제목 설정, README | 직접 입력하고 수정했으며, README 작성에 대해 구글링, 문장 정리에 AI의 도움을 받았습니다.|

## 수정 후 재배포하기

1. 위의 "사이트 구조와 수정 위치"를 보고 파일을 고친 뒤 저장합니다.
2. 변경을 커밋하고 `main` 브랜치에 올립니다.

   ```bash
   git add 고친파일
   git commit -m "변경 내용 설명"
   git push
   ```

3. 저장소의 **Actions** 탭에서 가장 위 실행이 초록 체크(성공)가 될 때까지 기다립니다. 보통 1~2분 걸립니다.
4. 사이트 주소(https://hechi15.github.io/First-portfolio/)를 열고 Ctrl+F5로 새로고침해서 바뀐 내용을 확인합니다.