## 1. How to include one component inside another component in VueJs? ##
- Say we do have HelloWorld.vue component located inside src/components/HelloWorld.vue
- In another component located inside src/App.vue
- We can import HelloWorld.Vue inside the script tag in App.Vue and use it
```js
<template>
  <HelloWorld></HelloWorld>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>
```

<img src="img/img1.png" />