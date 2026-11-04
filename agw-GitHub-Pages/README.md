# agw HTML 버전

`index.html` 한 파일 안에 화면, 스타일, 158종 메뉴, 추천 및 합의 코드가 모두 들어 있습니다. Node.js, 서버, API 키, 패키지 설치가 필요하지 않습니다. 파일을 브라우저로 직접 열거나 GitHub Pages에 올려 사용할 수 있습니다.

## GitHub Pages에 올리기

1. GitHub에서 새 저장소를 만듭니다.
2. 이 폴더 안의 `index.html`, `.nojekyll`, `README.md`를 저장소 최상위에 업로드하고 커밋합니다. `github-pages` 폴더 자체가 아닌 그 안의 파일을 올립니다.
3. 저장소의 **Settings → Pages**로 이동합니다.
4. **Source → Deploy from a branch**를 선택합니다.
5. **Branch → main**, 폴더는 **/ (root)**를 선택하고 **Save**를 누릅니다.
6. 배포가 완료되면 Pages 화면에 표시되는 주소로 접속합니다.

공식 안내: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

이 패키지에는 서버의 DB, 기존 참여자 정보, API 키를 포함하지 않습니다. 서버 버전의 `data` 폴더를 저장소에 업로드하지 마세요.

## 사용 방법과 저장 범위

방을 만든 뒤 **참여자 추가**로 같은 기기에서 친구들을 추가합니다. 상단의 **지금 의견을 입력할 사람** 선택창으로 사람을 바꾸고 각자의 먹고 싶은 메뉴와 피하고 싶은 메뉴를 제출합니다. 마지막에는 방장으로 전환하여 수집을 마감하고 최종 메뉴를 제안합니다. 각 참여자로 전환해 동의한 뒤 방장이 확정합니다.

정보는 현재 브라우저의 localStorage에 저장됩니다. 서버 버전의 기존 방은 자동 이전되지 않습니다. 다른 기기, 다른 브라우저, 시크릿 창과 실시간으로 공유되지 않습니다. URL만 전달해도 같은 방에 접속하는 방식은 이 버전에서 제공하지 않습니다. 브라우저 데이터를 삭제하면 방도 삭제됩니다. 같은 기기에서 사람을 바꾸는 기능은 로그인이나 사용자 신원 검증 기능이 아닙니다.

이전 서버 버전처럼 여러 기기의 실시간 링크 참여가 필요하면 GitHub Pages 외에 공유 데이터베이스와 인증을 처리할 백엔드를 연결해야 합니다.

HTML 생성 원본은 별도로 `agw-app`에 유지합니다. 수정 후 재생성하려면 그 폴더에서 `node export-static.mjs`를 실행합니다.
