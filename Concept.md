# Frontend-concept

## 용어
- Grave : ` (1번 왼쪽)
- Tilde : ~
- At sign : @
- Caret : ^ (6)
- Ampersand : &
- Asterisk : *
- Verticalbar : | or ₩
- Brace : { }
- Bracket : [ ]
- Parenthesis : ( )
- Angle bracket : < >

## 단축키
- 사이드바 열고 닫기 : Cmd + B
- 파일 검색 : Cmd + P
- 모든 명령 : Cmd + shift + P
- 닫기 :Cmd + W
- 바꾸기 : Cmd + alt + f
- 줄 이동 : Alt + up/down
- 줄 복사 : Alt + shift + up/down
- 내어쓰기 : Shift + Tab
- 자동 setting : Cmd + alt + L
- 옆 파일로 이동 : Cmd + shift + [
- 화면 분할 : Cmd + \
- 전체 저장 : Alt + Cmd + S
- 내어쓰기 : Shift + Tab

## Settings
- Korean Language : 한국어로 변경 지원
- Beautify(Prettier) : 자동 정렬 기능
  > 기능 기여도 -> HookyQR 복사
  > Code -> 기본 설정 -> 바로가기 key -> Beautify Selection
  > Auto Rename Tag -> Alt + Cmd + L
- Live Server
  > HTML File에서만 작동
  > 우클릭 -> Open with Live Server
- 공백 2 설정
  > Code -> 기본설정 -> 설정 -> Editor -> Tab Size 2

## VSCode
- Project 단위 = Folder(Directory)
  - File – Open – 폴더 선택
---

## HTML(Hyper Text Markup Language) : 기획자(구조)
- 페이지의 제목, 문단, 표, 이미지, 동영상 등 웹의 구조를 담당
- 쉽게 말해 링크가 걸려있는 파일을 만들 수 있는 곳
- ! + Enter : HTML 기본 구조 생성
- ``` <!DOCTYPE html> ``` : 문서(페이지)의 HTML 버전을 지정
- 주석 
  - ``` <!-- --> ```
  - Cmd + L (windows -> Ctrl + /)
- 주요 요소
  -  ``` <div> ``` : 특별한 의미가 없는 구분을 위한 요소
  -  ``` <h1~6> ```  
     -  제목을 의미하는 요소(목차) / Block 요소
     -  숫자가 작을 수록 중요한 제목 정의
  -  ``` <p> ``` : 문장을 의미하는 요소 / Block 요소
  -  ``` <img src="삽입할 이미지 경로" alt="삽입할 이미지의 이름" /> ```
     -  src, alt는 필수 속성 / Inline 요소
     -  src에 있는 경로가 잘 못되어 액박이 뜨면 alt(alternative)가 화면에 출력
  -  ``` <ul><li>사과</li></ul> ``` : Block 요소
     - Unordered List & List Item : 서로 한 세트
     - ul>li*4 : li가 4개 자동 완성
  -  ``` <a href="http://www.naver.com" target="_blank">NAVER</a> ``` : Inline 요소
     - 다른 페이지로 이동하는 하이퍼링크 지정
     - ```target="_blank"``` : 새로운 탭에 열겠다 
  -  ``` <span>동해물</span>과 백두산이 ``` : Inline 요소
     - 특별한 의미가 없는 구분을 위한 요소 (동해물 만 어떠한 처리를 하고 싶을 때)
  - ``` <br/> ``` : 줄바꿈
  - ``` <input type="text" value="JUNE" /> ``` : Inline-block 요소
    - 사용자가 데이터를 입력하는 요소 
    - 기본적으로 Inline 성격으로 수평으로 쌓이지만 가로, 세로, 여백 조정 가능
    - type -> 글자입력창 
    - value -> 입력창 안에 기본적으로 입력된 값 
    - placeholder -> 사용자가 입력할 값의 힌트(이름을 입력하세요)
    - checkbox(checked -> 미리 체크 되어 있음)
      - ``` <label><input type="checkbox" checked /> Apple </label> ``` 
      - ``` <label><input type="checkbox" /> Banana </label> ``` 
    - radio : 택 1 (name으로 그룹 지정)
      - ``` <label><input type="radio" name="fruits" /> Apple </label> ``` 
      - ``` <label><input type="radio" name="fruits" /> Banana </label> ``` 
   - 테이블 요소
    ``` 
        <table>
          <tr>
           <td>A</td><td>B</td>
          </tr>
          <tr>
           <td>C</td><td>D</td>
          </tr>
         </table> ```
         -> AB
            CD
- 전역 속성
  - ``` <태그 title="설명"></태그> ``` : 요소의 정보나 설명을 지정
  - ``` <태그 style="스타일"></태그> ``` : 요소에 적용할 스타일(CSS) 지정
  - ``` <태그 class="이름"></태그> ``` : 요소를 지칭하는 중복 가능한 이름
    - ``` <span class="red"> 글자 </span> ``` 
    - 색으로 예를 들면 css에서 전역을 뜻하는 .을 붙여 ``` .red { color: red;} ```
  - ``` <태그 id="이름"></태그> ``` : 요소를 지칭하는 고유한 이름
    - ``` <span id="abc"> 글자 </span> ``` 
    - 색으로 예를 들면 css에서 전역을 뜻하는 #을 붙여 ``` #abc { color: red;} ```
    - 고유해야함!
  - ``` <태그 data-이름="데이터"></태그> ``` : 요소에 데이터를 지정
    - ``` <div data-fruit-name="apple">사과</div> ```
    - 데이터를 저장해 놓고 JS에서 사용       
 #### ``` <html> ``` : 문서의 전체 범위
  - ``` <html lang=”ko”> ``` : 한국어 설정
 #### ``` <head> ``` : 문서의 정보를 나타내는 범위(제목, 설명, 스타일(CSS))
  - 눈에 보이지 않음
  - Link : ``` <link rel=”stylesheet” href=”./main.css/> ```
   > -  href에 ./(css파일 이름) -> css파일을 가져오겠다
   > -  ``` <link rel=”icon” href=”./favicon.png>  ``` -> Favicon : Title 옆 Logo
  - Script : ``` <script src=”./(JS파일이름)”></script>```
   > - ``` <script src=”./main.js”></script> ```
   > - 작업자관리창(F12) -> Console에 찍힌다.
  - Style : HTML파일에서 CSS, JavaScript 스타일 변경
   > - CSS : ``` <style> div{text-decoration:underline;}</style> ``` 
   > - JavaScript : ``` <style> console.log(‘Hello world!’)</style> ```
  - Title : HTML 문서의 제목을 정의
  - META : HTML문서의 제작자, 내용, 키워드 같은 여러 정보를 검색 엔진이나 브라우저에게 제공
   > ``` <meta name=”author” content=”JUNE”/> ```
   > ``` <meta name=”정보의 종류” content=”정보의 값”/> ```
 #### ``` <body> ```  : 문서의 구조를 나타내는 범위(로고, 헤더, 푸터, 내비게이션 등) -> 눈에 보여지는 구조
  > - ``` <a href=http://naver.com> NAVER </a> ```
  > > - href : 이동 경로
  > > - Naver 누르면 페이지로 이동

 #### ``` Tag ``` 
  - 기능의 확장 : 속성과 값을 사용
    - <태그 속성(Attribute) = "값(Value)"> 내용 </태그>
    - ``` <img src="이미지 경로(필수 속성)" alt=""> ```
  - Empty Tag : ``` <태그/> ```
    - ``` <input type(데이터 타입) = "text"(사용자에게 일반 텍스트를 입력 받음)/> ``` : 사용자가 데이터를 입력하는 요소(태그)
  - 줄 바꿈 : ``` <br> ```

 #### ```글자와 상자``` : 요소가 화면에 출력되는 특성
- Inline 요소 : "글자"를 만들기 위한 요소들
  - ``` <sapn> 대표적인 인라인 요소!(영역구분) </span> ```
    - 줄바꿈 = 띄어쓰기
    - ```<sapn style="width(height):100px;">Hello</span>``` : 글자 취급하기 때문에 가로 세로 너비 지정하는 속성을 줘도 반응 X
    - ```<sapn style="margin(padding):20px 20px;">Hello</span>``` : 좌우 여백 조절만 가능(위 아래 여백은 X)
    - 인라인(글자) 요소 안에는 블락(상자)요소(```<div>```) 넣을 수 없다
- Blcok 요소 : "상자(레이아웃)"를 만들기 위한 요소들 
  - ```<div style="width(height):100px;">Hello</div>```
  - 제어 가능(width, height, margin, padding)
  - 위에서 아래로 수직으로 쌓인다
  - 가로 너비는 최대한 늘어나려하고 세로 너비는 최대한 줄어든다. 
  - 블록 요소 안에 인라인, 블록 요소 모두 포함 가능

---

## CSS(Cascading Style Sheets) : 디자이너(스타일)
 - 실제 화면에 표시되는 방법(색상, 크기, 폰트, 레이아웃)을 지정해 콘텐츠를 꾸며주는 시각적인 표현(정적)을 담당
 - HTML 요소를 CSS에서 style 변경
 - 작성방법
    - ``` 선택자 {속성 : 값;} ```
    - 선택자 : 스타일(CSS)을 적용할 대상
    - 속성 : 스타일(CSS)의 종류
    - 값 : 스타일(CSS)의 값
    - : -> 은 / ; -> 이다.
```
div { color : red;   
      font-size: 100px;
        } 
```
 - 주석 : Cmd + /
    -  ``` /* 설명 작성 */ ```
 
 - 선언 방식
    - 내장 방식 : HTML에 Style의 내용(Contents)으로 스타일을 작성하는 방식 / 권장 X
       ```
       <style>
        div {
          color: red;
          margin: 20px;
          }
        </style>
        ```
    - 인라인 방식 : 요소의 style 속성에 직접 스타일을 작성하는 방식(선택자X) / 권장 X
        ```
        <div style="color: red; margin: 20px;"></div>
        ```
    - 링크 방식 : ``` <link/> ```로 외부 CSS 문서를 가져와서 연결하는 방식(병렬)
        ```
        <link rel="styleshee" href="./css/main.css">
        ```
    - @import 방식 : CSS의 @import 규칙으로 CSS 문서 안에서 또 다른 CSS 문서를 가져와 연결하는 방식(직렬) 
        ```
        <link rel="styleshhet" href="./css/main.css">
        [mian.css]
        @import url("./box.css);
        div {
          color: red;
          margin: 20px;
          }
        [box.css]
        .box {
          background-color : red;
          padding: 20px;
          }
         ```
 - 선택자
    - 기본 
      - *(전체 선택자) : 모든 요소를 선택
      - 태그 선택자(div, li...) : 태그 이름으로 요소 선택
      - 클래스 선택자(.fruits) : HTML에서 class 지정(fruits)해주고 선택(CSS에서 앞에 .을 붙인다)
      - 아이디 선택자(#abc) : HTML id 속성의 값이 abc인 요소 선택(CSS에서 앞에 #을 붙인다)
    - 복합
      - 일치 선택자 : 선택자 ABC와 XYZ를 동시에 만족하는 요소 선택(ex.태그.클래스)
        ```
        <sapn class-"orange">오렌지</span>
        span.orange {
          color : red;
         }
        ```
       - 자식 선택자 : ABC>XYZ / 해석은 뒤에서 부터 (orange class이지만 ul의 자식인 것만)
          ```
          ul>.orange {
            color: red;
            }
          ```
        - 하위 선택자 : ABC(띄어쓰기)XYZ / div안에 있는 모든 class 요소 선택
          ```
          div(띄어쓰기).orange {
            color: red;
            }
           ```
        - 인접 형제 선택자 : ABC + XYZ / 선택자 ABC의 다음 형제 요소 XYZ "하나" 선택
          ```
          .orange + li {
            color: red;
            }
           ```
         - 일반 형제 선택자 : ABC ! XYZ / 선택자 ABC의 다음 형제 요소 XYZ "모두" 선택
            ```
            .orange ~ li {
              color: red;
             }
            ```
    - 가상 클래스 : 어떠한 행동을 했을 때 동작하는 방식
      - ABC:hover / 마우스 올리기
      - ABC:active / 마우스 클릭
        ```
        .box {
          width: 100px;
          height: 100px;
          background-color: orange;
          transition: 1s;
          }
        .box:hover {
          width: 300px;
          background-color: royalblue;
          }
        ```
      - ABC:focus / 데이터 입력 받는 형식에서만 동작, 대표적으로 input
        - 데이터 입력 받는 형식이 아닐 때 사용법 : HTML -> tabindex
          ```
          <div class="box" tabindex="-1"></div>
          ```
      - ABC:first(last)-child / 선택자 ABC가 형제 요소 중 첫째라면 선택 / span태그 중에서 첫번째
        ```
        <div class="fruits">
          <span>딸기</span>
          <span>수박</span>
          <div>오렌지</div>
          <p>망고</p>
          <h3>사과</h3>
        </div>
        ```
        ```
        [딸기]
        .fruits span:first-child {
          color: red;
          }
        ```
      - ABC:nth-child(n) / 선택자 ABC가 형제 요소 중 (n)번째라면 선택 (짝수:2n / 홀수:2n+1 / 두번째 부터 전부: n+2)
        ```
        [수박]
        .fruits *:nth-child(2) {
          color: red;
          }
        ```
      - ABC:not(XYZ)
        ```
        .fruits *:not(span) {
          color: red;
          }
        ```
    - 가상 요소
      - ABC::before(after) / content 속성 무조건 사용해야함 /선택자 ABC 요소의 내부 앞(뒤)에 내용을 삽입(Inline)
        ```
        <div class="box">
          Content
        </div>
        .box::before {
          content: "앞";
          display: blcok;(inline->block/가로, 세로 변경 가능하기 위함)
          width: 30px;
          height: 30px;
          }
         -> 앞 Content(Inline)
         ```
    - 속성
      - [ABC] : 속성 ABC를 포함한 요소 선택
        ```
        <input type="text" value="June">
        <input type="password" value="June">
        <span data-fruit-name="apple">사과</span>
        ```
        ```
        [type] / [type="password"] / [data-fruit-name] {
          background-color: orange;
         }
         ```
 - 상속되는 CSS 속성들 : 모두(모든X) 글자/문자 관련 속성들!
    - font-style
    - font-weight
    - font-size
    - line-height
    - font-family : 폰트(서체)
    - color
    - text-align : 정렬
    - 강제 상속 = inherit / 글자가 아닌 다른 속성들 상속하고 싶을 때 사용
       ```
       .parent {
          width: 300px;
          height: 200px;
          background-color: orange;
         }
       .child {
          width:100px;
          height: inherit;
          background-color: inherit;
          position: fixed;
          top: 100px;
          right: 10px;
         }
       ```
 - 우선순위
     ```
     <div
        id="color_yellow"
        class="color_green"
        style="color: orange;"> -> 인라인 선언(1000점)
        Hello World!
     </div>
     
     -> Hello World는 무슨 색으로 출력?
     
     div {color: red !important; } -> !important(가장 높은 점수!)
     #color_yellow {color: yellow; } -> ID선택자(100점)
     .color_green {color: green; } -> Class선택자(10점)
     div {color: blue; } -> Tag선택자(1점)
     * {color: darkblue; } -> 전체선택자(0점)
     body {color: violet; } -> 상속(X)
     ```
 - 속성(Properties)
    - Inline요소(ex.span) : 줄어들려고 함
    - Block요소(ex.div) : 늘어나려고 함
    - width, height : 요소의 가로/세로 너비
      - 기본값 : auto(브라우저가 너비를 계산)
      - 단위 : px, em, vw 등 단위로 지정
      - max-width,height : 기본값 = none
      - min-width,height : 기본값 = 0
      
    - margin : 요소의 외부 여백(공간)을 지정하는 단축 속성(음수로 사용 가능)
      - margin-top/right/bottom/left
         ```
         margin: 10px(top,bottom) 20px(left, right);
         margin: 10px(top) 20px(left, right) 30px(bottom);
         margin: 10px(top) 20px(right) 30px(bottom) 40px(left); -> 시계방향
         ```
      - 0 : 외부 여백 없음
      - auto : 브라우저가 여백을 계산(가운데 정렬)
      - 단위 : px, em, vw 등 단위로 지정
      - % : 부모 요소의 가로 너비에 대한 비율로 지정   
       
    - padding : 요소의 내부 여백(공간)을 지정하는 단축 속성 -> 요소의 크기가 늘어남
      - 0 : 내부 여백 없음
      - 단위 : px, em, vw 등 단위로 지정
      - % : 부모 요소의 가로 너비에 대한 비율로 지정 
      - padding-방향 : margin과 동일
      
    - border: border-width(선-두께) border-style(선-종류) border-color(선-색상) 
      - 요소의 테두리 선을 지정하는 단축 속성
      - 기본값 = border: medium none black;
      - border-width(단위로 사용할 것, margin처럼 방향 지정 가능)
        - medium
        - thin
        - thick
        - 단위 : px, em, %
      - border-style(선의 종류, 방향 지정 가능)
        - none
        - solid : 실선
        - dashed : 파선 (---)
        - dotted : 점선 (...) 
        - double : 두 줄 선
        - groove : 홈이 파여있는 모양
        - ridge : 솟은 모양(groove의 반대)
        - inset :요소 전체가 들어간 모양
        - outset : 요소 전체가 나온 모양
      - border-color(방향 지정 가능)
        - 기본값 : black
        - transparent : 투명
      - border-right: 두께 종류 색상;
      - border-right-widht: 두께;
      - border-right-style: 종류;
      - border-right-color: 색상; 
      - border-radius : 요소의 모서리를 둥글게 깎음(border-raidus: 0 10px 0 0; -> 오른쪽 모서리)
    
    - box-sizing : 가로, 세로 너비 그대로 사용하고 싶다면 border-box 사용
      - box-sizing: border-box; 
      - content-box(기본값) : 요소의 내용(content)으로 크기 계산
      - border-box : 요소의 내용 + padding + border로 크기 계산

    - overflow : 요소의 크기 이상으로 내용이 넘쳤을 대, 보여짐을 제어하는 단축 속성
      - 기본값 : visible -> 넘친 내용을 그대로 보여줌
      - overflow-x / overflow-y : 개별 속성으로 표현 가능
      - hidden : 넘친 내용을 잘라냄
      - scroll : 넘친 내용을 잘라내고 스크롤바 생성
      - auto : 넘친 내용이 있는 경우에만 잘라내고 스크롤바 생성
      - scroll 보다는 auto 사용

    - display : 요소의 화면 출력(보여짐) 특성
      - inline 요소에서 block 요소를 사용해야할 때 : display: block;
      - block / inline / inline-block : 각 요소에 이미 지정되어 있는 값
      - flex(1차원 레이아웃) / grid(2차원 레이아웃) / none(보이짐x, 화면에서 사라짐) : 따로 지정해서 사용하는 값
      - 기타 : table, table-row, table-cell ...

    - opacity : 요소 투명도
      - 기본값 : 불투명
      - 0~1 사이의 소수점 숫자
   
    - 글꼴
      - font-style : 글자의 기울기
        - 기본값 : normal
        - italic : 이텔릭체
      - font-weight : 글자의 두께(100단위)
        - 기본값 : normal, 400
        - bold, 700 : 두껍게
      - font-size : 글자의 크기
        - 기본값 : 16px
        - 단위 : px, em, rem
      - line-height : 한 줄의 높이, 행간과 유사
        - 기본값 : 브라우저의 기본 정의를 사용
        - 숫자(권장) : 요소의 글꼴 크기의 "배수"로 지정(ex.20px -> 20배)
        - 단위 : px, em, rem, % 
      - font-family: 글꼴1, "글꼴2", ...글꼴계열(필수로 작성!);
        - 글꼴(서체) 지정
        - 글꼴이 많이 지정해 놓는 이유는 없을 경우 사용하기 위함
        - 글꼴에 띄어쓰기가 있을 때는 ""로 묶어서 명시
        - 글꼴 계열
          - serif : 바탕체
          - sans-serif : 고딕체 계열
          - monospace(추천!) : 고정너비(가로폭이 동등) 글꼴
          - cursive : 필기체 계열
          - fantasy : 장식 글꼴 계열

    - 문자
      - color : 글자의 색상
        - 기본값(검정색) : rgb(0, 0, 0)
      - text-align : 문자의 정렬 방식
        - left / right /center /justify(양쪽 정렬)
      - text-decoration : 문자의 장식(선)
        - none / underline / overline / line-through(중앙선)
        - a 태그에는 기본적으로 밑줄이 추가되어 있기 때문에 none을 사용해야한다
      - text-indent : 문자 첫 줄의 들여쓰기
        - 내어쓰기(outdent) : 음수를 사용
        - 들여쓰기 없음 : 0
        - px, em, rem 

    - 배경
      - background-color : 요소의 배경 색상
        - 기본값 : transparent(투명한)
        - 지정 가능한 색상
      - background-image : 요소의 배경 이미지 삽입
        - 기본값 : none
        - url("경로") : 이미지 경로
      - background-repeat : 일반적으로 배경 이미지는 반복되어 나타나기 때문에 제어
        - 기본값 : repeat(이미지를 수직, 수평 반복)
        - repeat-x : 수평 반복
        - repeat-y : 수직 반복
        - no-repeat : 반복 없음
      - background-position : 요소의 배경 이미지 위치
        - 기본값 : 0% 0% (0~100% 사이의 값)
        - 방향 : top / bottom / left / right / center
          - background-position: top right; -> 오른쪽 위
        - 단위(x축, y축) : px, em, rem
      - background-size : 요소의 배경 이미지 크기
        - 기본값 : auto(이미지의 실제 크기)
        - 단위 : px, em, rem
        - cover : 비율을 유지, 요소의 더 넓은 너비에 맞춤
        - contain : 비율을 유지 요소의 더 짧은 너비에 맞춤
      - background-attachment : 요소의 배경 이미지 스크롤 특성
        - 기본값 : scroll(이미지가 요소를 따라서 같이 스크롤)
        - fixed : 이미지가 뷰포트에 고정, 스크롤X
        - local : 요소 내 스크롤 시 이미지가 같이 스크롤 

    - 배치(기준을 먼저 잡고 위치 값을 설정해야한다)
      - position : 요소의 위치 지정 기준
        - 기본값 : static(position 속성이 없다고 보면 되고 배치 할 수 있는 기준이 없다)
        - relative : 요소 자신을 기준
          - 위치를 조정하면 relative가 사용된 영역은 그대로 확보하고 있다 
        - absolute : 위치 상 부모 요소를 기준
          - absolute를 사용했다면 부모 요소에 position값이 있어야하는데 relative가 가장 무난하다
          - 1, 2(absolute), 3 : 2번은 이제 1, 3번과 상호작용 X -> 공중에 떠 있게 출력
          - 조상 요소 = relative / 부모 요소 = static -> 조상 요소 기준으로 배치
          - 조상요소에도 없다면 기준 position이 나올 때까지 올라간다
        - fixed : 뷰포트(브라우저)를 기준
          - 항상 화면에 고정되는 기능
      - 위치(숫자값으로도 설정 가능, 음수도 가능) : top / bottom / left / right / z-index 
        - 요소의 각 방향별 거리 지정
        - 기본값 : auto(브라우저가 계산)
        - 단위 : px, em, rem
      - 요소 쌓임 순서(Stack Order) : 어떤 요소가 사용자와 더 가깝게 있는지(위에 쌓이는지) 결정
        1. 요소에 position 속성의 값이 있는 경우 위에 쌓임(기본값 static 제외 / relative, absolute, fixed)
        2. 1번 조건이 같은 경우, z-index 속성의 숫자 값이 높을 수록 위로 쌓임
        3. 1번과 2번 조건까지 같은 경우, HTML에서 늦게 작성된 것일 수록 위에 쌓임
        - z-index : 요소의 쌓임 정도를 지정(숫자가 커지지 않게 잘 관리해야한다)
          - auto(=0) : 부모 요소와 동일한 쌓임 정도
          - 숫자 : 숫자가 높을 수록 위에 쌓임
       - position 속성의 값으로 absolute, fixed가 지정된 요소는 display 속성이 block으로 변경됨 (relative는 안된다!)
          - 가로 세로 값을 가질 수 있음

    - 플렉스 : 수직으로 있던 요소들이 수평으로 정렬
      - Flex Container = display:flex; 값이 있는 곳(부모 요소)
        - 정 가운데 정렬 예시
          ```
          .container {
            width: 500px;
            height: 300px;
            background-color: royalblue;
            display: flex;
            justify-content: center;
            align-items: center;
          }
          ``` 
        - 속성
          - display : Flex Container의 화면 출력(보여짐) 특성
            - Container를 만들어야하고 그 안 속성에 display:flex;가 있어야 한다
            - flex : 블록 요소와 같이 Flex Container 정의(Block요소이기 때문에 밑으로 쌓임)
            - index-flex : 인라인 요소와 같이 Flex Container 정의(container가 inline 요소처럼 동작 할 수 있게 한다 -> 옆으로 쌓임)
          - flex-flow
          - flex-direction : 주 축을 설정(수평정렬(row) or 수직정렬(column))
            - 기본값 : row(행 축 / 좌->우)
            - row-reverse : 행 축 / 우->좌
            - column : 열 축 / 위->아래
            - column-reverse : 열 축 / 아래->위
          - flex-wrap : Flex Items 묶음(줄 바꿈) 여부
            - 한 줄로 정렬하는 속성 때문에 넘치는 경우가 있다. 이 때 넘치는 부분은 줄 바꿈!
            - 기본값 : nowrap(묶음, 요소들의 줄 바꿈 없음) -> 한 줄로만 정렬
            - wrap : 여러 줄로 묶음
            - wrap-reverse : wrap의 반대 방향으로 묶음
          - justify-content : 주 축의 정렬 방법(수평 정렬)
            - 기본값(왼쪽 정렬) : flex-start(Flex Items를 시작점으로 정렬)
            - flex-end(오른쪽 정렬) : Flex Items를 끝점으로 정렬
            - center(가운데 정렬) : Felx Items를 가운데 정렬
            - space-between : 각 Flex Item 사이를 균등하게 정렬
            - space-around : 각 Flex Item의 외부 여백을 균등하게 정렬
          - align-content : 교차 축의 "여러 줄" 정렬 방법(수직 정렬)
             ```
             [위에서부터 정렬]
             display: flex;
             flex-wrap: wrap;
             align-content: flex-start;
             ```
            - 조건 
              - Items들이 두 줄 이상이어야한다.
              - flex-wrap: wrap; 이 있어야 한다. 
            - 기본값 : stretch(Flex Items를 시작점으로 정렬)
            - flex-start : Flex Items를 시작점으로 정렬
            - flex-end : Flex Items를 끝점으로 정렬
            - center : Flex Items를 가운데 정렬
          - align-items : 교차 축의 "한 줄" 정렬 방법
            - 기본값 : stretch(Flex Items를 교차 축으로 늘림)
            - flex-start : Flex Items를 각 줄의 시작점으로 정렬
            - flex-end : Flex Items를 각 줄의 끝점으로 정렬
            - center : Flex Items를 각 줄의 가운데 정렬
            ```
            [수직 상단 정렬]
            display: flex;
            align-items: flex-start;
          
            [수직 가운데 정렬]
            display: flex;
            align-items: center;
          
            [수직 하단 정렬]
            display: flex;
            align-items: end;
            ```
      - Flex items = Flex Container가 된 자식 요소들(한 줄 일 때 사용)
        - 속성
          - order : Flex Item의 순서(음수 가능)
            - 기본값 : 0(순서 없음)
            - 숫자 : 숫자가 작을 수록 앞에 정렬
          - flex
          - flex-grow : Flex Item의 증가 너비 비율(비율을 넣어주면 남는 부분 채운다)
            - 기본값 : 0(증가 비율 없음)
            - 숫자 : 증가 비율
          - flex-shrink : Flex Item의 감소 너비 비율
            - 기본값 : 1 (Flex container 너비에 따라 감소 비율 적용)
            - 숫자 : 감소 비율
            - 요소들이 찌그러지는 현상을 막고 싶을 때 = flex-shrink: 0;
          - flex-basis : Flex Items의 공간 배분 전 기본 너비
            - 기본값 : auto(요소의 Content 너비)
            - 단위 : px, em, rem
          - align-self

    - 전환
      - transition : 요소의 전환(시작과 끝) 효과를 지정하는 단축 속성
        ```
        div {
          width: 100px;
          height: 100px;
          background-color: orange;
          transition: 
            width .5s;
            background-color 2s;
        }
        div:active {
          width: 300px;
          background-color: royalblue;
        }
        ```
        - trainsition: [속성명] [지속시간] [타이밍함수] [대기시간];
        - trainsition-property/duration/timing-function/delay
        - 지속시간(duration) : 단축형으로 작성할 때, 필수포함 속성!
        - transition-property : 전환 효과를 사용할 속성 이름을 지정
          - 기본값 : all(모든 속성에 적용)
          - 속성이름 : 전환 효과를 사용할 속성 이름 명시
        - transition-duration : 전환 효과의 지속시간을 지정
          - 기본값 : 0s (전환 효과 없음)
          - 시간 : 지속시간(s)을 지정
        - transition-timing-function : 전환 효과의 타이밍(Easing) 함수를 지정
          - [Google] easing functions / + mdn / tweenmax easing(GreemnSock) -> Easing 함수 치트 시트 참고
          - 기본값 : ease(느리게 - 빠르게 - 느리게)
            - cubic-bezier(0.25, 0.1, 0.25, 1)
          - linear : 일정하게
          - ease-in : 느리게 - 바쁘게
          - ease-out : 빠르게 - 느리게
          - ease-in-out : 느리게 - 빠르게 - 느리게
          - cubic-bezier(n, n, n, n) : 자신만의 값을 정의
          - steps(n) : n번 분할된 애니메이션
        - transition-delay : 전환 효과가 몇 초 뒤에 시작할지 대기시간 설정
          - 기본값 : 0s
          - 시간 : 대기시간(s)을 지정

    - 변환
      - transform: 변환함수1 변환함수2 변환함수3 ...;
      - transform: 원근법 이동 크기 회전 기울임;
      - 2D 변환 함수
        - 단위 : px
          - translate(x, y) : 이동(x축, y축)
          - translateX(x) : 이동(x축)
          - translateY(y) : 이동(y축)
        - 단위 : 없음(배수) / 숫자
          - scale(x, y) : 크기(x축, y축)
        - 단위 : deg
          - rotate(degree) : 회전(각도)
          - skewX(x) : 기울임(x축)
          - skewX(y) : 기울임(y축)
       - 3D 변환 함수
          - rotateX(x) : 회전(x축)
          - rotateY(y) : 회전(y축)
          - perspective(n) : 원근법(거리) / 단위 : px (perspective 함수)
            - 제일 앞에 작성해야 함!
            - transform: perspective(500px) rotate(45deg);
            - (추천!!) 또는, 부모요소에 추가하여 원근법 표현 (perspective 속성)
              - perspective: 500px;
              - transform: rotateY(45deg);
          - backface-visibility : 3D 변환으로 회전된 요소의 뒷면 숨김 여부
            - 기본값 : visible
            - hidden

 - 단위
    - px : 픽셀
    - % : 상대적 백분율
    - em : 요소의 글꼴 크기
    - rem : 루트(최상위) 요소(HTML)의 글꼴 크기
    - vw : 뷰포트 가로 너비의 백분율
    - vh : 뷰포트 세로 너비의 백분율
 
 - 색상 표현
    - 색상이름
      - 브라우저에서 제공하는 색상 이름
      - red, tomato, royalblue...
    - HEX 색상 코드(추천!)
      - 16진수 색상(Hexadecimal Colors)
      - #000, #FFFFFF
    - RGB
      - 빛의 삼원색
      - rgb(255, 255, 255)
    - RGBA
      - 빛의 삼원색 + 투명도
      - rgba(0, 0, 0, 0~1(투명도)) 
---

## JavaScript : 개발자(동적)
 - 콘텐츠를 바꾸고 움직이는 등 페이지를 동작시키는 동적 처리를 담당
 - 작성방법
    > ``` Console.log(‘console에 찍힐 내용’); ```
 - 표기법
    - dash-case(kebab-case)
    - snake_case
    - camelCase
    - ParcelCase

---

## 개발자 도구(F12)
 - 구성 요소 보는 법
  > Elements –> 맨 왼쪽 –> 알고 싶은 구성요소에 마우스
 - Image 가져오기
  > - 원하는 Logo click
  > - Styles –> Image URL 우클릭 –> Open In a New Tab –> 저장
  > - 작업하고 있는 Project File에 Image 저장
  > - ``` <body> ``` 부에 작성
   > - ``` <img src=”./(경로)” alt=”(오류 시 대체 글자)”> ```  
   > - 경로 -> 이미지 저장한 경로 or Open In a New Tab 경로
 - Elements
  > - Styles에서 임시로 바꿔 볼 수 있다.
  > -	Styles -> hov (호버) :hover
  > - Couputed : CSS 적용된 내용 값 확인 가능

  ---
  
## Project 시작 전 할 일
  - CSS, JS, Images 폴더 생성 후 관리 
  - ** html은 폴더 만들지 말 것 **
  - Reset.css.cdn 
   > - 브라우저 마다 기본적으로 적용되는 요소들이 있다. 예를 들어 너비 등이 있는데 이것을 초기화 시킬 때 사용 
   > - jsdelivr Github 사용
   > - ``` <head> ``` 안쪽에 넣으면 CSS 스타일 초기화
   > - ``` <link rel=”stylesheet” href=https://cdn.jsdelivr.net/npm/rest-css@5.0.1/reset.min.css> ```
  
