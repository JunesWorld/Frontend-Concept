# SCSS(Sass)

## Sass VS SCSS

Sass(Syntactically Awesome Style Sheets)의 3버전에서 새롭게 등장한 SCSS는 CSS 구문과 완전히 호환되도록 새로운 구문을 도입해 만든 Sass의 모든 기능을 지원하는 CSS의 상위집합(Superset) 입니다.
즉, SCSS는 CSS와 거의 같은 문법으로 Sass 기능을 지원한다는 말입니다.

더 쉽고 간단한 차이는 {}(중괄호)와 ;(세미콜론)의 유무입니다.

Sass는 선택자의 유효범위를 ‘들여쓰기’로 구분하고, SCSS는 {}로 범위를 구분합니다.

Sass는 =와 + 기호로 Mixins 기능을 사용했고,
SCSS는 @mixin과 @include로 기능을 사용했습니다.

## 장점

- CSS의 불편한 부분들을 개선하여 작성은 쉽게하고 CSS로 변환(Compile)하여 동작시킨다.

- 중첩 기능</br>
  CSS에서 반복되는 조상 요소들을 손쉽게 사용 가능하다.
  
- 변수</br>
  색상 표현(#2C2A29)과 같이 오타가 쉽게 날 수 있는 것들을 변수를 통해 표현하고 손쉽게 재활용 가능.
  
## 설치

- Project : scss-test

- Terminal
  - `npm init -y`
  - `npm i -D parcel-bundler`

- package.json
  ```JS
  "scripts": {
    "dev": "parcel index.html",
    "build": "parcel build index.html"
    },
  ```

- index.html & main.scss 생성
- index.html : parcel bundler를 통해 분석되어 CSS로 변환
  ```html
  <title>Document</title>
  <link rel="stylesheet" href="./main.scss" />
  ```
     
## 주석

- `/* */` : 변환 시 보인다.
- `/ /` : 변환 시 보이지 않는다.

## sassmeister

<a href="https://sassmeister.com" title="sassmeister로 이동!" target="_blank">sassmeister로 이동!</a>  

SCSS code를 CSS로 바로 변환하여 보여주는 Site!
