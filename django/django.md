## MTV패턴

장고는 Model, Template, View 세 개로 분할하여 작업할 수 있는 환경을 제공한다.

Front : 

- Template : 사용자가 보이는 영역. HTML, CSS, 템플릿언어, (javascript)

Back : Model, View

- Model : DataBase(DB)
- View : 데이터를 처리하는 곳, MTV중에서 핵심.

ex : 당근마켓 :

- 검색창에 검색어 입력 -> Template
- 엔터를 누름 -> View로 데이터 전송
- Model에서 검색어에 대한 데이터를 찾은 후 다시 View로 전송.
- View에서 가져온 정보를 분류해 Template로 전송
- Template에서 사용자에게 출력

## app

app : 하나의 프로젝트를 서비스별로 쪼갠 단위

```python
python manage.py startapp "app이름"
```

후 settings.py 의 INSTALLED_APPS 에 '앱이름.apps.앱이름(첫글자대문자)Config' 추가

## 웹사이트 구동순서 :

- 사용자가 서버에 요청
- 서버의 view는 model에게 요청에 필요한 데이터 받음
- view는 받은 데이터를 적절하게 처리해서 template로 너김
- template는 받은 정보를 사용자에게 보여줌

-> 앱을 제작할 때에는 반대의 순서로 제작

- app을 생성 (python manage.py startapp "app이름")
- template 폴더 생성 후 html페이지 제작
- views.py에 함수 추가
- urls.py 에 views import, path추가 (경로, views.함수명, name="welcome") (name은 html에서 호출시 대신 사용할 수 있는 이름)

## 장고와 데이터베이스

데이터베이스를 사용하면 웹을 열때마다 데이터가 보존되어있게 만들 수 있다.

### orm

orm을 통해 파이썬으로 데이터베이스에 직접 제어할 수 있다.
(sql, 객체지향 개념 알기)
데이터베이스는 row, column으로 구성된 하나의 표이다.
python에서는 데이터베이스를 class를 통해 조작한다.
하나의 클래스 (row)에 각각의 데이터 (column) 

### model

models.py에서는 model 클래스를 상속받은 데이터베이스 클래스를 생성해 각 필드를 생성한다.

![image-20210614185524455](C:\Users\kuhy\AppData\Roaming\Typora\typora-user-images\image-20210614185524455.png)

![image-20210614185559478](C:\Users\kuhy\AppData\Roaming\Typora\typora-user-images\image-20210614185559478.png)

model에서 사용하는 필드 타입과 옵션
model 클래스에 id 필드가 이미 정의되어있으므로 id는 따로 만들 필요 x

makemigrations : 앱 내의 migration 폴더를 생성해서 models.py의 변경사항 저장
migrate : Migration 폴더를 실행해 데이터베이스에 적용

admin 페이지를 통해 데이터베이스를 확인할 수 있다.

1. superuser 생성 -> python manage.py createsuperuser
2. admin.py에  models.class import
3. admin.site.register(class) 추가
4. (참고) models class 내에 _str___ 를 추가하면 데이터셋이 저장될 때의 호출을 변경할 수 있다.



models.py 에 데이터테이블(클래스, 함수) 생성 -> templates(페이지) 생성 -> views.py 함수 지정 -> urls.py path 지정

## CRUD

### CRUD - read

데이터베이스를 읽는 것. html에서 python 문법을 사용해서 데이터를 읽을 수 있다. (wordcount)

Path-converter : 
세부페이지를 각 데이터베이스마다 하나의 페이지를 만드는 것이 아닌 데이터베이스 id에 따라 다른 페이지를 보일 수 있게 하는 것.
Primary key : 
기본 키.ID 값을 말한다.

### CRUD - create

GET  : 
데이터를 얻기 위한 요청
데이터가 url에 보임

POST :
데이터를 생성하기 위한 요청
데이터 url 안보임
Csrf 공격 방지

create 기능은 페이지를 생성할 new.html, 생성한 페이지를 저장할 create 함수로 이루어짐. 

### CRUD - update

update 기능은 페이지를 수정할 edit.html, 수정한 페이지를 저장할 update 함수로 이루어짐. 

### CRUD - delete

delete 기능은 페이지 id를 받아와 삭제하는 delete 함수 생성으로 이루어짐.

## Template 상속

html 파일에서 중복되는 코드들은 base.html에 저장하고 상속을 통해 사용할 수 있다.

1. 공통으로 사용할 html 부분을 base.html에 저장한 후 내용이 들어갈 부분에
   {% block content %}

   {% endblock %} 를 작성한다.

2. {% extends 'base.html' %}
   {% block content %}
   inner html
   {% endblock %}
   로 작성한다.

### urls.py management

urls.py를 각 app별로 관리할 수 있다.

메인 urls.py에는 django.urls.include를 import 한 후 
path('appname/' include ('appname.urls')) -> 주석에 설명적혀있음. 만 추가한다.
app에 사용되는 path는 모두 잘라낸 후 앱 내에 urls.py를 생성하여 옮긴다. 



