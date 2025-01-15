# 팩트를 이용한 시스템 모니터링 (monitoring_facts)

## 사전분석
- 팩트를 이용하여 다음과 같은 정보를 추출한다.
  - 호스트 이름
  - 커널 버전
  - 네트워크 인터페이스 이름
  - 네트워크 인터페이스 IP주소
  - 운영체제 버전
  - CPU개수
  - 사용 가능한 메모리
  - 스토리지 장치의 크기 및 여유공간
- 추출한 내용은 클라이언트 서버에 ansible.builtin.shell 모듈을 이용해서 `/var/log/daily_check`디렉터리에 저장한다.

## ⭐ Ansible에서 모든 조건문과 제어문은 task의 실제 모듈 실행 전에 먼저 평가됩니다.

- when (조건부 실행)
- loop (또는 with_items, with_dict 등의 반복문)
- ignore_errors (오류 무시 여부)
- register (결과 저장)
- changed_when (변경 조건 정의)
- failed_when (실패 조건 정의)
- until (반복 종료 조건)

## ⭐ YAML문법과 SHELL스크립트의 줄바꿈
- 보통 작업을 진행하다보면 `|`, `\`를 많이 본다. 쉘에서는 `\`는 줄바꿈을 의미하고 `|` 는 ymal에서 줄바꿈을 의미한다고 한다.