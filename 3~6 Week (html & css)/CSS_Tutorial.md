# CSS

## CSS 기초 :

### css : Cascading Style Sheets
Style Sheets : 웹에 적용할 스타일을 명시한 명세서

### 구성 :
선택자 : 스타일을 적용하고자 하는 HTMl 요소를 선택하는 역할
속성(Property) : 지정할 스타일의 속성명에 해당. [속성:값;] 이 한 단위로 세미클론을 이용하여 구분한다.
값(Value) : 키워드나 특정 단위를 이용하여 원하는 스타일을 적용. 속성과 쌍을 이룬다.

![image-20210507145154784](C:\Users\kuhy\AppData\Roaming\Typora\typora-user-images\image-20210507145154784.png) 

<strong>css는 반드시 html에 적용을 해야 사용할 수 있다.</strong>

### 적용방법 : 
Link style :
	HTML에 외부에 있는 CSS파일을 불러옴.
Embedding style :
	HTML의 head에 <style>를 이용하여 CSS를 작성
Inline style :
	HTML요소에 직접 style 속성(attributes)를 이용하여 CSS를 

## 선택자 기초

- 여러 개의 선택자를 ','를 이용해 스타일을 한번에 지정할 수 있다.

### 단순선택자

- 타입선택자 : 해당 태그를 가지는 모든 요소에 해당 스타일을 적용한다.
- 아이디 선택자 : Id로 스타일을 적용. 해당 Id 하나에 적용된다. (id는 고유값)
  - HTML문서에서 동일한 id는 존재할 수 없다.
  - id는 속성으로 부여한다.
- 클래스 선택자 : Class로 스타일을 적용. 같은 클래스 이름을 속성으로 갖는 모든 태그에 적용.
  - 클래스 : 비슷한 특징을 갖는 요소를 지정하여 묶을 수 있다.
- 전체 선택자 : 모든 요소에 스타일을 적용한다. (속도저하 가능성 있음)
- 속성 선택자 : 특정 속성을 소유하는 모든 요소에 스타일을 적용.

### 복합선택자 :

복합 선택자 :  ( 자식 : 한 단계 아래의 요소, 후손 : 모든 하위 단계 요소

- 자식 선택자 : 선택자A의 모든 자식 중 선택자 B와 일치하는 요소 선택 a > b
- 후손 선택자 : 선택자A의 모든 후손 중 선택자 B와 일치하는 요소 선택 a b

### pseudo 클래스 : 요소의 특별한 상태를 지정할 때 사용.

- 가상의 클래스 역할

- :link

  방문하지 않은 링크의 스타일

- :visited

  방문한 링크의 스타일

- :hover

  요소에 마우스가 올라와 있을 경우의 스타일

밖의 다양한 pseudo 클래스가 있다.

## 값과 단위

### 숫자값과 백분율 :

각 태그의 속성들은 값을 가지며 다양한 단위를 가진다.

숫자값 :

- px : 픽셀. 출력화면의 해상도를 픽셀단위로 쪼갠 값이지만, CSS에서는 1/96 inch의 절대값으로 쓰인다.

- em : 현재 스타일이 지정된 요소의 font-size 기준 상대적 길이 -> 선택자에 비례

- rem : 최상위 요소의 font-size 기준 상대적 길이 -> html태그에 비례

  -> em, rem 을 통해 반응형 웹을 구현가능하다.rem을 주로 사용

백분율도 사용 가능하다.

### 색상 :

색상을 키워드로 지정하는 것은 한계가 있으며, 값으로 표현할 수도 있다.

- hex code

  #000000 구조로 이루어짐. rgb값을 16진수로 나열
  뒤의 16진수 두자릿수 추가를 통해 투명도 설정 가능 (00~FF)

- rgb

  rgb 값을 10진수로 각각 나열

  rgba 를 통해 투명도 설정 (0~1) 가능

## 텍스트와 관련된 프로퍼티

### 폰트  :   

- font-size
- font-family :
  - 폰트를 여러개 묶어 선언 가능 (사용자가 해당 폰트가 없다면 다음 폰트를 적용할 수 있도록)
  - fontsgoogle 등 웹폰트를 가져와 적용할 수도 있다.
- font-style : normal, italic, oblique
- font-weight : 폰트굵이 (bold(700), normal(400), 숫자)
- font : ~~로 한번에 적용 가능

### 텍스트 정렬

- text-align : 자신을 기준으로 텍스트 좌, 우, 중앙정렬 (left, right, center)
- line-height : 줄간격 조절 해당 줄의 height (px단위, em)
- letter-spacing : 문자 사이의 좌우간격 (px)
- text-indent : 문단의 시작부에 해당 크기만큼 들여쓰기를 함(px).

## 박스모델

 HTML의 모든 태그는 박스형태로 구성되어있다.
단순히 컨텐츠만이 아닌 컨텐츠를 감싼 모든 것을 말한다.

### Content, border

상우좌하로 적용.

- border : width style color
  - border-style :
    - dashed, solid, dotted, double 
  - border-width : px
  - border-color : color
  - border-radius : 경계선을 둥글게 한다. (모서리 반지름 px)

### padding, margin

- padding : border 내부의 여백
- margin : border 외부의 여백

서로 다른 요소의 위아래 margin이 적용되는경우 마진상쇄에 의해 큰 margin만 적용.

## BoxSizing

- box-sizing: content-box
  -> width(height) = content size
- box-sizing: border-box
  -> width(height)= content size + padding + border

## 위치와 관련된 프로퍼티

### display : 

요소가 보여지는 방식을 지정.

- block elememt :
  : width, height, margin, padding 가능
- inline element : a, img, 등
  :width, height, margin-top, margin-bottom 불가능
- inline-block
  inline 요소이지만, width, height, margin, padding 가능
- none :
  display가 브라우저에 출력되지 않음.

### position :

- static : 기본값. 좌표 사용불가
- relative : 상대위치, 기본위치 기준으로 좌표사용
- absolute : 부모나 조상 중 relative, absolute, fixed 가 선언된 곳을 기준으로 좌표적용
- fixed : 보이는 화면을 기준으로 좌표프로터피 이용해 위치 고정.
- z-index : static 외에 요소에서 사용가능. z-index 값이 큰 값이 앞으로 배치

### flexbox

부모요소 : flex container, 자식요소 : flex item으로 구성.
부모요소에 display : flex 추가해서 사용.
가로 혹은 세로 방향으로 요소를 정렬.

flex Container :

- flex-direction : flex 컨테이너 안의 item들의 방향 지정 (기본값 : row)

  - row, row-reverse, column, column-reverse

- flex-wrap : flex 컨테이너 내에서 아이템을 감싸는 여부 지정 (wrap, nowrap)

  -> flex-flow 로 direction 과 wrap 한번에 지정 가능

- justify-content : flex-direction 방향을 기준으로 수평으로 item 정렬하는 방법 정함.

  - flex-start (기본값), center, flex-end : 각각 처음 중간 끝 기준 정렬
  - space-around : 시작과 끝을 기준으로 동일한 간격으로 아이템 배치
  - space-between : 처음과 끝에 아이템 하나씩 두고 남은 간격에 아이템 배치

- align-items : flex-direction 기준 수직으로 item 정렬하는 방법 정함.

  - stretch : 기본값. 아이템들을 수직으로 늘려 정렬
  - flex-start, center, flex-end

  baseline (글자 기준 밑줄) 을 기준으로 정렬.

- align-content : flex-direction 방향 기준 수직으로 여러 줄인 item 정렬 방법

  - stretch : 기본값. 아이템들을 수직으로 늘려 정렬
  - flex-start, center, flex-end
  - space-around : 시작과 끝을 기준으로 동일한 간격으로 아이템 배치
  - space-between : 처음과 끝에 아이템 하나씩 두고 남은 간격에 아이템 배치

flex item :

- flex-grow : 확장과 관련된 속성, 기본 0
  - 1이상 값을 가지는 값들은 container 크기에 맞춰 늘려 조정.
- flex-shrink : 축소와 관련된 속성, 기본 1
  - 0이면 컨테이너 크기가 작아져도 아이템 크기 유지
  - 값이 클수록 더 많은 비율로 줄어든다.
- flex-basis : flex 아이템의 기본 크기 결정. 기본값 auto
  - px 단위 지정
- flex :
  - flex item 속성을 한번에 지정 (ex : 1, 0 , auto)

-> https://classlion.net/class/10?l_id=392 18:30~end 학습

 







