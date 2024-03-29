# TypeScript

= Language / Typed Superset of JavaScript
= compiles to plain(Browser or Node.js 실행 환경에서 이해할 수 있는) JavaScript

## Typed JavaScript at any Scale

- TypeScript extends JavaScript by adding types.
- By understanding JavaScript,  
TypeScript saves you time catching errors and providing fixes</br> 
before you run code.
- Any browser, anyOS, anywhere JavaScript runs. Entirely Open Source.

## 타입이란?

그 value가 가지고 있는 프로퍼티나 함수를 추론할 수 있는 방법이다.

"apple"
- string 문자열
- 이것은 value인데 문자열이 가지는 프로퍼티, 메소드를 가지고 있는 value입니다.
  ```js
  let string: string;
  'string'.length // 프로퍼티 : 문자열 길이 제공
  'string'.toLowerCase(); // 메소드 : 문자열에 작업을 수행한 다음 반환
  ```
  
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

## Primitive Type
- 오브젝트와 레퍼런스 형태가 아닌 실제 값을 저장하는 자료형입니다.
- 프리미티브 형의 내장 함수를 사용 가능한것은 자바스크립트 처리 방식 덕분
- ES2015 기준 6가지
  - boolean
  - number
  - string
  - symbol
  - null
  - undefined
- literal값으로 Primitive 타입의 서브 타입을 나타낼 수 있다.
  ```
  true;
  'hello';
  3.14;
  null;
  undefined;
  ```
- 또는, 래퍼 객체로 만들 수 있다.
  ```
  new Boolean(false); // typeof new Boolean(false) : 'object'
  new String('world'); // typeof new String('world') : 'object'
  new Number(42); // typeof new Number(42) : 'object'
  ```
- TypeScript의 핵심 Primitive Types는 모두 소문자!!

## 타입 시스템

- 컴파일러에게 사용하는 타입을 명시적으로 지정하는 시스템
- 컴파일러가 자동으로 타입을 추론하는 시스템
- TypeScript의 타입 시스템
  - 타입을 명시적으로 지정할 수 있다.
  - 타입을 명시적으로 지정하지 않으면, 타입스크립트 컴파일러가 자동으로 타입을 추론
```JS
// 타입이란 해당 변수가 할 수 있는 일을 결정합니다.
// f1이라는 함수의 body에서는 a를 사용하겠습니다.
// a가 할 수 있는 일은 a의 타입이 결정합니다.
function f1(a) {
  return a;
}

// 함수 사용법에 대한 오해를 야기하는 자바스크립트
// (f2 실행의 결과가 NaN을 의도한 것이 아니라면)
// 이 함수의 작성자는 매개변서 a가 number 타입이라는 가정으로 함수를 작성했습니다.
function f2(a) {
  return a * 38;
}
// 사용자는 사용법을 숙지하지 않은 채, 문자열을 사용하여 함수를 실행했습니다.
console.log(f2(10)); // 380
console.log(f2('Mark')); // NaN

// 타입스크립트의 추론에 의지하는 경우
// 타입스크립트 코드지만,
// a의 타입을 명시적으로 지정하지 않은 경우이기 때문에 a는 any로 추론
// 함수의 리턴 타입은 number로 추론 (NaN도 number의 하나)
function f3(a) {
  return a * 38;
}
// 사용자는 a가 any이기 때문에, 사용법에 맞게 문자열을 사용하여 함수를 실행
console.log(f3(10)); // 380
console.log(f3('Mark') + 5); // NaN
```
- noImplicitAny 옵션을 켜면 타입을 명시적으로 지정하지 않은 경우</br>
  타입스크립트가 추론 중 any라고 판단하게 되면 컴파일 에러를 발생시켜 명시적으로 지정하도록 유도
  ```JS
  // Error: Parameter 'a' implicitly has an 'any' type.
  function f3(a) {
    return a * 38;
  }
  // 사용자의 코드를 실행할 수 없습니다. 컴파일이 정상적으로 마무리 될 수 있도록 수정해야 합니다.
  console.log(f3(10)); 
  console.log(f3('Mark') + 5); 
- number 타입으로 추론된 리턴 타입 
  - number안에 undefined가 포함되어 있다.
  - strictNullChecks 옵션을 켜야한다. 
  ```JS
  // 매개변수의 타입은 명시적으로 지정
  // 명시적으로 지정하지 않은 함수의 리턴 타입은 number로 추론
  function f4(a: number) {
    if (a > 0) {
      return a * 38;
    }
  }
  // 사용자는 사용법에 맞게 숫자형을 사용하여 함수를 실행했습니다.
  // 해당 함수의 리턴 타입은 number이기 때문에, 타입에 따르면 이어진 연산을 바로 할 수 있다.
  // 하지만, 실제 undefined + 5가 실행되어 NaN이 출력
  console.log(f4(5)); // 190
  console.log(f4(-5) + 5); // NaN
- strictNullChecks 옵션을 켜면 모든 타입에 자동으로 포함되어 있는 `null`과 `undefined`를 제거
  - number | undefined 타입으로 추론된 리턴 타입
  ```JS
  // 매개변수의 타입은 명시적으로 지정
  // 명시적으로 지정하지 않은 함수의 리턴 타입은 number | undefined로 추론
  function f4(a: number) {
    if (a > 0) {
      return a * 38;
    }
  }
  // 사용자는 사용법에 맞게 숫자형을 사용하여 함수를 실행했습니다.
  // 해당 함수의 리턴 타입은 number | undefined이기 때문에, 타입에 따르면 이어진 연산을 바로 할 수 없다.
  // 컴파일 에러를 고쳐야하기 때문에 사용자와 작성자가 의논해야함
  console.log(f4(5)); 
  console.log(f4(-5) + 5); // Error: Object is possibly 'undefined' 
  ```
- 명시적으로 리턴 타입을 지정해야할까?
```JS
// 실제 함수 구현부의 리턴 타입과 명시적으로 지정한 타입이 일치하지 않아 컴파일 에러 발생
// Error: Function lacks ending return statement and return type does not incorrect.
function f5(a: number): number {
  if (a > 0) {
    return a * 38;
  }
}
```
- noImplicitReturns 옵션을 켜면, 함수 내에서 모든 코드가 값을 리턴하지 않으면, 컴파일 에러 발생시킨다.
  - 모든 코드에서 리턴을 직접해야 한다.
  - if문과 아닌 경우 모두 return 해줘야 한다!!
  ```JS
  // if가 아닌 경우 return을 직접 하지 않고 코드가 종료
  // Error: Not all code paths return a value.
  function f5(a: number) {
    if (a > 0) {
      return a * 38;
    }
  }
  ```
- 매개변수에 object가 들어오는 경우
  - object literal type을 사용하면 되지만 길어진다. 그래서 나만의 타입을 만들어 사용
  - 나만의 타입을 만드는 방법
    ```JS
    interface PersonInterface {
      name: string;
      age: number;
    }
    type PersonTypeAlias = {
      name: string;
      age: number;
    };
    function f8(a: PersonInterface): string {
      return `이름은 ${a.name}이고, 연령대는 ${Math.floor(a.age / 10) * 10}대 입니다.`;
    }
    console.log(f8({ name: 'Mark', age: 38 })); // 이름은 Mark 이고, 연령대는 30대 입니다.
    console.log(f8('Mark')); // Error: Argument of type 'string' is not assignable to parameter of type 'PersonInterface'

## Structural Type System VS Nominal Type System

- TypeScript는 duck typing이 아니다.
  - duck typing
    - 만약 어떤 새가 오리처럼 걷고, 헤엄치고, 꽥괙 소리를 낸다면 나는 그 새를 오리라고 부를 것이다.
    - python이 대표적

- Structural Type System : 구조가 같으면 같은 타입이다.
  - Typescript
  ```JS
  interface IPerson {
    name: string;
    age: number;
    speak(): string;
  }
  
  type PersonType {
    name: string;
    age: number;
    speak(): string;
  }
  
  let personInterface: IPerson = {} as any;
  let personType: PersonType = {} as any;
  
  personInterface = personType;
  personType = personInterface;
  ```

- Nominal Type System : 구조가 같아도 이름이 다르면, 다른 타입이다.
  - C언어, Java
  ```JS
  type PersonID = string & { readonly brand: unique symbol };
  
  function PersonID(id: string): PersonID {
    return id as PersonID;
  }
  
  function getPersonById(id: PeersonID) {}
  
  // PersonID로 치환된 형태만 넣을 수 있게 한다.
  getPersonById(PersonID('id-aaaaaa'));
  getPersonById('id-aaaaaa'); // ERROR
  ```

## 타입 호환성(Type Compatibility)

- 서브 타입
  - 공변 : 같거나 서브 타입인 경우, 할당이 가능하다.
  - 반병 : 함수의 매개변수 타입만 같거나 슈퍼타입인 경우, 할당이 가능하다.
  ```JS
  // sub1 타입은 sup1 타입의 서브 타입이다.
  // object = primitive type이 아닌 것
  // sub1은 sup1의 하위 타입이기 때문에 할당 할 수 없다.
  let sub1: number[] = [1]; // Array
  let sup1: object = sub1;
  sub1 = sup1; // Error
  ```
  
## 타입 별칭(Type Alias)

- Interface와 비슷해보인다.
  - Interface : Type으로써 목적 or 존재가치가 명확할 때 사용
  - Alias : 단순히 가리키거나 별명으로써 사용
- Primitive, Union Type, Tuple, Function
- 기타 직접 작성해야하는 타입을 다른 이름을 지정할 수 있습니다.
- 만들어진 타입의 refer로 사용하는 것이지 타입을 만드는 것은 아닙니다.
- Aliasing Union Type
  ```JS 
  let person: string | number = 0;
  person = 'Mark';
  
  type StringOrNumber = string | number;
  
  let another: StringOrNumber = 0;
  another = 'Anna';
  
- Aliasing Tuple
  ```JS
  let person: [string, number] = ['Mark', 35];
  type PersonTuple = [string, number];
  let another: PersonTuple = ['Anna', 24];
  ```
  
- Aliasing Function
  ```JS
  type EatType = (food: string) => void;
  ``` 
