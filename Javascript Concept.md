# JavaScript : 개발자(동적)
 - 콘텐츠를 바꾸고 움직이는 등 페이지를 동작시키는 동적 처리를 담당
 - 작성방법
    > ``` Console.log(‘console에 찍힐 내용’); ```
 - 표기법
    - dash-case(kebab-case)
    - snake_case
    - camelCase
    - ParcelCase
 - Zero-based Numbering
    - 0기반 번호 매기기!
    - 특수한 경우를 제외하고 0부터 숫자를 시작
 - 주석(Comments) : Cmd + /
    - 한 줄 메모 : // or /* */
    - 여러 줄 메모
      ```
      /**
       * 여러 줄
       * 메모1
       * 메모2
       * /
      ```
 - 데이터 종류 : let = 변수선언
    - index.html
      ```
      <head>
      <script src="./main.js"></script>
      </head>
      ```
    - main.js
      ```
      // String(문자 데이터)
      // 따옴표를 사용합니다.
      let myName = "June";
      let email = 'june@gmail.com';
      (보간법=다른 데이터를 넣는 것) let hello = `Hello ${myName}?!`
   
      console.log(myName); // June
      console.log(email); // june@gmail.com
      console.log(hello); // Hello June?!
      ```
      ```
      // Number(숫자 데이터)
      // 정수 및 부동 소수점 숫자를 나타냅니다.
      // 따옴표로 묶여 있으면 문자 데이터
      let number = 123;
      let opacity = 1.57;
   
      console.log(number); // 123
      console.log(opacity) // 1.57
      ```
      ```
      // Boolean
      // true, false
      let checked = true;
      let isShow = false;

      console.log(checked); // true
      console.log(isShow); // false
      ```
      ```
      // Undefined
      // 값이 할당되지 않은 상태를 나타냅니다.
      let undef;
      let obj = { abc: 123 };

      console.log(undef); // undefined
      console.log(obj.abc); // 123
      console.log(obj.xyz); // undefined
      ```
      ```
      // Null
      // 어떤 값이 "의도적으로" 비어있음을 의미
      let empty = null;

      console.log(empty); // null
      ```
      ```
      // Object(객체 데이터)
      // 여러 데이터를 Key:Value 형태롤 저장. { }
      let user = {
       // Key : Value
      name: 'June',
       age: 30,
       isValid: true
      };

      console.log(user.name); // June
      console.log(user.age); // 30
      console.log(user.isValid); // true
      ```
      ```
      // Array(배열 데이터)
      // 여러 데이터를 순차적으로 저장. [ ]
      let fruits = ['Apple', 'Bannana', 'Cherry'];

      console.log(fruits[0]); // 'Apple'
      console.log(fruits[1]); // 'Bannana'
      console.log(fruits[2]); // 'Cherry'
      ```
 - 변수 : 데이터를 저장하고 참조(사용)하는 데이터의 이름
    - var, let(추천!), const(추천!)
    - 보통은 재할당이 불가능한 const 사용하고, 재할당이 필요한 경우 let으로 변경하여 사용
      ```
      // 재사용이 가능!
      // 변수 선언!
      let a = 2;
      let b = 5;
      
      console.log(a + b); // 7
      console.log(a - b); // -3
      console.log(a * b); // 10
      console.log(a / b); // 0.4
      
      // 값(데이터)의 재할당 불가! = const / let(재할당 가능)
      const(a) = 12;
      console.log(a); // 12
      
      a = 999;
      console.log(a); // TypeError: Assignment to constant variable.
      ```
 - 예약어 : 특별한 의미를 가지고 있어, 변수나 함수 이름 등으로 사용할 수 없는 단어
    - Editor가 판별해줌!
      ```
      let this = 'Hello!'; // SyntaxError
      let if = 123; // SyntaxError
      let break = true; // SyntaxError
      ```

 - 함수 : 특정 동작(기능)을 수행하는 일부 코드의 집합(부분)
      ```
      function helloFunc() {
        // 실행 코드
        console.log(1234);
      }
      
      // 함수 호출
      helloFunc(): // 1234
      
      ---
      
      function returnFunc() {
        return 123;
      }
      
      let a = returnFunc();
      
      console.log(a); // 123
      ---
      
      // 함수 선언!
      function sum(a,b) { // a와 b는 매개변수(Parameters)
        return a + b;
      }
      
      // 재사용!
      let a = sum(1, 2); // 1과 2는 인수(Arguments)
      let b = sum(7, 12);
      let c = sum(2, 4);
      
      console.log(a, b, c); // 3, 19, 6
      ---
      
      // 기명(이름이 있는) 함수
      // 함수 선언!
      function hello() {
        console.log('Hello~');
      }
      
      // 익명(이름이 없는) 함수
      // 함수 표현!
      let world = function () {
        console.log('World~');
      }
      
      // 함수 호출!
      hello(); // Hello~
      world(); // World~
      
      ---
      
      // 객체 데이터
      const june = {
        name: 'JUNE',
        age: 85,
        // 메소드(Method)
        getName: function () {
          return this.name;
        }
      };
      
      const hisNmae = june.getName();
      console.log(hisName); // JUNE
      // 혹은
      console.log(june.getName()); // JUNE
       
      ```
 - 조건문 : 조건의 결과(truthy, falsy)에 따라 다른 코드를 실행하는 구문(if, else)
      ```
      let isShow = true;
      let checked = false;
      
      if (isShow) {
        console.log('Show!'); // Show!
      }
      
      if (checked) {
        console.log('Checked!');
      }
      ```

 - DOM API : JavaScript로 HTML을 제어하는 여러가지 명령
    - DOM = Document Object Model
      - Document = HTML
      - Object Modle = div / sapn / input
    - Application Programming Interface : 웹 사이트가 동작하기 위한 프로그래밍 명령
    ```
    // HTML 요소(Element) 1개 검색/찾기
    // HTML 검색하는 메소드 = querySelector
    const boxEl = document.querySelector('.box');
    
    // HTML 요소에 적용할 수 있는 메소드!
    boxEl.addEventListener();
    
    // 인수(Arguments=1,2)를 추가 기능!
    boxEl.addEventListener(1, 2);
    
    // 참고) 매개변수(Parameters)
    // 아래 함수 선언의 a, b와 같이 함수 호출에서 전달받은 인수를 함수 내부로 전달하기 위한 변수
    function sum(a, b) {
      return a + b;
    }
    
    // 1 - 이벤트(Event, 상황)
    boxEl.addEventListener('click', 2);
    
    // 2 - 핸들러(Handler, 실행할 함수) = function
    // addEventListener Method가 click이라는 Event 발생하면 function 실행
    boxEl.addEventListener('click', function () {
      console.log('Click~!);
    });
    ```
    ```
    // HTML 요소(Element) 검색/찾기
    const boxEl = document.querySelector('.box');
    
    // 요소의 클래스 정보 객체 활용!
    // add Method
    boxEl.classList.add('active');
    let isContains = boxEl.classList.contains('active');
    console.log(isContains); // true
    
    // remove Method
    boxEl.classList.remove('active');
    isContains = boxEl.classList.contains('active');
    console.log(isContains); // false
    ```
    ```
    // HTML 요소(Element) 모두 검색/찾기
    // Els / All -> box 여러 개 & 모두 찾겠다
    // 유사 배열
    const boxEls = document.querySelectorAll('.box');
    console.log(boxEls);
    
    // 찾은 요소들 반복해서 함수 실행!
    // 익명 함수를 인수로 추가!
    boxEls.forEach(function () {});
    
    // 첫 번째 매개변수(boxEl): 반복 중인 요소
    // 두 번째 매개변수(index): 반복 중인 번호
    boxEls.forEach(function (boxEl, index) {});
    
    // 출력!
    boxEls.forEach(function (boxEl, index) {
      boxEl.classList.add(`order-${index + 1});
      console.log(index. boxEl);
    });
    ```
    ```
    const boxEl = document.querySelector('.box');
    
    // Getter, 값을 얻는 용도
    console.log(boxEl.textContent); // Box!!
    
    // Setter, 값을 지정하는 용도
    box.textContent = 'JUNE?!';
    console.log(boxEl.textContent); // JUNE?!
    ```

 - 메소드 체이닝
    ```
    const a = 'Hello';
    // split: 문자를 인수 기준으로 쪼개서 배열로 반환
    // reverse: 배열을 뒤집기
    // join: 배열을 인수 기준으로 문자로 병합해 반환
    const b = a.split('').reverse().join(''); // 메소드 체이닝
    
    console.log(a); // Hello~
    console.log(b); // ~olleH
    ```
