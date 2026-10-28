# AIERA 3D 웹 배포

`https://3d.aiera.co.kr/`에 [hichoni/3d-modeling](https://github.com/hichoni/3d-modeling)의 공개 웹 파일을 배포한다. 앱 원본과 서명된 설치 파일은 원본 저장소에서 관리한다.

기존 `https://hichoni.github.io/3d-modeling/`의 도메인 설정을 변경하지 않아, 이미 설치된 크롬북 IWA와 Android 앱의 origin 제한·업데이트 URL이 계속 작동한다. 새 주소에서도 같은 대문, 체험, STL 스튜디오, 설치 파일을 제공한다.

## 업데이트

- 배포 워크플로는 15분 간격으로 원본 `main`의 변경을 확인한다. GitHub의 예약 실행은 지연될 수 있다.
- **릴리스 직후 즉시 반영하려면** Actions → Deploy AIERA 3D → Run workflow를 실행하고 완료를 확인한다.
- `https://3d.aiera.co.kr/deployment.json`의 `source_sha`로 실제 배포된 원본 커밋을 확인한다.
- 예약 실행은 공개 저장소가 오래 비활성 상태인 경우 중단될 수 있다. 작업을 재개할 때 Actions에서 활성 여부와 최신 SHA를 확인한다.
- 별도의 토큰·서명 키를 이 저장소에 넣지 않는다. 공개 원본을 읽고 이 저장소의 Pages에 배포하는 기본 Actions 권한만 사용한다.

## 도메인

- GitHub Pages: GitHub Actions / 사용자 지정 도메인 `3d.aiera.co.kr`.
- 예스닉 CNAME: `3d` → `hichoni.github.io`.
- 소유 확인 TXT: `_github-pages-challenge-hichoni.3d.aiera.co.kr` (GitHub에서 발급된 값 유지).
- `aiera.co.kr`의 원래 홈페이지와 루트 DNS는 변경하지 않는다.

기존 설치 앱은 원래 GitHub 주소에서 웹 화면을 읽는다. 일반 웹사이트에 접속하는 것만으로 브라우저에 프린터 소켓 권한이 생기는 것은 아니므로, 크롬북은 기존 IWA, Android는 APK, 일반 PC 브라우저는 연결 프로그램을 사용한다.
