# apaceh repo setting: 패키지 리포지터리 환경 설정하기
## 사전 분석
- 본 프로젝트는 RHEL 호스트 대상으로 한다.
- httpd 서비스 설치와 관련된 모든 태스크는 물론 롤을 이용해 구현한다.
- 롤을 통해 리포지터리 환경 설정이 끝나면, 리포지터리 URL을 체크한다.
- 롤에는 다음과 같은 절차를 갖는 태스크가 존재한다.
- repo 디렉터리를 생성한다.
- httpd 서비스를 설치한다.
- repo.conf라는 환경 설정 파일을 대상 노드로 복사한다.
- httpd 서비스를 재시작하고 sefcontext 설정한다.
- http 서비스를 firewalld에 추가하고, firewalld서비스를 reload한다.