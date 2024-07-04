## 💭 Router

라우터는 브라우저에서 웹 페이지 이동 간에 화면 상 깜빡거림 없이 매끄럽게 화면을 전환할 수 있는 기능을 제공한다. <br>
URL 변경 시 DOM을 새로 갱신하는 것이 아니라 미리 컴포넌트를 가지고 있다가 변경된 요소의 영역만 갱신하기 때문에 유연한 페이지 전환이 가능하다. <br>
(*SPA 언어의 큰 특징!*) <br>

<br> 

> SPA 어플리케이션에선 라우팅 기능을 주로 사용하고, vue 프레임워크에서는 vue-router라는 라우팅 라이브러리를 지원한다.

#### 🏷️ 라우터 태그

- &lt;router-link to="URL"&gt; : 페이지 이동 태그 &lt;a&gt;와 동일
- &lt;router-view&gt; : 라우터의 컴포넌트가 보여지는 영역

#### 💡 간단한 예제
```html
<!-- App.vue -->
<template>
  <div id="app">
    <nav>
      <router-link to="/componentA">componentA</router-link> |
      <router-link to="/componentB">componentB</router-link>
    </nav>
    <h1>Router Test</h1>
    <router-view></router-view>
  </div>
</template>

<script>
export default {}
</script>

<style>
</style>
```
➡️ router-link는 a 태그로 렌더링 되며, to 속성에 지정한 url로 이동한다. <br>
tag 속성을 통해 다른 tag로 변경이 가능하다. (예, tag='div'로 하면 div로 생성)

➡️ router-view는 현재 라우터에 맞는 컴포넌트가 렌더링 된다. <br>

```js
// main.js
import { createApp } from 'vue'
import App from './App.vue'

import router from "./router" 

createApp(App).use(router).mount('#app') 
```

```js
// router.js
import { createWebHistory, createRouter } from "vue-router";


import componentA from "@/components/componentA"
import componentB from "@/components/componentB"


const routes = [
    { path : "/componentA", name : "componentA", component : componentA },
    { path : "/componentB", name : "componentB", component : componentB },
]

const router = createRouter({
    history : createWebHistory(),
    routes : routes
});

export default router;
```

```html
<!-- componentA -->
<template>
    <h1>componentA 페이지</h1>
</template>

<script>
  export default {}
</script>
  
<style>
</style>

<!-- componentB -->
<template>
    <h1>componentB 페이지</h1>
</template>

<script>
  export default {}
</script>
  
<style>
</style>
```

#### 💡 실행 화면
<img src="https://github.com/yejinsohn/TIL/assets/104317217/ab9c05d9-8785-4c5c-a45a-26e0a91827e7" width="400" height="150"/>
<br>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/1576c525-8b90-49aa-9968-604adb09be94" width="400" height="150"/>
<img src="https://github.com/yejinsohn/TIL/assets/104317217/fda683c9-bc4e-44fe-a2a6-049ac2c3ae8c" width="400" height="150"/>
