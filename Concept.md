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
- 전체 저장 : Alt + cmd + S

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
  * File – Open – 폴더 선택

## HTML(Hyper Text Markup Language) : 기획자(구조)
- 페이지의 제목, 문단, 표, 이미지, 동영상 등 웹의 구조를 담당
- 쉽게 말해 링크가 걸려있는 파일을 만들 수 있는 곳
- ! + Enter : HTML 기본 구조 생성
- ``` <!DOCTYPE html> ``` : 문서(페이지)의 HTML 버전을 지정
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

## CSS(Cascading Style Sheets) : 디자이너(스타일)
 - 실제 화면에 표시되는 방법(색상, 크기, 폰트, 레이아웃)을 지정해 콘텐츠를 꾸며주는 시각적인 표현(정적)을 담당
 - 작성방법
  >  div { color : red;   
             font-size: 100px;
        } 
        
## JavaScript : 개발자(동적)
 - 콘텐츠를 바꾸고 움직이는 등 페이지를 동작시키는 동적 처리를 담당
 - 작성방법
  > ``` Console.log(‘console에 찍힐 내용’); ```

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

## Project 시작 전 할 일
  - CSS, JS, Images 폴더 생성 후 관리 
  - ** html은 폴더 만들지 말 것 **
  - Reset.css.cdn 
   > - 브라우저 마다 기본적으로 적용되는 요소들이 있다.   예를 들어 너비 등이 있는데 이것을 초기화 시킬 때 사용 
   > - jsdelivr Github 사용
   > - ``` <head> ``` 안쪽에 넣으면 CSS 스타일 초기화
   > - ``` <link rel=”stylesheet” href=https://cdn.jsdelivr.net/npm/rest-css@5.0.1/reset.min.css> ```
  
