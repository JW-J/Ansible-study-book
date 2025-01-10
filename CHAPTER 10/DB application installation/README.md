# DB application installation (DB 애플리케이션 설치하기)

### 2025.01.10
AWS에서 리포지토리를 찾지 못해서 설치를 못함.


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


