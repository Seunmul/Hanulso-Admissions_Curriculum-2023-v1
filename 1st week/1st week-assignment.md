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

## 1주차 교육과정

- Created : 23/08/26
- Last Modified : 23/08/26
- 최종 수정자 : 박건하


### 01. 교육과정 목표

C 프로그래밍을 위한 개발환경 구축 - linux, vscode, gcc

1. (Windows) WSL 기반의 Linux 개발환경을 구축한다.
2. 컴파일러 동작을 이해하고, GCC 컴파일러를 통해 실행파일이 빌드되는 과정을 말할 수 있다.
3. Makefile을 통해 여러 c 파일을 한번에 빌드 할 수 있다.
4. 작성한 코드 버전을 git을 통해 관리하고 github에 업로드 한다.

### 02. Keywords
> **교육과정 공통사항** :   
> 아래 안내된 방법 순서대로 진행하되, 어떤 방법을 사용하셔도 무방합니다.
> 안내된 레퍼런스 외에 자료는 Keywords에 있는 단어들을 검색 후 자료를 찾아보시기 바랍니다.

    C 포인터, 컴파일러, GCC, Makefile, Git, Github

### 03. 세부내용 안내

0. vscode 설치하기
1. Reference를 참고하여 WSL 기반의 Linux 개발환경 구축하기.(Windows 기준)
2. Ubuntu에서 gcc installation

```bash
$ sudo apt update
$ sudo apt upgrade -y
$ sudo apt install gcc make -y
```

3. 간단한 C 프로그램 구현 후 gcc 로 컴파일 (hello world 등)
4. 실행파일 확인 후 어셈블리 파일 및 목적파일 생성 확인 (reference 참조)
5. Makefile로 빌드 스크립트 작성 후 빌드 프로그램 실행 확인
6. Git 시스템 구축 후 Github에 업로드

### 04. 제출 결과물 안내

- .c 파일
- .o 파일
- 실행파일
- 컴파일러 작동방식에 대한 보고서 (.md형식 혹은 워드형식으로 업로드)
- Makefile Script
- **위 모든 파일을 본인 Github 레포지토리에 업로드 후 확인 연락 바람**
- **통과기준 : 제출 시 통과**

## Reference

- wsl 설치 : https://learn.microsoft.com/ko-kr/windows/wsl/install
- vscode 설치(환경변수 연동) :https://seong6496.tistory.com/314
- vscode 설치 : https://code.visualstudio.com/download
- wsl & vscode 연동하기 : https://learn.microsoft.com/ko-kr/windows/wsl/tutorials/wsl-vscode
- gcc : https://80000coding.oopy.io/d5fa7c87-192f-4c68-95eb-aa4af5b9dbf5
- c 언어 레퍼런스 : https://youtube.com/@nullnull_not_eq_null
