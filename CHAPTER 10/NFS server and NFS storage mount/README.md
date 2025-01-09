# NFS server and FNS storage mount: NFS서버 설치 및 NFS 스토리지 마운트하기

## 사전 분석
- NFS 구성 방법 및 플레이북 모듈은 챗 GPT를 통해 찾은 플레이북을 참조한다.
- 실습 환경에서는 NFS 서버를 CentOS에 구성한다.
- NFS 서버가 구성되면 나머지 두 노드에는 NFS 스토리지를 마운트한다.
- 플레이북 재사용을 위한 NFS 서버 및 클라이언트는 롤로 구성한다.
- AWS는 ansible의 함수인 `ansible_facts['distribution` 은 Amazon으로 받아온다. 디버그모드로 어떤값을 가져오는지 확인해보는걸 권장한다. 그래서 `distribution information.yml`을 실행하면 어떻게 받아 오는지 알 수 있다.