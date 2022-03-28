



## Add CSS to HTML

- CSS와 HTML을 섞는 방법

  1. HTML 파일에 CSS 코드를 추가
     head tag 안에 style tag를 작성하고 그안에 CSS 코드를 작성
  2. CSS와 HTML을 분리
     link tag를 이용해 CSS파일과 연결하고 rel을 이용해 관계명시 (stylesheet)

  



## Cascading?

- 브라우저가 CSS를 읽을 때 위에서부터 순서대로 읽는다.
- CSS를 직접 적는 것은 inline CSS, CSS 파일을 include 하는 것은 external CSS
- 만약 같은 selector를 가리키는 CSS가 여러개이면, 가장 마지막 스타일이 적용된다.



## Blocks and Inlines

- 옆에 다른 요소가 올 수 없는 것 : block (box)
- 올 수 있는 것 : inline (in the same line)
- 대표적인 inline 태그 : span, link(a), img



## Margin

- Margin은 box의 border의 바깥에 있는 공간
- block의 특징 (inline에는 없음) : margin, padding, border
- block는 높이와 너비가 있다.
- inline block 서로 바꿀 수 있다. (display속성이라고 함)
- 어떤 요소가 inline 이면, 높이와 너비를 가질 수 없다.
- margin 2개 : 상하 , 좌우  /  margin 4개 : 상 우 하 좌
- 두 요소의 border가 만나면 하나로 취급됨 : collapsing margin (상,하만) 



## Padding

- padding은 box의 border로부터 '안쪽'에 있는 공간
- 여러 div를 생성했을 때 'id'를 이용하여 div들을 구분할 수 있고, 각각 다른 속성을 적용시킬 수 있다.
- CSS로 first div에 속성을 적용 시킬 땐, #first {}  /  body,span도 같음



## Border

- border는 box의 경계를 뜻함, 보통 한종류만 사용
- 적용 예시) border: 2px solid black; (너비,스타일,색)
- *는 전체를 뜻함
- border는 inline과 block 모두에 적용됨



## Inline block

- inline-block은 block이 inline 속성을 갖게 해줌
- 옆에 둘수도 있고, 높이와 너비를 가질수 있게 됨
- 하지만 정해진 형식이 없고 깔끔하지 않음. 반응형 디자인 지원 X
- 따라서 inline block은 잘 쓰이지 않지만, 이런 방법도 있다는걸 알아두자



## Flexbox

1. flexbox를 적용하려면 자식x, 부모 엘리먼트 에게만 알려줌
2. justify-content와 align-items를 적용하기전 display:flex 적용 → flex 컨테이너가 됨
3. flex 컨테이너는 두 축이 있음 주축(main axis),교차축(cross axis)
4. 기본값으로 주축은 수평, 교차축은 수직 (변경될 수 있음)
5. justify-content는 주축에 적용, align-items는 교차축에 적용



## Flexbox and more

1. 'flex-direction'을 수정하여 justify-content나 align-items의 default를 변경가능
2. flex-direction에는 두 가지 속성, column과 row가 있다. default는 row이다.
3. flex-wrap: nowrap;을 통해 wrapping이 일어나지 않게 할 수 있다.
4. column-reverse; wrap-reverse; 를 통해 반전시키는 것도 가능



## Fixed

- position:fixed 를 통해서 요소를 고정시킬 수 있음 (스크롤위치와 관계없이)
- top, left, right, bottom 중 하나만 추가해도 원래 만들어진 위치가 무시됨



## Relative Absolute

- positon: static (default)
- position: fixed  element가 처음 생성된 자리에 고정.
- position: relative;  element가 '처음 생성된 위치'를 기준점으로, top bottom left right으로 위치를 조금씩 수정할 수 있다.
- position: absolute;
  가장 가까운 relative 부모를 기준으로 이동
- position:relative; 를 해주면 부모가 된다. 없으면 body.



## Pseudo Selector

- 좀 더 세부적으로 요소를 선택하는 기능
- id나 class를 따로 만들기보다 더 좋은 방법임. html코드를 고칠 필요가 없기 때문!
- 예시) div:first-child {}  div:last-child {}
- n번째 : div:nth-child() {}   → ()안에 odd, even, 3n+1 등등 활용 가능.



## Combinators

- div span {} : div의 밑의 모든 span을 찾아 효과를 주기
- div > span {} : div의 바로밑의 span만 찾아 효과를 주기
- div + span {} : div의 형제 중 span을 찾아 효과를 주기
- div ~ span {} : 바로 다음에 오지않아도 되는 형제 관계



## Colors and Variables

- CSS 에서 알아야할 color system

  1. hexadecimal color (16진수 컬러) : #000000의 형태
  2. RGB 방식 (디자이너들이 주로 사용) : rgb(252,206,0); 의 형태
  3. rgba(a,b,c,d); → a는 투명도를 뜻함

- Variable을 통해 CSS를 프로그래밍 언어처럼 사용

  1. :root에 변수를 추가. root는 모든 document의 뿌리가 된다

  2. "--변수이름 : ..." 의 형태로 사용, 빈칸은 - 로 채운다

  3. 변수를 사용할 곳에 var(이름); 형태로 사용



## Recap

1. combinator
   - p span{} 부모자식관계
   - p>span{} 부모와 바로 밑 자식관계
   - p+span{} 바로 다음에 오는 형제관계
   - p~span{} 바로 다음에 오지 않아도 되는 형제관계
2. attribute
   - input[type="word"]{} type="word"인 input만을 선택
   - input[type~="word"]{} "word"를 포함하는 input선택
   - input[type$="word"]{} 끝에 "word"가 오는 input 선택
   - input[type^="word"]{} 앞에 "word"가 오는 input 선택
3. state
   - :hover 커서가 올라간상태
   - :active 클릭할때
   - :focus 키보드로 선택한경우
   - :visited link에서 쓰이고 사이트를 방문한 이력이 있을경우
   - :focus-within 자식들중 하나라도 focus상태에 있다면 부모가 바뀔때 쓰임
4. pseudo element
   - ::placeholder placehoder만을 꾸밀때 사용
   - ::selection 드래그 했을때
   - ::first-letter 앞 글자에
   - ::first-line 첫 줄









