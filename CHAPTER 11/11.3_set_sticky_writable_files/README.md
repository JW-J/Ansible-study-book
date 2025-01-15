# 11.3 디렉터리 및 파일 접근 권한 변경하기

## 주의사항
Sticky bit가 적용된 파일 목록중에 보안을 위해 이를 적용하면 안되는 파일 목록이 있다.
Sticky bit가 적용된 파일의 권한을 수정할 땐 적용하면 안되는 파일인지 반드시 확인해야 한다. 
이 확인은 KISA(한국인터넷진흥원)에서 보안 관련 문서를 참조하는것이 좋다.

## 사전분석
- Sticky bit 파일 검색 명령어: find / -xdev -perm -04000 -o -perm -02000 -o -perm -01000
- World Writable 파일 검색 명령어: find / -xdev -type f -perm -2
- ansible.builtim.shell 모듈을 이용하여 Sticky bit 파일과 World Writable 파일을 찾는다.
- 찾은 파일 목록은 ansible.builtin.file 모듈을 이용하여 파일의 접속 권한을 설정한다.
- Stickey bit 파일은 u-s, g-s, o-s로 설정하고, World Writable 파일은 o-w로 설정한다.

## 비고
보통 정보보안관리체계에서도 나오는 World Writable 파일은 모두 지우라는 권고사항이 있다.
이를 활용하면 좋을 것 같다.


