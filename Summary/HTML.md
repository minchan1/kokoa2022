



# 0311

(NC-1)



## 웹사이트의 구성

- 웹사이트는 단지 text 파일이다
- 적절한 위치에 알맞는 text 사용 → 웹사이트 구현
- 브라우저에게 코드를 전달 → 브라우저가 코드구현, 웹사이트 출력
- 어떤 종류의 text를 써야하는지, text를 어디에 써야 하는지를 배우자
- 웹사이트는 3개의 언어로 구성 - HTML, CSS, Javascript



## HTML

- Markup (= content) 언어
- 브라우저에게 웹사이트의 content가 어떻게 구성되는지 설명함
- ex) 이것은 title 이다, 이것은 link 이다, ... 등등



## CSS

- 디자인과 스타일을 위한 언어

- CSS는 HTML과 함께 사용해야함

- 브라우저에게 웹사이트의 content가 어떻게 보여야하는지 알려줌

- ex) 제목의 색상, 이미지의 크기, ... 등등

  

## Javascript

- 웹사이트를 동적으로 만들어 줌 (상호작용)
- HTML, CSS와 달리 프로그래밍 언어로 분류
- 필수요소는 아님





# 0313



## VSC

- 코드 편집기, VSC 없이도 웹페이지를 만들 수 있지만, 좋은 확장프로그램이 많다.
- WakaTime → 사용한 시간을 알려줌
- Community Material Theme → VSC 테마 변경 익스텐션
- IMaterial Icon Theme → 아이콘 표시해주는 익스텐션



## 브라우저

- 브라우저는 HTML문법을 따르지 않아도 언제나 사용자에게 콘텐츠를 보여준다
- 단점 : HTML 파일에 에러가 있어도 알려주지 않는다
- 장점 : 우리가 실수를 하더라도 유저는 콘텐츠를 볼 수 있음



## Tag

- 태그 사이에 넣는 내용을 통해서 content를 제시해준다
- 알맞은 위치에 알맞는 태그를 사용하면 브라우저가 이해하고 표시해줌
- /이 붙으면 태그가 끝남을 의미. 태그를 제대로 닫아줘야 제대로 작동함



## Attributes

- a = anchor를 뜻함, link의 기능
- attributes = 태그에 부여하는 추가적인 정보
- href = http reference라고 함 (anchor 태그에만 추가 가능)
- target = 기본값은 _self, _blank 입력 시 새 탭에서 링크가 열림
- img = 다른 태그와 다르게 /로 닫는 태그가 없다 (자체 닫기 태그이기 때문)
- src = img 안에 사진을 집어넣음 (img에서 작동)



## Tags and Head

- 같은 폴더에 이미지가 있을 경우 src=이미지 이름.확장자
- 다른 폴더일 경우 폴더/이미지.확장자 (경로 표기 법)
- 모든 HTML 문서는 <!DOCTYPE html>로 시작
- HTML 문서는 HEAD(웹사이트의 환경 설정), BODY(사용자가 볼 수 있는 내용)로 구성



## Head

- meta : 부가적인 요소 (content, name attribute를 가짐)
- charset : 한글 등 문자 표시 (utf-8)
- language : 사이트에 사용되는 언어 표기 (검색엔진에게 알려줌)
- HEAD 태그는 보이지 않는 사이트 설정들을 바꿔준다!! 
- og태그(open graph)는 콘텐츠의 요약내용을 SNS에 최적화된 데이터로 가지고 갈 수 있도록 설정 ex) og:~~ 카카오톡, fb:~~ 페이스북, twitter:~~ 트위터





# 0314



## Tags and IDs

- lable은 input과 함께 작동한다. (label이 input을 activate)
- lable 태그에 for=" ", input 태그에 id=" "  같은 id값이 들어가야 함
- id는 body 안에 어떤 태그에든 넣을 수 있는 attribute임
- element당 하나의 id 만을 가질 수 있다 (고유식별자, id중복시 작동X)
- CSS가 태그를 지정하여 꾸미기 위해선 ID가 필요함!



## Semantic HTML

- non-semantic : html에서 의미 없는 태그 but 기능은 있음 (div)
- semantic : 문서를 보기만해도 그 의미를 짐작할 수 있음 (header,main,footer 등)
- div나 span으로 바꿔도 문제없지만, 코드를 이해하기 번거롭다
- 코드를 이해하기 쉽도록 semantic tag를 활용하자
- p : paragraph에 적합, span : 짧은 텍스트에 적합, div : box의 개념, 줄 구분해줌

















