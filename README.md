# 오픈소스 과제_20223171 배대운
---

###  top

*  시스템의 상태를 전반적으로 가장 빠르게 파악 가능
*  옵션 없이 입력하면 interval 간격으로 화면을 갱신하며 정보를 보여줌
*  top 실행 전 옵션
   1) 순간의 정보를 확인하려면 -b 옵션 추가(batch모드)
   2) -n : top 실행 주기 설정(반복 횟수)
* top 실행 후 명령어
   1) shift + p : CPU 사용률 내림차순
   2) shit + m : 메모리 사용률 내림차순
   3) shift + t : 프로세스가 돌아가고 있는 시간 순
   4) k : kill. k 입력 후 PID 번호 작성. signal은 9
   5) f : sort field 선택 화면 -> q 누르면 RES순으로 정렬
   6) a : 메모리 사용량에 따라 정렬
   7) b : Batch 모드로 작동
   8) 1 : CPU Core별로 사용량 보여줌


__top -b -n 1__ 

<img width="300" alt="스크린샷 2018-07-18 20 25 32" src="https://user-images.githubusercontent.com/106725929/171567728-08303b63-998b-469c-81f3-0ef4f2eaff08.png">

*  Kib Mem,Swap: 각 메모리의 사용량
*  PR: 실행 우선순위
*  VIRT,RES,SHR : 메모리 사용량
*  S: 프로세스 상태

### ps

* ps: 현재 실행중인 프로세스의 목록을 보는 명령어이다.


__옵션__



1) -e: 실행중인 모든 프로세스의 정보를 출력
2) -f: 프로세스에 대한 자세한 정보를 출력
3) -u 사용자이름: 특정 사용자에 대한 모든 프로세스의 정보를 출력
4) -p pid: pid로 지정한 프로세스의 정보를 출력
5) u: 프로세스의 소유자의 이름, CPU 사용량, 메모리 사용량 등 상세 정보 출력
6) a:터미널에서 실행한 프로세스의 정보를 출력
7) x: 실행중인 모든 프로세스의 정보를 출력

### jobs

* jobs : 작업의 상태를 표시하는 명령어이다.

|옵션|설명|
|---|---|
|-l|프로세스 그룹ID를 state필드앞에 출력|
|-n|프로세스 그룹 중에 대표 프로세스 ID 출력|
|-p|각 프로세스 ID에 대해 한 행씩 출력|
|command|지정한 명령어를 실행|


* jobs로 알 수 있는 세션의 상태 값

|상태|설명|
|---|:---:|
|Running| 작업이 일시 중단되지 않았고 종료하지 않고 계속 진행 중임|
|Done|작업이 완료되어 0을 반환하고 종료 함|
|Done(code)|작업이 정상적으로 완료되었으며, 0이 아닌 코드를 반환 함|
|Stopped|작업이 일시 중단|
|Stopped(SIGTSTP)|SIGTSTP 신호가 작업을 일시 중단|
|Stopped(SIGTTOU)|SIGTTOU 신호가 작업을 일시 중단|


###  kill
---

* kill : 프로세스에 특정한 신호를 보내는 명령어 일반적으로 프로세스를 종료 시킬 때 사용

__주요 시그널__

|signal|영어|설명|
|---|---|:---:|
|sighup|Hang up|세션이 종료될 때 시스템이 내리는 시그널|
|sigkill|kill|강제종료 시그널|
|sigterm|teminate|기본 값, 종료 요청 시그널|
|sigtstp|temporary stop|Crtl + z 일시 중지 요청 시그널|


### vim 매크로

1) 일반모드에서 q를 누른 후 매크로 사용할 알파벳을 눌러준다.
   * ex) q를 누른 후 a를 누르면 a매크로가 저장된다.
2) 밑에 --recording--이 뜨면 자신이 매크로에 저장할 내용을 작업한다.
3) 타이핑이 끝나면 esc를 눌러 일반모드로 돌아가 q를 해준다.
4) 일반 모드에서 @a라고 누르면 매크로 a가 재생된다.
   

