# HTML(Hyper Text Markup Language) : 기획자(구조)

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

### BEM(Blcok Element Modifier) : HTML 클래스 속성의 
- 요소__일부분 : Underscore(Lodash) 기호로 요소의 일부분을 표시
- 요소--상태 : Hyphen(Dash) 기호로 요소의 상태를 표시
