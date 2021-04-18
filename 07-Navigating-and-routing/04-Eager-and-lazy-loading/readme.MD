## 1. Eager and Lazy loading ##

```js

LAZY LOADING

{
    path: '/about',
    name: 'About',
    // route level code-splitting
    // this generates a separate chunk (about.[hash].js) for this route
    // which is lazy-loaded when the route is visited.
    component: () => import(/* webpackChunkName: "about" */ '../views/About.vue')
  }
```

```js

EAGER LOADING

{
    path: '/hero',
    name: 'Hero',
    component: () => import(/* webpackChunkName: "about" */ '../views/components/Heros.vue')
  }
```