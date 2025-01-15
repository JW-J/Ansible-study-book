# CPU, 메모리, 디스크 사용률 모니터링

## 사전 분석
- dstart, sysstat 패키지를 설치한다. 운영체제가 레드햇 계열이면 `ansible.builtin.dnf`모듈을 이용하여 설치하고, 데미안 계열이면 ansible.builtin.apt,yum 모듈을 이용하여 설치한다.
- 각각의 명령어 실행은 `ansible.builtin.shell`을 이용하여 실행하고, loop 키워드를 이용하여 모니터링 명령어 별로 여러 옵션을 추가하여 명령을 실행한다.
- 실행된 명령어 결과는 로그 디렉터리에 저장한다.

