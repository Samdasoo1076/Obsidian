---
tags:
  - "#vuejs"
  - "#공부"
date: 2024-07-03
---
#2024-07-03 #2024-07 #2024- [[2024-07-03]]

# 싱글 파일 컴포넌트 

Ex.
```vue.js
<template>
  <div class="my-component">
    <h1>{{ title }}</h1>
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    message: String
  }
};
</script>

<style scoped>
.my-component {
  color: blue;
}
</style>

```

## `<template>` : 컴포넌트의 HTML 구조를 정의
    1. 컴포넌트의 DOM 구조 정의
    2.
```vue.js
<template>
  <div class="my-component">
    <h1>{{ title }}</h1>
    <p>{{ message }}</p>
  </div>
</template>

```


`<script>`: 컴포넌트의 로직을 정의하는 부분

1. 데이터, 메소드 등을 정의
2. `props`를 사용하여 부모 컴포넌트로부터 값 받기 가능
3. 
```js
<script>
export default {
  props: {
    title: String,
    message: String
  }
};
</script>
```


`<style scoped>` : 컴포넌트의 스타일을 정의하는 부분
1. scoped` 속성을 사용하면 스타일이 해당 컴포넌트에만 적용됨
2.   
```css
<style scoped>
.my-component {
  color: blue;
}
</style>
```