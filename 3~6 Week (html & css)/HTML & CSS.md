## HTML & CSS

## INTRO

Programing : 프로그램 코드를 작성하는 일.

프로그래밍 언어 : 컴퓨터에 명령을 내리기 위한 언어.

html과 css는 프로그래밍 언어가 아님.

### html/css, javascript 소개

html : Hyper Text Markup Language - 구조

css : Cascading Style Sheets - 스타일

- Style Sheets : 웹 페에지의 스타일을 정의해둔 시트
- Cascading : 우선순위, 후에 설명

javascript : 웹을 이용하는 유저와 상호작용하기 위한 기능을 추가할 때 쓰는 언어 - 동작



## HTML 기초문법

### 요소와 태그

html 요소는 시작태그, 요소, 종료태그로 이루어짐.

### html 문서구조

```html
<!DOCTYPE html> # 문서 형식을 정의
<html lang="kr"> # html 태그 밖에 다른 태그가 있으면 안됨. 주 언어 정의
	<head> # html 문서에 대한 정보를 담고 있음. html태그 바로 밑에 존재.
		<meta charset="utf-8"> # 문서와 관련된 정보를 담음.
		<title>김우헌을 소개합니다.</title> # 웹 탭에 표시되는 이름 변경.
	</head>
	<body> # 사용자에게 보이는 영역.
		<h1> 안녕하세요, 저는 김우헌입니다.
		<p>저는 현재 웹 프로그래밍을 공부하는 학생입니다.</p>
	</body>
</html>
```

### 레이아웃과 관련된 기본 태그

#### 시맨틱 태그(Semantic tag) : 의미를 가지고 있는 태그

- header : 소개나 제목을 담는 태그

- nav : 네비게이션, 페이지 이동을 담당하는 태그

- section : 기준에 맞게 구간을 나누는 태그

- article : 주 내용을 담는 태그

- aside : 사이트의 주변부(광고) 를 담는 태그

- footer : 회사정보, 사이트정보등의 추가정보를 담는 태그

```html
<!DOCTYPE html> 
<html lang="kr"> 
	<head> 
		<meta charset="utf-8">
		<title>XX일보</title> 
	</head>
	<body> 
		<header>
        	<p>여기는 로고와 이름이 들어갑니다.</p>
        </header>
        <nav>
            <p>여기는 사이트 매뉴입니다.</p>
        </nav>
        <section>
        	<p>여기서부터는 기사가 들어갑니다.</p>
            <article>
            	<p>여기는 첫번째 기사입니다.</p>
            </article>
            <article>
            	<p>여기는 두번째 기사입니다.</p>
            </article>
        </section>
        <aisde>
        	<p>여기에 광고가 들어갑니다.</p>
        </aisde>
        <footer>
        	<p>여기에 회사 정보가 들어갑니다.</p>
        </footer>
	</body>
</html>
```

### 텍스트와 관련된 태그

- 제목 태그 : 제목을 나타내고 싶을때 사용. 중요도에 따라 1~6단계

  - ```html
    <h1>1</h1>
    <h2>2</h2>
    <h3>3</h3>
    <h4>4</h4>
    <h5>5</h5>
    <h6>6</h6>
    ```

- 본문 태그

  - p : 단락, 문단을 구분하는 태그

  - br : break. 줄바꿈을 해주는 태그. 종료태그를 쓰지않음. 종료태그가 없는것을 빈 요소라 부름

    - 빈 요소 : br, img ~~

  - pre : 형식화된.입력한 내용 그대로 표시하는 태그

    ```html
    <p>사람을 답답하게 만드는 방법이 두가지가 있습니다.<br>
    첫번째는 하던 말을 긑까지 안하는 거고, <br>
    두번째는</p>
    <pre>사람을 답답하게 만드는 방법이 두가지가 있습니다.
    첫번째는 하던 말을 긑까지 안하는 거고, 
    두번째는</pre>
    ```

- 글자와 관련된 태그

  - strong : 감싼 문장을 볼드체로바굼
  - em : emphasize, italic체로 바꿈

  ```html
  <strong>strong</strong>
  <em>emphasize</em>
  ```

  - sub : 문장 기준 아래에 기입.
  - sup : 문장 기준 위에 기입.

  ```html
  <p>log<sub>10</sub>4</p>
  <p>e<sup>2</sub></p>
  ```

  - ins : 끼워넣은, 문장 밑줄
  - del : 삭제된, 취소선 생성

  ```html
  <p>하루를 이겨내는 원동력은<ins>맛있는 밥</ins>입니다.</p>
  <p>하루를 이겨내는 원동력은<del>맛있는 밥</del>입니다.</p>
  ```



## 링크태그

Hyper link : 접근을 가능하게 해주는 링크

#### a태그

- a태그는 속성을 가짐.

- 속성은 시작태그 안에 들어가며, 태그이름 뒤 한칸 띄우고 작성.

- 속성 : 

  - 태그에 대해 추가적인 정보제공
  - HTML의 모든 태그는 속성을 가질 수 있다.
  - 속성간의 구분은 띄어쓰기로 한다.

- 형식 : <a 키="값">내용</a>

  ```html
  <a href="https://www.google.com">구글</a>
  <a href="https://www.naver.com">네이버</a>
  <a href="https://www.daum.net">다음</a>
  ```

- href는 연결할 웹 사이트 주소를 담는다.

#### 경로(path)

- URL(Uniform Resource Locator) : 인터넷에서 HTML페이지, CSS문서, 이미지 등 자원의 위치를 나타냄.

- 우리가 흔히 쓰는 URL은 주소(Address)와 경로(Path)로 이루어진다. (address/path)

  - 절대 URL : 접근하는 최초 시작점부터 경유한 경로를 모두 기록하여 위치를 나타냄.
  - 상대 URL : 기준점을 기준으로 상대적인 경로를 기록하여 위치를 나타냄.

  ![image-20210417004004950](C:\Users\kuhy\AppData\Roaming\Typora\typora-user-images\image-20210417004004950.png

![image-20210417004021562](C:\Users\kuhy\AppData\Roaming\Typora\typora-user-images\image-20210417004021562.png)

#### target

- 클릭으로 링크를 열 곳을 정하는 속성
  - _self : 현재 탭에서 링크를 염
  - -blank : 새 탭에서 링크를 염

### 멀티미디어와 관련된 태그

#### 이미지태그

```html
<img src = "imageURL", alt : "text">
```

src : 불러올 이미지의 URL을 속성값으로 가짐. (source의 약자)

alt : 불러올 이미지가 없거나 불러오는데 실패했을 경우 대신 표시되는 문장 alternative text(대체문구)의 약자

height, width : 이미지의 크기(높이, 너비) 를 조절하는 속성. but html을 아닌 css태그를 이용해 조절하는 것이 좋음.

youtube 동영상 사이트에 개시하기 : 동영상 공유 후 퍼가기로 iframe코드를 복사하기

### 테이블과 리스트

#### 테이블의 구성

- 테이블 : table태그 
- 행 : tr태그 (table row)
- 제목 : th태그 (table heading)
- 데이터 : td태그 (table data)

```html
<table>
    <tr>
        <th>성별</th>
        <td>남</th>
        <td>여</th>
    </tr>
    <tr>
        <th>학년</th>
        <td colspan="2">3</th>
    </tr>
    <tr>
        <th>이름</th>
        <td>우헌</th>
        <td>곽두팔</th>
    </tr>
</table>
# rowspan ="숫자" : 숫자만큼 셀이 행을 점유
# colspan ="숫자" : 숫자만큼 셀이 열을 점유
```

#### 목록

- ul : unordered list
- ol : ordered list
- li : ul, ol 내부의 리스트요소

```html
<h3>장보기목록</h3>
<ul>
    <li>우유</li>
    <li>세제</li>
    <li>바지</li>
</ul>
<h3>TO-DO 리스트</h3>
<ol>
    <li>시험공부</li>
    <li>과제하기</li>
    <li>냉장고정리</li>
</ol>
```

특성 :

- 리스트는 기본적인 들여쓰기를 포함한다.
- 리스트는 중첩이 가능하다.

속성 :

- start : 리스트가 시작하는 숫자를 정함 (start = "숫자")
- type : 순서를 시작하는 문자를 정함 (type = "문자")
- reversed : 순서를 반대로 시작. 키만 사용하여 적용
- value : 해당하는 리스트 아이템의 번호를 지정 (value = "숫자")

### Form

#### form tag : 

폼에 포함되는 다양한 입력 양식 태그들을 감싸줌.

- 속성 : 
  - action : 데이터를 보낼 URL을 지정
  - method : 보내는 방식을 지정
    - get : 
      - 브라우저에서 form에 입력한 데이터를 URL에 넣어 보이게 보냄.
      - 데이터 조회를 목적으로 할 때 주로 쓰임. (ex : 검색)
    - post :
      -  데이터를 URL에 적지 않고 내부에 숨겨서 보냄.
      - 서버에 있는 데이터를 쓰거나 수정, 삭제할 때 주로 사용. (ex : 로그인)

#### input tag :

- 사용자에게 입력을 받기 위해 사용되는 태그, 빈 태그
- 텍스트 뿐이 아닌 다양한 것을 입력받을 수 있음
- type 속성을 통해 입력방식을 결정함.
- name 속성을 키로 사용해 입력받은 데이터를 구분함.
- placeholder : 가이드 문구
- value : 초기값 지정

#### label tag:

- 해당하는 라벨을 클릭시 input태그가 활성화 됨.
- 이름표와 같은 역할
- for="id" 속성을 통해 활용.

#### div :

- 태그들을 구분짓고 나누기 위해 활용하는 태그 (division)

#### select :

- 여러 개의 선택지를 제시하고 싶을때 사용.
- select 태그와 option 태그로 이루어져 작동.

#### textarea :

- 한번에 많은 글을 입력받을 때 사용.
- cols, rows 는 각각 가로글자 수, 세로줄 수 를 의미함.

#### button tag

- input 태그의 버튼타입과 동일하게 버튼을 생성할 수 있음.
- button 태그를 사용할 수도 있음.
- 이미지버튼 등 다양하게 이용 가능.

```html
<body>
    <h2>회원가입</h2>
    <form action="my-app", method="get">
        <div>
        	<label for="userid"></label>
       		<input type="text", id="userid", name="id", placeholder='id를 입력하세요.' value='None'>
    	</div>
   	 	<div>
        	<label for="userpassword"></label>
       <input type="password", id="userpassword", name="password", placeholder="비밀번호를 입력하세요.">
    	</div>
        <div>
            <label for="gender">성별</label>
            <select name="gender", id="gender">
                <option value="male">남성</option>
                <option value="female">여성</option>
            </select>
        </div>
        <div>
            <label for="job">직업</label>
            <select name="job", id="job">
                <option value="student">학생</option>
                <option value="teacher">교사</option>
                <option value="etc">기타</option>
            </select>
        </div>
        <div>
            <label for="introduce">자기소개</label>
            <textarea name="introduce", id="introduce", cols="30", rows="10", placeholder="자기소개를 입력하세요."></textarea>
        </div>
        <button type="submit">제출</button>
        <button type="reset">리셋</button>
    </form>
</body>
```





