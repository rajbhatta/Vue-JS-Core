## How Vue App Starts ? ##
## 1. Main.js (src/main.js) ##
```js
import Vue from 'vue';
import App from '@/app';

Vue.config.productionTip = false;

new Vue({
  render: h => h(App),
}).$mount('#app');
```

- First inside main.js we created first instance of Vue.js. 
- Taking the App (which is App component) and mounting to the ID (#app) which is div in index.html

## 2. Index.html (public/index.html) ##
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width,initial-scale=1.0" />
    <link rel="icon" href="<%= BASE_URL %>favicon.ico" />
    <link
      rel="stylesheet"
      href="https://use.fontawesome.com/releases/v5.4.1/css/all.css"
      integrity="sha384-5sAR7xN1Nv6T6+dT2mhtzEpVJvfS3NScPQTrOxhwjIuvcA67KV2R5Jz6kr4abQsz"
      crossorigin="anonymous"
    />
    <title>Vue Heroes</title>
  </head>
  <body>
    <noscript>
      <strong
        >We're sorry but vue-heroes doesn't work properly without JavaScript
        enabled. Please enable it to continue.</strong
      >
    </noscript>
    <div id="app"></div>
    <!-- built files will be auto injected -->
  </body>
</html>
```
- public folder contains the index.html

## 3. App.Vue (src) ##
```js
<template>
  <div id="app">
    <HeaderBar />
    <div class="main-section content-title-group">
      <h2 class="title">Heroes</h2>
      <div>We'll start here</div>
    </div>
  </div>
</template>

<script>
import HeaderBar from '@/components/header-bar';

export default {
  name: 'App',
  components: { HeaderBar },
};
</script>

<style lang="scss">
@import '@/design/index.scss';
</style>
```

- Inside the app.vue we are using another component: HeaderBar

## 4. header-bar.vue (src/components/header-bar.vue) ##
```js
<template>
  <header>
    <nav
      class="navbar has-background-dark is-dark"
      role="navigation"
      aria-label="main navigation"
    >
      <HeaderBarBrand></HeaderBarBrand>
      <HeaderBarLinks></HeaderBarLinks>
    </nav>
  </header>
</template>

<script>
import HeaderBarBrand from '@/components/header-bar-brand';
import HeaderBarLinks from '@/components/header-bar-links';

export default {
  name: 'HeaderBar',
  components: { HeaderBarBrand, HeaderBarLinks },
};
</script>

<style lang="scss" scoped>
.foo{
  color:white:
}
</style>

```

- Inside headerbar we are using header-bar-brand and header-bar-link components.
- Scoped means this css is scoped for this component only.

## 5. header-bar-link (src/components/header-bar-link) ##
```js
<template>
  <div class="navbar-menu">
    <div class="navbar-end">
      <div class="navbar-item">
        <div class="buttons">
          <a :href="github" target="_blank" rel="noopener noreferrer">
            <i class="fab fa-github fa-2x" aria-hidden="true"></i>
          </a>
          <a :href="twitter" target="_blank" rel="noopener noreferrer">
            <i class="fab fa-twitter fa-2x" aria-hidden="true"></i>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      github: 'https://github.com/johnpapa/vue-getting-started',
      twitter: 'https://twitter.com/john_papa',
    };
  },
};
</script>
```

## 6. header-bar-brand (src/components/header-bar-brand.vue) ##
```js
<template>
  <div class="navbar-brand">
    <a
      class="navbar-item"
      href="https://vuejs.org/"
      target="_blank"
      rel="noopener noreferrer"
    >
      <i class="fab js-logo fa-vuejs fa-2x" aria-hidden="true" />
    </a>
    <div class="navbar-item nav-home">
      <span class="tour">TOUR</span>
      <span class="of">OF</span>
      <span class="heroes">HEROES</span>
    </div>
    <button
      class="link navbar-burger burger"
      aria-label="menu"
      aria-expanded="false"
      data-target="navbarBasicExample"
    >
      <span aria-hidden="true" />
      <span aria-hidden="true" />
      <span aria-hidden="true" />
    </button>
  </div>
</template>
```