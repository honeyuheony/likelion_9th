# Web 기초 

## Web & Web Service

- 서버 : serve + er ->  서비스에 대해 응답하는 입장

- client -> server (request)

- server->client (response)

- 클라이언트와 서버간의 html을 이용한 통신

- 나는 네이버를 켜고 웹툰을 본다음 재미있다고 댓글을 달았다

- 네이버를 켬(get), 웹툰을 봄 (get), 댓글작성(post)

- p2p (peer to peer) : 모두가 서버이자 모두가 클라이언트

- www : world wide web ~~ internet

- chrome, ie, edge -> web brower

## How to make Web Server?

- Server PC : 컴퓨팅자원, 무한루프, 냉각, 클라이언트 수 고려, 보안에 집중된 PC
- 서버설계방법
  - 로컬환경세팅
    - 설치 다소 까다로움
    - 추가 지식 요구
    - 한번 익히면 자유롭게 이용가능
  - 웹 호스팅 업체 이용
    - 설치 조작 단순
    - 과금발생
    - 개발 제약있음
    - 클라이언트 수 고려 안해도 됨

- 멋사에서는 <a> github를 이용할 예정

## HTML

- Hyper Text Markup Language
  - Hyper Text -> Link
  - Markup Language != Programing Language

- 내용물

  - 글, innertext

  - 태그 ( in 마카)

    - ```html
      <h1></h1>, <h2></h2> ~ title
      ```

    - ```html
      <a> link
      ```

    - ```html
      <img> img
      ```

    - ```html
      <ol, ul> list
      <li> </li> list inner
      ```

    - ```html
      <p>  단락
      <br> 줄바꿈
        
      ```

    - ```html
      <strong> 강조
      ```

  - 속성 ( in 마카) : 태그 내부 구성요소

  #### 대원칙 : HTML로 꾸미려 하지 말자. 꾸미는 언어는 CSS임

- 구성

  - html로 작성된 문서임을 알려주는 태그
    
    - ```html
      <!DOCTYPE html>, <html> 
      ```
  - 직접 화면에 등장하지 않지만 이 문서를 설명하는 태그  (title, incoding type, ~)
    
  - ```html
      <meta charset="UTF-8">
          <meta http-equiv="X-UA-Compatible" content="IE=edge">
          <meta name="viewport" content="width=device-width, initial-scale=1.0">
          <title>Document</title>
      ```
    
  - 화면에 들어나는 태그
    
    - in <body>, ex : <h1>, <a>, <img> ~~
    
    - ```html
      <H2>todolist</H2>
          <ol>
              <li><a href="1.html">충분한 수면</a></li>
              <li>멋사과제</li>
              <li>교회</li>
              <li>운체</li>
      ```

- Form : 입력된 내용을 전달하기 위한 태그

  - ex : <form action =  target> </form>

## Bootstrap

- css/javascript 기반 프레임워크

- 공짜, 반응형 웹 지원, 브라우저 호환성
- 단점 : 티가남, 성능이 다소 떨어짐
- 부트스트랩 cdn 링크를 헤드에 넣으면 부트스크랩 사용가능

### 실습코드 (in bootstarp)

```HTML
<!DOCTYPE html>
<html lang="en">
<head>
    
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <script src="https://code.jquery.com/jquery-3.6.0.js" integrity="sha256-H+K7U5CnXl1h5ywQfKtSj8PCmoN9aaq30gDh27Xc0jk=" crossorigin="anonymous"></script>
    <!-- 합쳐지고 최소화된 최신 CSS -->
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.2/css/bootstrap.min.css">

    <!-- 부가적인 테마 -->
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.2/css/bootstrap-theme.min.css">

    <!-- 합쳐지고 최소화된 최신 자바스크립트 -->
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.2/js/bootstrap.min.js"></script>
    <title>Document</title>
</head>
<body>
    <div class = 'container'>
        <ul class="nav nav-tabs">
            <li role="presentation" class="active"><a href="1.html">충분한 수면</a></li>
            <li role="presentation"><a href="2.html">멋사과제</a></li>
            <li role="presentation"><a href="3.html">교회</a></li>
            <li role="presentation"><a href="4.html">운체</a></li>
          </ul>
    <h1>1</h1>
    <h2>2 </h2>
    <form action = "target">
        아이디 : <input type = 'text', name = 'id'>
        패스워드 : <input type = 'password', name = 'pw'>
        <div class="form-group">
          <label for="exampleInputEmail1">이메일 주소</label>
          <input type="email" class="form-control" id="exampleInputEmail1" placeholder="이메일을 입력하세요">
        </div>
        <div class="form-group">
          <label for="exampleInputPassword1">암호</label>
          <input type="password" class="form-control" id="exampleInputPassword1" placeholder="암호">
        </div>
        <div class="form-group">
          <label for="exampleInputFile">파일 업로드</label>
          <input type="file" id="exampleInputFile">
          <p class="help-block">여기에 블록레벨 도움말 예제</p>
        </div>
        <div class="checkbox">
          <label>
            <input type="checkbox"> 입력을 기억합니다
          </label>
        </div>
        <button type="submit" class="btn btn-info">제출</button>
    </form>

    </form>
    <br>
    <form action="target">
        <h2>my note</h2>
        제목 : <input type='text', name='title'> <br>
        <select>
            <option value="goodday">좋은날</option>
            <option value="day">그저그런날</option>
            <option value="badday">나쁜날</option>
        </select><br>
        내용 : <br><textarea cols='30', rows='20'></textarea>
        <br><input type = 'submit'>
    </form>

    <H2>todolist</H2>
    <ol>
        <li><a href="1.html">충분한 수면</a></li>
        <li>멋사과제</li>
        <li>교회</li>
        <li>운체</li>
    </ol>
    <!-- ol>li*3  단축키-->
    <div class="progress">
        <div class="progress-bar progress-bar-success" role="progressbar" aria-valuenow="40" aria-valuemin="0" aria-valuemax="100" style="width: 40%">
          <span class="sr-only">40% Complete (success)</span>
        </div>
      </div>
      <div class="progress">
        <div class="progress-bar progress-bar-info" role="progressbar" aria-valuenow="20" aria-valuemin="0" aria-valuemax="100" style="width: 20%">
          <span class="sr-only">20% Complete</span>
        </div>
      </div>
      <div class="progress">
        <div class="progress-bar progress-bar-warning" role="progressbar" aria-valuenow="60" aria-valuemin="0" aria-valuemax="100" style="width: 60%">
          <span class="sr-only">60% Complete (warning)</span>
        </div>
      </div>
      <div class="progress">
        <div class="progress-bar progress-bar-danger" role="progressbar" aria-valuenow="80" aria-valuemin="0" aria-valuemax="100" style="width: 80%">
          <span class="sr-only">80% Complete (danger)</span>
        </div>
      </div>
    </div>
    
</body>
</html>
```

## Github 배포

### Github

- 코드 저장 기능 (commit)
- 저장시점마다 기록하고, 되돌아가기 가능 (이전상태로 되돌림)
- 협업 기능
- web Hosting (FREE!)

#### 실습 html 파일 호스팅

https://honeyuheony.github.io/