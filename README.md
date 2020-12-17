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
## etc

코딩은 중복의 제거가 중요하다.

CSS로 HTML을 디자인 하는 것이 훨씬 효율적이다.

style 태그 말고 속성을 통해서도 CSS를 사용할 수 있다.

같은 선택자일 때 보다 밑에 있는 선택자가 더 우선 순위이다.

태그 서열이 id > class > 태그인 이유는 포괄적인 것 일수록
그것을 전체적으로 변화시키고 특수하고 예외적인 것들만 우선적으로 변경시키는 것이 효율적이기 때문이다.


---