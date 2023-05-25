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

전 세계의 개발자들이 만든 다양한 기능(패키지, 모듈)들을 관리
