# 오픈소스 과제_20223171 배대운


### 리눅스 명령어 top
---

*  시슽템의 상태를 전반적으로 가장 빠르게 파악 가능
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


#### top -b -n 1
<img width="300" alt="스크린샷 2018-07-18 20 25 32" src="https://user-images.githubusercontent.com/106725929/171567728-08303b63-998b-469c-81f3-0ef4f2eaff08.png">
* 3:58 3시간 58분 전에 서버가 구동
* load average: 현재 시스템이 얼마나 일을 하는지를 나타냄.
* Tasks: 프로세스 개수 
* Kib Mem,Swap: 각 메모리의 사용량
* PR: 실행 우선순위
* VIRT,RES,SHR : 메모리 사용량
* S: 프로세스 상태

