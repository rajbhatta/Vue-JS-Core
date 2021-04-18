## Passing value from parent component to child component ##
- we can pass value from parent component to child component using <b><span>props</span></b>

<img src="img/img1.png" />
- Tips for using props

<img src="img/img2.png" />
- Validation in props

<img src="img/img3.png" />
- Custom validation in props

## Short cut for creating props in Vue component ##
<img src="img/img4.png" />
- shortcut for creating props

<img src="img/img5.png" />
- provide name for props

<img src="img/img6.png" />
- Define the type of the prop

<img src="img/img7.png" />
- It is object

<img src="img/img8.png" />
- default implementation is object

# 1. Passing value from parent component to child component in VueJs - Option 1#
- Within the template  section of the parent component, <b>Heros.vue in our case</b>, call the child component. Prop data is passed as an attribute.

```js
<template>
    <div>
        <Header></Header>
    </div>
    <div>
        <HeroDetail></HeroDetail>
    </div>
    <div>
        <HeroList titleChild="This title is for child sent from parent"></HeroList> // This one nothing else is needed.
    </div>
</template>

<script>
import Header from './Header.vue'
import HeroDetail from './Hero-detail.vue'
import HeroList from './Hero-list.vue'

    export default {
        name:'Heros',
        components:{Header,HeroDetail,HeroList}
    }
</script>

<style lang="scss" scoped>

</style>
```

## 1.2 How to receive and bind in child ##
- we must declare attribute passed from parent in the prop section as given below:

```js
props:{
    attributeName: typeOfAttribute
}

or

props:{
    titleChild:String
}
```

### 1.2.1 Example ###
```js
<template>
    <div>
        <p>Property 1: {{titleChild}}</p>
        <p>Property 2: </p>
        <p>Property 3: </p>
        <p>Property 4: </p>
    </div>
</template>

<script>
    export default {
        name:'HeroList',
        props: {
            titleChild: String,
        },
    }
</script>

<style lang="scss" scoped>

</style>
```