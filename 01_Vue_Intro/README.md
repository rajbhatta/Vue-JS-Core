## Introuduction to Vue JS component ##

**public/index.html:** This is the first file that loads when the application starts. Also, this file has the following code snippet <div id=”app”></div>. 
All the components are loaded within this div with id app.


**src/main.js:** This is the file where the Vue Instance is created. This file has the following code snippet new Vue({ render: h => h(App)}).$mount(‘#app’). This snippet is telling that App Component needs to be loaded into an element with id app (which is the div element).

**src/App.vue:** This file corresponds to the App component which acts as a container to all other components. It has a template for the HTML code, it has a script for the JavaScript code, and it has a style for CSS.

**src/components:** This is where all the components you develop will be stored. All the components will have a template, script, and style tags for HTML, JavaScript, and CSS code respectively.

### Types of component registration and naming convention in VUE JS ###
**Naming convention**
With kebab-case
```js
Vue.component('my-component-name', { /* ... */ })
```
When defining a component with kebab-case, you must also use kebab-case when referencing its custom element, such as in <my-component-name>.

With PascalCase
```js
Vue.component('MyComponentName', { /* ... */ })
```
When defining a component with PascalCase, you can use either case when referencing its custom element. That means both 
```html
<my-component-name> and <MyComponentName>
```
are acceptable.

### Global component in Vue JS
So far, we’ve only created components using Vue.component:
```js
Vue.component('my-component-name', {
  // ... options ...
})
```
These components are globally registered. That means they can be used in the template of any root Vue instance (new Vue) created after registration. For example:
```js
Vue.component('component-a', { /* ... */ })
Vue.component('component-b', { /* ... */ })
Vue.component('component-c', { /* ... */ })

new Vue({ el: '#app' })
```
```js
<div id="app">
  <component-a></component-a>
  <component-b></component-b>
  <component-c></component-c>
</div>
```
### Example ###
```html
<div id="app">
	<contact-us></contact-us>
</div>
```
```js
Vue.component('contact-us', {
	data: function() {
		return {
			email: 'info@mycompany.com'
		};
	},
	template: `
		<div>
			<h1>Contact Us</h1>
			<p>Please send an e-mail to: {{ email }}</p>
		</div>
	`
});


new Vue({
	el: '#app',
});

```
This component is actually a global component, because we registered it with the component method on the global Vue object.

### Local Registration ###
In these cases, you can define your components as plain JavaScript objects:
```js
var ComponentA = { /* ... */ }
var ComponentB = { /* ... */ }
var ComponentC = { /* ... */ }
```
Then define the components you’d like to use in a components option:
```js
new Vue({
  el: '#app',
  components: {
    'component-a': ComponentA,
    'component-b': ComponentB
  }
})
```
For each property in the components object, the key will be the name of the custom element, while the value will contain the options object for the component.

Note that locally registered components are not also available in subcomponents. For example, if you wanted ComponentA to be available in ComponentB, you’d have to use:
```js
var ComponentA = { /* ... */ }

var ComponentB = {
  components: {
    'component-a': ComponentA
  },
  // ...
}
```
Or if you’re using ES2015 modules, such as through Babel and Webpack, that might look more like:
```js
import ComponentA from './ComponentA.vue'

export default {
  components: {
    ComponentA
  },
  // ...
}
```

### Example ###
var contactUs = {
	data: function() {
		return {
			email: 'info@mycompany.com'
		};
	},
	template: `
		<div>
			<h1>Contact Us</h1>
			<p>Please send an e-mail to: {{ email }}</p>
		</div>
	`
};
Then within the Vue instance, we can add a components property with the components that we want to register locally. This property should be an object and contain key-value pairs of tag names and configuration objects.

new Vue({
	el: '#app',
	components: {
		'contact-us': contactUs
	}
});
Notice that in this example, I have added the components property to a Vue instance, but I could just as well have added it to another component.

If you were to run the code, you would see the component working. But just to prove that the component is indeed local and not globally available, I will add another Vue instance and change the selector of the existing one.

new Vue({
	el: '#app1',
	components: {
		'contact-us': contactUs
	}
});

new Vue({
	el: '#app2',
});
And then I will update the template to reflect these changes.

<div id="app1">
	<contact-us></contact-us>
</div>

<div id="app2">
	<contact-us></contact-us>
</div>
Now we only see the contact component being rendered once, even though we used the tag twice within the template.
