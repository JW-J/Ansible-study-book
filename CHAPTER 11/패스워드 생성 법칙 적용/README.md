# 패스워드 생성 법칙 적용하기

## 상황
패스워드 주기와 함게 반드시 설정해야 하는 보안 설정은 패스워드 생성 법칙입니다.
이를 위해 `pwquality.conf`라는 pam 설정 파일을 이용해야 하고 리눅스 서버에서 libpam-pwqualiy 패키지 설치가 되어있어야 합니다.

## 사전 분석
- 데미안 계열의 우분투에는 libpam-pwquailty 패키지를 설치한다.
- 패스워드 변경 주기는 /etc/security/pwpquality.conf 파일로 설정한다.
- /etc/security/pwquality.conf 파일을 설정하기 전에 원본 파일은 백업받는다.
- qwquality.conf 파일은 사용자가 커스텀으로 설정하는 파라미터들로 구성되어 있으며, Jinja2 템플릿 방식으로 구현한다.
- 파라미터들은 별도의 변수 설정 파일에서 정의한 파라미터 값으로 사용하고, 파라미터 정의 여부를 체크하여 pwpuality.conf 파일의 내용을 구성한다.


