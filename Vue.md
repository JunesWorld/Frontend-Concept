# Vue.js

> Framework : Vue, React, Svelte, Angular

## CDN

```HTML
<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<div id="app">
  <h1>{{ message }}</h1>
</div>
```
```Javascript
Vue.createApp({
  // data = method
  data() { 
    return {
      message: 'Hello Vue!'
    }
  }
}).mount('#app')
```

## CLI(Command Line Interface)

```npm i -g @vue/cli```

```bash
cd [원하는 설치 경로]
vue create [생성을 원하는 파일 이름]
Default (Vue 3 Preview) 선택
cd [생성한 파일 이름]
npm run serve
code . -r
```

package.json/scripts
- serve = dev : 개발용 서버 open 할 때 사용
  > ```npm run serve```
- build : 제품화 과정
  > ```npm run build```
- lint : 코드를 작성하는 규칙
  > eslintConfig에 옵션에 명시되어 있고 필요한 규칙은 rules에 작성

기본적으로 Webpack을 사용하고 있다.

## 확장 프로그램 Vetur

Code 하이라이팅

## App.vue

- template = HTML
  > Helloworld Vue File(Component) 제거 후 Project 시작 
- script = Javascript
- style = CSS/SCSS

## Webpack을 기반으로 하는 Vue Project

webpack-template-basic 기반으로 시작
```bash
npx degit JunesWorld/webpack-template-basic vue3-webpack-template
```
