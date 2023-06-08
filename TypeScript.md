# TypeScript

= Language / Typed Superset of JavaScript
= compiles to plain(Browser or Node.js 실행 환경에서 이해할 수 있는) JavaScript

## Typed JavaScript at any Scale

- TypeScript extends JavaScript by adding types.
- By understanding JavaScript,  
TypeScript saves you time catching errors and providing fixes</br> 
before you run code.
- Any browser, anyOS, anywhere JavaScript runs. Entirely Open Source.

## TypeScript는
- Programming Language 언어
- Complied Language
  - 전통적인 Compiled Language와는 다른 점이 많다.
  - 그래서 'Transpile' 이라는 용어를 사용하기도 한다.
- JavaScript는 'Interpreted Language'이다.

## Compiled VS Interpreted

Complied | Interpreted
:--:|:--:
컴파일이 필요 O | 컴파일이 필요 X
컴파일러가 필요 O | 컴파일러가 필요 X
컴파일하는 시점 O </br>(컴파일 타임) | 컴파일 하는 시점 X
컴파일된 결과물을 실행 | 코드 자체를 실행
컴파일된 결과물을 실행하는 시점 | 코드를 실행하는 시점 O </br>(Runtime)

## 정리

Editor를 사용해서 작성 </br>
-> TypeScript Compiler</br>(Browser or Node.js 실행 환경에서 이해하고 사용할 수 있는 Plain Javascripte로 변경)</br>
-> Browser, Node.js

## 설치

실행환경인 Browser(Chrome)와 Node.js가 설치되어있어야한다.
- `npm init -y`
- `npm i typescript -D`
- `npx tsc --init` : Typescript에서 compile하는 옵션
  - tsconfig.json 파일 생성
- `.ts` : 확장자명
- `npm tsc` : 모든 ts 파일이 config에 맞춰 Compile

## Typescript Types VS Javascript Types

Typescript Types | Javascript Types
:--:|:--:
Static Types | Dynamic Types
set during development | reslolved at runtime
개발 중간에 타입 체크 | 런타임에 돌입해야만 알 수 있다

- 프로그램이 유용하려면, 가장 간단한 데이터 단위로 작업 할 수 있어야합니다.
  - numbers, strings, structures, boolean 값 등등
- TypeScript에서, 우리는 JavaScript에서 기대하는 것과 동일한 타입을 지원하며, 돕기 위해 추가적인 열거 탑입이 제공되었습니다.
- Typescript에서 프로그램 작성을 위해 기본 제공하는 데이터 타입
- 사용자가 만든 타입은 결국은 이 기본 자료형들로 쪼개집니다.
- JavaScript 기본 자료형을 포함(superset)
  - ECMAScript 표준에 따른 기본 자료형은 6가지
    - Boolean
    - Number
    - String
    - Null
    - Undefined
    - Symbol(ECMAScript 6에 추가)
    - Array : object형
- 프로그래밍을 도울 몇가지 타입이 더 제공된다.
  - Any, Void, Never, Unknown
  - Enum
  - Tuple : object형
