# DB application installation (DB 애플리케이션 설치하기)

### 2025.01.10 (Fail)
AWS에서는 `variables.yml` 에서 `ansible_os_family`를 RedHat-{버전}으로 가져오는데,
AWS는 RedHat으로 가져온다. 그래서도 문제긴한데, 이름을 변경해줘도 mysql 버전을 못가져온다...
나중에 원인좀찾아보자....

## 사전 분석
- 테스트 환경에서 가장 많이 설치하는 데이터베이스인 MYSQL을 AWS CentOS에 설치한다.
- 앤서블 갤럭시에서 우분투에서 설치할 수 있는 MySQL 롤을 검색하여 해당 롤을 이용한다.
- 검색된 롤은 레드햇과 데비안 계열 운영채제에서 MySQL을 설치할 수 있다.

## 플레이북 설계
- ansible.cfg
- inventory
````yaml
[db]
tnode-centos.exp.com
install_mysql.yml
````

- roles
````yaml
 자신이 사용하고 있는 컬렉션 명(geerlingguy.mysql)
````

## 갤럭시북 추가 설명
galaxy.ansible.com 에 들어가게 되면, Search를 통해 찾으면 나오지 않는다.
역할에 들어가서 찾아야 한다.


