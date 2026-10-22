# Jinkyeong Choi · Research homepage

GitHub Pages용 개인 연구 홈페이지입니다. HTML/CSS와 정적 파일만 사용합니다.
블랙·라일락·화이트 색상, Georgia 이름 글꼴, Arial 본문을 사용합니다.

- GitHub 사용자명: `zingyon`
- 저장소명: `zingyon.github.io`
- 배포 완료 후 주소: https://zingyon.github.io/
- 현재 목록: KARMA, SimDiffRec, KIISE 논문. 심사 중 원고는 제외했습니다.

이 파일 묶음은 배포용 준비물입니다. 저장소 생성이나 GitHub 배포가 이미 실행된 것은 아닙니다.

## 1. 저장소 만들기

1. https://github.com/ 에 `zingyon` 계정으로 로그인합니다.
2. https://github.com/new 를 엽니다.
3. Owner를 `zingyon`으로 선택합니다.
4. Repository name에 `zingyon.github.io`를 입력합니다.
5. Description은 `Jinkyeong Choi's research homepage`로 입력합니다.
6. Visibility는 **Public**을 선택합니다.
7. **Add README**를 켭니다. Git ignore와 License는 선택하지 않아도 됩니다.
8. **Create repository**를 누릅니다.

GitHub 사용자명이 다르면 저장소명도 `실제사용자명.github.io`로 바꿔야 합니다.
`zingyon.github.io` 저장소가 이미 있다면 새로 만들지 말고 기존 저장소에서 진행하세요.
기존 홈페이지 파일이 있다면 교체 전에 로컬로 보관하세요.

## 2. 파일 업로드

1. 받은 ZIP을 압축 해제합니다.
2. 압축을 푼 `zingyon.github.io` 폴더를 엽니다.
3. 저장소의 **Code → Add file → Upload files**로 갑니다.
4. 아래 파일과 `assets` 폴더를 한꺼번에 드래그합니다.
   - `index.html`
   - `style.css`
   - `assets` 폴더 전체
   - `README.md`
   - `robots.txt`
   - `sitemap.xml`
5. Commit message에 `Add research homepage`를 적습니다.
6. 직접 `main`에 커밋하는 옵션을 선택하고 **Commit changes**를 누릅니다.

**ZIP 자체를 올리거나, 바깥 `zingyon.github.io` 폴더 전체를 한 겹 더 올리면 안 됩니다.**
저장소의 첫 화면에서 `index.html`과 `style.css`가 바로 보여야 합니다.
`assets` 안에는 `portrait.jpg`, `favicon.svg`, `Jinkyeong_Choi_CV.pdf`가 있어야 합니다.

직접 커밋 대신 **Propose changes**가 표시되는 경우에는 제안된 변경으로 Pull request를 만들고
저장소에서 **Merge pull request**를 완료한 후 다음 단계로 진행하세요.

## 3. GitHub Pages 켜기

저장소 상단 **Settings → 왼쪽 Pages → Build and deployment**로 이동합니다.

| 항목 | 설정 |
|---|---|
| Source | Deploy from a branch |
| Branch | main |
| Folder | / (root) |

**Save**를 누릅니다. 별도의 테마 선택, 패키지 설치, 빌드 명령은 필요하지 않습니다.
`main`이 보이지 않으면 2단계 업로드와 커밋이 완료되었는지 확인하세요.
Custom domain은 처음에는 비워 두세요.

## 4. 배포 확인

1. 저장소의 **Actions**에서 Pages 관련 실행이 성공했는지 확인합니다.
2. **Settings → Pages**에서 게시된 주소 또는 **Visit site**를 확인합니다.
3. 배포 후 https://zingyon.github.io/ 에 접속합니다.
4. 첫 배포나 변경 반영에는 최대 10분 정도 걸릴 수 있습니다.
5. 사진, CV, 논문 링크와 스마트폰 화면을 확인합니다.
6. GitHub 프로필의 Website 필드에도 홈페이지 주소를 추가하면 됩니다.

페이지는 로그인하지 않은 방문자에게도 열립니다. 포스터 QR에는 배포가 완료된 주소를 사용하세요.

## 5. 이후 수정

| 수정 내용 | 파일 |
|---|---|
| 이름·소속·연락처 | index.html |
| 연구 분야 | index.html의 RESEARCH INTERESTS 영역 |
| 논문 | index.html의 PAPERS 영역 |
| 학력·경력·수상 | index.html |
| 색상·글씨 크기·간격 | style.css |
| 프로필 사진 | assets/portrait.jpg |
| CV | assets/Jinkyeong_Choi_CV.pdf |

텍스트를 바꾸려면 GitHub에서 파일을 열고 연필 모양 **Edit** 버튼을 누릅니다.
수정 후 **Commit changes**로 저장하면 같은 주소에 자동으로 반영됩니다.
사진이나 CV는 같은 경로와 파일명으로 다시 업로드하면 링크를 고칠 필요가 없습니다.
제공한 CV는 원래 첨부한 PDF입니다. 홈페이지에서 심사 중 원고를 제거한 작업이 PDF 내용까지
수정한 것은 아니므로, 새 CV가 있으면 이 파일을 교체하세요.

로컬에서 미리 보려면 이 폴더에서 다음 명령을 실행합니다. Python 3가 설치되어 있어야 합니다.

```bash
python3 -m http.server 8000
```

브라우저에서 http://localhost:8000 을 엽니다. 종료는 터미널에서 Ctrl+C입니다.

## 6. 자주 생기는 문제

| 증상 | 확인할 것 |
|---|---|
| 404 | Pages의 main / (root), 배포 성공 여부, 루트 index.html 위치 |
| README만 보임 | index.html이 하위 폴더에 들어가 있지 않은지 확인 |
| 사진·스타일이 안 나옴 | assets 폴더, style.css 업로드 여부와 대소문자 확인 |
| 변경이 안 보임 | Actions 완료 후 새로고침, Mac에서는 Cmd+Shift+R |
| 기존 Pages 저장소가 있음 | 해당 저장소에 파일을 올리고 기존 주소를 유지 |

사용자명을 바꾸면 index.html의 canonical·og:url, robots.txt, sitemap.xml 안의
`https://zingyon.github.io/`도 새 주소로 바꿔 주세요.

## 선택: 터미널로 업로드

웹 업로드가 편하면 이 단계는 건너뛰세요. Git이 설치되고 GitHub 인증이 되어 있어야 합니다.
1단계에서 README와 함께 만든 저장소를 복제한 뒤, 압축을 푼 파일을 복제 폴더 안에 복사합니다.

```bash
git clone https://github.com/zingyon/zingyon.github.io.git
cd zingyon.github.io
# 여기에 ZIP에서 푼 파일과 assets 폴더를 복사합니다.
git add index.html style.css assets README.md robots.txt sitemap.xml
git commit -m "Add research homepage"
git push origin main
```

그 다음 3단계에서 Pages를 설정합니다. 기존 저장소를 복제하는 방식이므로 README 초기 커밋과
충돌하는 문제를 피할 수 있습니다.

## 공식 문서

- https://docs.github.com/en/pages/quickstart
- https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
- https://docs.github.com/en/repositories/working-with-files/managing-files/adding-a-file-to-a-repository
