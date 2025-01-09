# Network IP setting (No test): 네트워크 IP 설정하기
AWS에서 테스트를 진행하다보니 환경 문제로 인해 테스트는 불가

## 사전 분석
- nmcli 명령어는 community.general.nmcli 모듈을 제공한다.
- netplan은 파일이므로 사전에 netplan 파일 구조를 확인하고 jinja2 템플릿으로 작성한다.
- 운영체제가 레드햇이면서 앤서블 오토메이션 플랫폼을 사용할 경우에는 redhat.rhel_system_roles.network 라는 룰을 사용할 수 있다.
- 예제에서는 ethernet 타입의 네트워크 IP를 설정한다.
- IP 설정 관련 정보는 메인 플레이북에서 변수로 정의한다.
- 변수로 정의한 네트워크 인터페이스가 실제 호스트에 존재하는지 앤서블 팩트를 통해 확인한다.
- 운영체제가 CentOS이거나 레드햇일 경우에는 nmcli 모듈을 사용하여 IP를 설정한다. (OS 구분)
- 운영체제가 우분투일때 netplan 파일을 이용하여 IP를 설정한다. (OS 구분)
- AWS에서 할 땐 운영체제를 Amazon으로 인식한다.

