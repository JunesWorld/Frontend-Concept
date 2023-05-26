# Node.js

Chrome V8 JavaScript 엔진으로 빌드된 JavaScript 런타임(=프로그래밍 언어가 동작하는 환경)

## 동작하는 환경
- 컴퓨터
- 브라우저

## 사용하는 이유
웹브라우저에서는 HTML / CSS / JS 만 가지고 동작한다.  
하지만, 비효율적이기 때문에 여러가지 모듈들을 설치해서 개발해야한다.  
모듈들은 웹브라우저에서 동작하지 않기때문에 Node.js환경의 도움을 받아  
HTML/CSS/JS 변환을 해주기 위해 사용한다.

## NVM(Node Version Manager) : 버전 관리
1. Google 검색 -> nvm-sh/nvm(Github)
2. Installing and Updating
3. curl 코드 복사 후 설치!
> Windows Install!
>  > nvm-windows 검색 -> coreybutler/nvm-widows(Github)
>  > Download Now!
>  > nvm-setup.zip 파일 다운 후 설치!
4. 사용법
  - Terminal에서 설치 확인 
    ```bash
    $ nvm ls
    ```
  - Node.js LTS Version 확인 후 설치 및 사용
    ```bash
    $ nvm install [Version]
    $ nvm use [Version] // 변경시
    ```
  - Node.js 설치 확인
    ```bash
    $ node --version
    ```
  - Version 삭제
    ```
    $ nvm uninstall [Version]
    ```
    
## NPM(Node Package Manager)

전 세계의 개발자들이 만든 다양한 기능(패키지, 모듈)들을 관리. 
Node.js를 설치하면 자동으로 설치된다.  

- 실행
  ```bash
  $ npm init -y
  ```
  package.json 파일이 생성된다.
  `name` : 폴더 이름
  `main` : 현재의 project를 하나의 pkg처럼 만들어서 npm 생태계에 upload하기 위한 옵션
  `scripts` : 현재 프로젝트에서 사용할 수 있는 scripts 명령어 명시

- 설치
  pakage 설치(parcel-bundler & lodash) 
  - 개발용 의존성 패키지 설치 : 개발할 때만 필요하고 웹브라우저에서 동작할 때 필요하지 않을 때 사용
  ```bash
  npm install parcel-bundler -D
  ```
  - 일반 의존성 설치 : 실제로 웹브라우저에서 동작해야 할 때 사용
  ```bash
  npm install lodash
  ```
  - 설치가 되면 node-modules 폴더에 pkg(+필요한 pkg)가 들어간다.
  - `node_modules` 파일을 지우더라도 `npm i`를 사용하면 설치한 pkg 다시 생성

- `pakage.json` : 설치한 pkg 명시되어 있는 곳(직접 관리! & 삭제 X)
  - install 시 -D : `devDependencies`
  - install : `dependencies`

- `pakage-lock.json` : 설치한 pkg의 내부적으로 사용되는 pkg 정보(자동 관리! & 삭제 X)

## 사용해보기
- index.html & main.js 파일 생성
- index.html
  ```html
  <script src="./main.js"></script>
  ```
- main.js
  ```javascript
  console.log(hello world!);
  ```

## 유의적 버전(Semantic Versioning, SemVer)

12.14.1 (Major.Minor.Patch)
- Major : 기존 버전과 호환되지 않는 새로운 버전
- Minor : 기존 버전과 호환되는 새로운 기능이 추가된 버전
- Patch : 기존 버전과 호환되는 버그 및 오타 등이 수정된 버전

^Major.Minor.Patch : Major 버전 안에서 가장 최신 버전으로 업데이트 가능
