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

