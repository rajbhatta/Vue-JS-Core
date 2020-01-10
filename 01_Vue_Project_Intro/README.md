## Introduction to Vue JS Projet ##


**public/index.html:** This is the first file that loads when the application starts. Also, this file has the following code snippet <div id=”app”></div>. All the components are loaded within this div with id app.

**src/main.js:** This is the file where the Vue Instance is created. This file has the following code snippet new Vue({ render: h => h(App)}).$mount(‘#app’). This snippet is telling that App Component needs to be loaded into an element with id app (which is the div element).

**src/App.vue:** This file corresponds to the App component which acts as a container to all other components. It has a template for the HTML code, it has a script for the JavaScript code, and it has a style for CSS.
