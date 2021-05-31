# Django setting

## 설치해야할 요소:

- chrome
- python 
  - (mac os에는 기본적으로 설치되어있음. python -v)
  - python 버전 3.7 이상으로 설치
  - 윈도우에서는 anaconda, ms store 등을 이용
- git
  - 버전관리를 위한 도구
  - 본 강의에서는 homebrew를 통해 다운로드
- vscode

## 터미널사용법 :

GUI : Graphic user interface

- 처음 지정된 기능밖에 사용불가
- 조작속도가 CLI에 비해 늦는 경우가 있음.

Terminal : CLI를 gui환경에서 실행할 수 있게 해주는 도구

- windows에서는 git bash, ms store terminal 사용 

- (cmd랑 터미널이랑 다른점은?)

  - 터미널 : **서버의** **로컬 또는 원격으로 접속할 수 있는 콘솔을 구현한 소프트웨어
  - cmd (쉘) : 실제로 명령어를 전달하고 결과를 전달받는 프로그램

  

![image-20210527211204520](C:\Users\kuhy\AppData\Roaming\Typora\typora-user-images\image-20210527211204520.png)

### 디렉토리

- 구조 : 트리형
- 요소 :
  - home(~) :털미널 구동시 처음 위치하는 디렉토리
  - working directory(.) : 현재 위치
  - root directory(/) : 모든 디렉토리의 시작점.
  - .. : 상위디렉토리

- 절대경로와 상대경로 :
  - 절대경로 : pwd 명령어를 통해 확인가능, 시작점부터 현재 위치까지의 경로를 쭉 나열해 표시
  - 상대경로 : 현재 경로를 기준으로 기준점으로부터의 위치를 표시

- 외워야 할 명령어:

  명령어 : 명령어 [옵션] [인자]로 구성된다.

  옵션 : -로 시작해서 영문 대소문자로 구성. 명령어의 기능을 구체화. 명령어에따라 없을 수도 있음

  인자 : 명령어의 수행시 대상이 될 파일이라 디렉토리, 없을수도 있고 필수일 수도 있음

  - pwd : print working directory -> 현재 위치(경로)를 알려줌.
  - man : manual -> 명령어 설명서, man [알고싶은 명령어]
  - ls : list -> 디렉토리의 목록을 보여줌. 옵션 : a (숨김표시), l (상세표시), F(종류표시)
  - cd : change directory -> 현재 위치를 이동해줌, cd [이동할 위치]
  - claer : 터미널 버퍼 초기화

  명령어나 디렉토리를 중간정도 입력 후 tap을 누르면 자동완성가능

## Django

- 프레임워크 : 반복적으로 사용되는 개념을 묶어 개발자의 편의성을 도움.

- 프레임워크 == 라이브러리?

  - 프레임워크는 라이브러리에 비해 구조화가 되어있음.
  - 프레임워크를 통해 개발속도를 증가시킬 수 있음.

- 가상환경 :

  - 여러 개의 프로젝트를 진행할 때 버전이 달라야 할 필요가 있음.

  - 그럴 때에 각각의 환경을 매번 설정하는 것은 비효율적이고 오류발생가능

  - 각각의 독립적인 가상환경을 설정하여 개발환경을 구축할 수 있음.

    ```python
    python -m venv "가상환경이름"
    ```

    - mac에서는 python 3 지정필요.
    - mac에서는 "bin", windows에서는 "Scripts" 폴더 에서 엑티베이터를 실행시킴

    ```python
    source "가상환경이름/bin|Scripts/activate"
    ```

- 장고 설치 및 환경구성 :

  - ```python
    pip install django // 장고설치
    pip install --upgrade pip // pip 업데이트
    django-admin startproject "프로젝트이름" // 프로젝트 시작
    cd "프로젝트이름" // 프로젝트로 경로이동
    python manage.py runserver // 서버 실행
    ```

    