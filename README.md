# StudyCSS
CSS SUMMARY

---
## Tag & Code

style CSS 코드 내용을 담음 : `<style>내용</style>`

HTML 태그 내에서 속성으로 사용 : `style="color:black"`

선택자 Selector : `a { }`

효과 declaration 선택자 내에서 사용 : `{      }`  
괄호 내에 있는 것을 선언(효과)라고 지칭함.

`color:black;`에서 color는 속성, red는 value라고 부름.

링크에 존재하는 언더라인 삭제 : `text-decoration: none;`

언더라인 생성 : `text-decoration: underline;`

글자 폰트 : `font-size: 60px;`

글자 정렬 : `text-align: center;`

class : `class="클래스이름"`

style 태그 내에서 class 사용 : `.클래스이름 { }`

id : `id="아이디이름"`

style 태그 내에서 id 사용 : `#아이디이름 { }`

선택자 서열 : id > class > 태그  
(같은 서열 내에선 가장 밑에 있는 선택자가 우선 순위)

암묵적 규칙 : id 선택자는 단 한번만 등장해야한다 id는 중복돼서는 안된다.

---
## Box Model

**border** : 테두리를 뜻함  
    `border-width: 5px;`  테두리 두께
    `border-color: red;`  테두리 색
    `border-style: solid;` 테두리 스타일 단선(solid)

Block level element : 화면 전체를 크기로 쓰는 태그 ex) h1

inline element : 자기 자신의 크기만큼만 크기로 갖는 태그 ex) a

display 속성을 추가해서 block과 inline을 전환할 수 있음  
    `display:inline;` inline level로 설정  
    `display:bloack;` block level로 설정
    `display:none;` 화면에서 보이지 않게 설정

중복의 제거 : `border: 5px red solid;`로 5px red solide 모두 설정 가능

**padding** : content와 border 사이에 여백을 주는 속성

**margin** : border와 또 다른 border 사이에 여백을 주는 속성

content 폭과 높이 : width와 height 속성으로 크기 조절  
`width:100px`  
`height:40px`

---
## Grid

div : 나누기 위해 쓰이는 아무런 의미 없는 태그. Block level element이다.  
`<div>내용</div>`

span : 나누기 위해 쓰이는 아무런 의미 없는 태그 Inline level element이다.  
`<span>내용</span>`

grid-templete-colums : 열로 나누게 됨.  
`grid-template-columns: 150px 1fr;` 여기서 1fr은 자동으로 나머지를 할당하는 것인데 만약 2fr 1fr로 쓰면 첫 열은 전체의 2만큼 두번째 열은 전체의 1만큼 총 3의 크기로 나뉘어 할당된다. px값을 넣으면 고정된다.

`#idname ol { }` 이라는 id 이름 뒤에 나온 태그 이름은
그 아이디 내에 있는 하위 ol 태그들에 대한 내용을 적용할 때 사용.

## Media Query

`@media(조건식) { }` : 조건이 맞다면 { }안에 해당하는 코드가 실행됨.

`min-width: 800px` : 화면의 크기 최소값이 800px이다  
(screenWidth > 800px )

`max-width: 800px` : 화면의 크기가 최대값이 800px이다  
(screenWidth < 800px )

미디어 쿼리를 활용하면 조건문처럼 특정 조건이 되었을 때 웹브라우저에 나타나는 화면을 제어할 수 있다.

Link 문서간 연결 혹은 외부 리소스 연결 시 사용 : `<link rel="stylesheet" type="text/css" href="theme.css">`  
link 태그 사용시 웹브라우저에서 해당 문서를 다운받아서 적용하게 됨.

속성
- href 연결 문서 위치
- rel 연결 문서와의 관계
- type 연결 문서의 타입
(예제에선 type 사용 안함)

Link 태그는 근시안적으로 보면 문서 다운을 받게 되면 트래픽을 사용하게 되어 비효율적이라고 생각할 수 있다. 하지만 원시안적으로 보면
캐싱이라는 기술을 사용해서 한번 다운한 파일을 다시 읽기 때문에
엄청난 효율을 낼 수 있다.

## Projection

position 속성 : 위치를 셋팅
- static : 위에서 아래로 배치 top left 무시됨
- relative : 상대적인 위치
- absoulute : 절대적인 위치(부모 기준) 스크롤시 그에 따라 움직임
- fixed : 절대적인 위치(화면 기준) 스크롤시 화면 위치에 그대로 고정


background-color 투명색 : `background-color : rgba(0, 0, 0, 0.4);`

z-index 먼저 나타나는 순서 : 값이 클 수록 가장 위에 나타남.

margin을 0으로 설정했음에도 공백이 생기는 현상은 다른 객체가
block이여서 공백이 생기는 경우가 종종 있음.

화면이 오버가 난다면
- grid-templete-rows/columns에 fr 값 분석해보기
- display가 block으로 설정된 것 중에 화면을 넘어가는 위치에 넣어준 것이 아닌지 확인해보기

F12 눌러서 수시로 확인해보기

**a태그를 활용한 Button**

링크 State
- link : 한번도 안 누른 상태 (Default)
- visited : 한번 누름
- hover : 마우스 올려둠
- active : 마우스로 누르고 있음

링크 target
- _blacnk : 새창
- _self : 현재 프레임(기본)
- _parent : 부모 프레임
- _top : 가장 상위 프레임

이미지 링크 걸기 : a 태그 안에 img 태그를 넣음  
js 버튼 링크는 button onclick="링크주소"

**button**
`<button class="btn">button 태그</button>`
`<a href="#" class="bun">a 태그</a>`
`<input type="button" value="input 태그" class="btn">`

hover : 마우스 오버

active : 클릭한 상태

focus : 가장 중요한 상태 지정, 다른 state 를 무시함

visited : 이미 클릭한 요소

[버튼 태그 스타일링](https://blog.naver.com/brusher3063/221657821331)
[버튼 테두리 없애는 법](https://blog.naver.com/sun_ldl/221996230241)


**input**
`<input type="text">`

transparent라는 값은 부모를 따라가는 값임.

transition : CSS 점진적 변화 애니메이션 `transition: all 0.3s;`

투명도 : `opacity: 0.3;`

마우스 커서 변경 : `cursor:pointer;`

[input 스타일링](https://webdir.tistory.com/429)

# Projection 만들면서 느낀점
**HTML 설계를 잘하자. tag class id를 구조적으로 잘 설계 하자**

---
## etc

코딩은 중복의 제거가 중요하다.

CSS로 HTML을 디자인 하는 것이 훨씬 효율적이다.

style 태그 말고 속성을 통해서도 CSS를 사용할 수 있다.

같은 선택자일 때 보다 밑에 있는 선택자가 더 우선 순위이다.

태그 서열이 id > class > 태그인 이유는 포괄적인 것 일수록
그것을 전체적으로 변화시키고 특수하고 예외적인 것들만 우선적으로 변경시키는 것이 효율적이기 때문이다.

**개발자도구 F12** 혹은 **마우스 우클릭 검사**를 이용하면 HTML 문서를 볼 수 있으며 각 컨텐츠의 CSS 부분이 어떻게 작성되었는지 볼 수 있다.

[CanIUse.com](https://caniuse.com/) : HTML CSS JAVASCRIPT 기술 등을 인터넷 브라우저가 채택하고 있는 통계를 보여주는 사이트

선택자와 속성이 CSS에서 가장 중요함.

속성을 많이 알 수록 표현이 풍부하고 선택자를 많이 알 수록 속성을 잘 활용할 수 있음. 

**HTML 기본 셋팅 초기화**
``` css
html, body, div, span, applet, object, iframe,
h1, h2, h3, h4, h5, h6, p, blockquote, pre,
a, abbr, acronym, address, big, cite, code,
del, dfn, em, img, ins, kbd, q, s, samp,
small, strike, strong, sub, sup, tt, var,
b, u, i, center,
dl, dt, dd, ol, ul, li,
fieldset, form, label, legend,
table, caption, tbody, tfoot, thead, tr, th, td,
article, aside, canvas, details, embed, 
figure, figcaption, footer, header, hgroup, 
menu, nav, output, ruby, section, summary,
time, mark, audio, video {
	margin: 0;
	padding: 0;
	border: 0;
	font-size: 100%;
	font: inherit;
    vertical-align: baseline;
}
/* HTML5 display-role reset for older browsers */
article, aside, details, figcaption, figure, 
footer, header, hgroup, menu, nav, section {
	display: block;
}
body {
	line-height: 1;
}
ol, ul {
	list-style: none;
}
blockquote, q {
	quotes: none;
}
blockquote:before, blockquote:after,
q:before, q:after {
	content: '';
	content: none;
}
table {
	border-collapse: collapse;
	border-spacing: 0;
}
```

---