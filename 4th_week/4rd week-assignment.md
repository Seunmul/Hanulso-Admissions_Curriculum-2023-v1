<h3 align="center">
    <img src="../img/HANULSO_LOGO1.png"
    width="250" height="250"/>
    <br>
    <br>
    <h1 align="center"> 하늘소</h1>
</h3>

<h5 align="center">
    KNU IT대학 SW 전공동아리
    <br>
    Since 1988
</h5>

## 4주차 교육과정

- Created : 23/08/26
- Last Modified : 23/08/26
- 최종 수정자 : 박건하

### 01. 교육과정 목표

Linux Bash Shell Script 작성 및 Socket 프로그래밍

1. SSH 기반 원격환경 접속에 대한 이해.
2. 터미널 실행 시 시스템의 환경변수의 로드에 대한 이해.
3. 리눅스 명령이 및 shell script에 대한 이해
4. 쉘 스크립트를 통해 3주차에서 작성한 실행파일 실행 및 argument에 대한 이해.
5. 데이터 버퍼링에 대한 이해 (with Queue)

### 02. Keywords

> **교육과정 공통사항** :  
> 아래 안내된 방법 순서대로 진행하되, 어떤 방법을 사용하셔도 무방합니다.
> 안내된 레퍼런스 외에 자료는 Keywords에 있는 단어들을 검색 후 자료를 찾아보시기 바랍니다.

    SSH, Shell Script, System Call, Process, Thread, TCP/IP, 소켓 프로그래밍

### 03. 세부내용 안내

> 3주차 교육과정에서 작성한 서버 및 클라이언트를 Docker 가상환경 내 네트워크에서 실행합니다. 실행 시 아래 조건을 만족시켜야합니다.  
> [조건 1] client 및 server는 쉘 스크립트를 통해 실행되어야 합니다.  
> [조건 2] client 실행 시 네트워크 정보는 argument를 통해 제공해야 합니다.  
> [조건 3] client 실행 시 전달 문자열은 client를 통해 제공해야 합니다.  
> [조건 4] server는 client에서 수신받은 문자열을 Queue 를 활용한 버퍼링을 기반으로 터미널에 한 글자씩 출력해야 합니다.
> 예시는 아래와 같습니다

```bash
# 서버 실행
./server "[서버_ip]:[서버_port]"
# 클라이언트 실행
./client "[서버 ip]:[서버 port]" "hello world "

...
# 서버 측 데이터 수신 결과 출력
...
>> data revceived, show received data :
h
e
l
l
o

w
o
r
l
d
>> data printing.
```

> 출력형태나 구현 방식에 대해선 가이드라인에서 제시하는 방법 외에 다른 방법을 사용하셔도 됩니다. 단, 위의 조건을 만족해야합니다.

1. 제공된 네트워크 구성도 분석
2. 네트워크 구성도를 기반으로 server container에 SSH 접속
3. 작성한 server 코드 실행
4. 네트워크 구성도를 기반으로 client container에 SSH 접속
5. 작성한 client 코드 실행
6. 결과 확인

### 04. 제출 결과물 안내

**동아리방에서 직접 시연을 통한 통과여부 판단**

- socket server, client 실행파일, 실행을 위한 shell script를 준비해주시면 됩니다.
- 동아리 방에 도착하시면 ssh 연결 방법을 안내해드립니다.
- 연결할 container의 네트워크 구성도는 당일 안내드립니다.
- 1회 당 제한시간은 **3시간**입니다.
- **통과기준 : 구현 혹은 일정 기준 만족 시 합격**

## Reference

- 자료에 대한 reference는 키워드 검색을 통해 확인할 것
- socket server 및 client에 대한 기본 레퍼런스는 개인별 제공
