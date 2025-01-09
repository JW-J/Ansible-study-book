# Hostname Setting: 호스트명 설정하기

## 사전 분석
- 앤서블로 접근하기 위한 대상 서버들은 이미 제어 노드의 인벤토리에 등록되어 있다.
- 호스트명 설정을 하기 위해 ansible.builtin.hostsname 모듈을 사용한다.
- /etc/hosts 에 tnode 정보들을 등록하기 위해 필요한 정보들을 변수로 정의한다.
- 호스트명을 hosts 파일에 추가할 때는 ansible.builtin.lineinfile 모듈을 사용한다.


