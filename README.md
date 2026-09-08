Markdown

# 리눅스 기초 명령어 실습 과제

## 1. 현재 위치를 확인하고 폴더를 이동해보기
- 'pwd':현재 작업 중인 폴더 경로 확인
- 결과:'/home/user'
<br />

- 'ls':현재 작업 중인 폴더 목록 확인
- 결과:'suap 공개 다운로드 문서 바탕화면 비디오 사진 서식 음악'
<br />

- 'cd':다른 폴더로 이동
- 실행:'user@user-Samsung-DeskTop-System:~$ cd 다운로드'
- 결과:'user@user-Samsung-DeskTop-System:~/다운로드$'
---
## 2. 나만의 폴더 구조 만들기
- 'mkdir':새로운 디렉터리 생성
- 결과:'mkdir -p linux_practice/{data, backup, scripts, test}'
---
## 3. 파일을 만들고 내용을 작성해보기
- 'user@user-Samsung-DeskTop-System:~/linux_practice/data$ touch profile.txt'
- 'user@user-Samsung-DeskTop-System:~/linux_practice/data$ nano profile.txt'
- name: 김서준
- grade: 2학년
- interest: ai
- ctrl+O, ctrl+X:저장, 나가기
- 'cat ~/linux_practice/data/profile.txt':결과확인
---
## 4. 파일을 복사하고 이동하고 이름 바꾸기
- 'cp profile.txt linux_practice/backup/':복사
- 'mv profile.txt linux_practice/scripts/':이동
- 'mv profile.txt student.txt':이름 변경
---
## 5. 파일을 찾고 내용 검색하기
- 'find linux_practice -name "*.txt"':.txt 파일 찾기
- 'find linux_practice -name "student"':이름에 student가 들어간 파일 찾기
- 'grep "김서준" student.txt':파일 안에 특정 내용 찾기
---
## 6. 필요 없는 파일과 폴더 삭제하기
- 'touch delete_me.txt':파일 생성
- 'rm delete_me.txt':파일 삭제
- 'rmdir test':폴더 삭제
---
## 7. 프로그램 설치하고 실행하기
- 'sudo':관리자 권한으로 실행
- 'apt':소프트웨어를 설치, 업데이트, 삭제하는 패키지 관리 도구
---
## 8. 내 컴퓨터 상태와 실행 중인 프로그램 확인하기
- 'whoami':사용자 계정 정보
- 'free -h':RAM 용량 확인
- 'df -h':디스크 용량 확인
- 'lscpu':CPU 상세 정보 확인
- 'ps aux':실행 중인 프로그램 확인
---
## 9. 파일 권한을 확인하고 변경해보기
- 'ls -l hello.sh':해당 파일의 권한 확인
- 'chmod +x hello.sh':해당 파일의 실행 권한 부여
- 'chmod -x hello.sh':해당 파일의 실행 권한 제거
- r(4):읽기, w(2):쓰기,x(1):실행, chmod:파일의 권한 변경
---
## 10. Linux 환경 조사하기
- 1 Linux와 Ubuntu는 무슨 차이인가?
- 리눅스는 핵심 운영 체제이고, 우분투는 리눅스 배포본인 운영체제이다.

  
- 2 Linux의 /, /home, /etc, /usr, /var 디렉터리는 각각 어떤 용도인가?
- '/':모든 파일과 디렉터리가 시작되는 최상위 디렉터리
- '/home':리눅스 시스템을 사용하는 일반 사용자들의 개인 공간
- '/etc':시스템 운영 및 설치된 프로그램의 환경 설정 파일이 모여있는 곳
- '/usr':기본 실행 파일과 라이브러리 파일, 헤더 파일등의 파일이 저장되어있는 디렉터리
- '/var':시스템 운영 중에 발생한 가변 데이터와 로그가 저장되는 디렉터리

  
- 3 사용자(User)와 그룹(Group)은 무엇인가?
- 'User':리눅스 시스템을 사용하는 개별 주체, 'Group':여러 명의 사용자들을 모아놓은 집합

  
- 4 root 사용자는 일반 사용자와 무엇이 다른가?
- 'root 사용자':리눅스 시스템에서 모든 권한을 가진 관리자 계정, '일반 사용자':제한된 권한을 가진 계정

  
- 5 환경변수(Environment Variable)는 무엇이며 PATH는 어떤 역할을 하는가?
- '환경변수':운영체제가 실행되는 과정에서 프로세스가 참고하는 동적인 값들의 모임
- 'PATH':운영체제가 실행 파일을 찾아볼 디렉터리 목록을 미리 지정해 둔 가장 중요한 환경 변수 중 하나

  
- 6 파일 시스템(File System)이란 무엇인가?
- 컴퓨터의 저장 장치에 있는 데이터를 어떻게 기록하고, 관리하고, 찾아낼지 정하는 규칙

  
- 7 디스크의 파티션(Partition)이란 무엇인가?
- 하나의 물리적인 저장 장치를 소프트웨어적으로 논리적인 여러 개의 구역으로 쪼개는 것

  
- 8 Mount란 무엇인가?
- 컴퓨터에 연결된 저장 장치를 운영체제가 인식할 수 있도록 특정 폴더와 연결해 주는 과정

  
- 9 LVM이란 무엇이고 일반 파티션 방식과 어떤 차이가 있는가?
- 물리적인 하드디스크나 파티션을 유연하게 관리할 수 있도록 도와주는 논리 볼륨 관리 시스템이다.
- 일반 파티션 방식과 가장 큰 차이점은 저장 공간의 유연성이다.
- 일반 파티션은 제한적이고 단순하다면 LVM은 자유롭게 변경이 가능하며 복잡하다.
