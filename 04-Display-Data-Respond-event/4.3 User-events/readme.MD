## User event in VueJs ##

v-on is the attribute added to the DOM elements to listen to the events in VueJS.

Click Event
Example
```js
<html>
   <head>
      <title>VueJs Instance</title>
      <script type = "text/javascript" src = "js/vue.js"></script>
   </head>
   <body>
      <div id = "databinding">
         <button v-on:click = "displaynumbers">Click ME</button>
         <h2> Add Number 100 + 200 = {{total}}</h2>
      </div>
      <script type = "text/javascript">
         var vm = new Vue({
            el: '#databinding',
            data: {
               num1: 100,
               num2 : 200,
               total : ''
            },
            methods : {
               displaynumbers : function(event) {
                  console.log(event);
                  return this.total =  this.num1+ this.num2;
               }
            },
         });
      </script>
   </body>
</html>
```

The following code is used to assign a click event for the DOM element.
```js
<button v-on:click = "displaynumbers">Click ME</button>
```
There is a shorthand for v-on, which means we can also call the event as follows −

```js
<button @click = "displaynumbers">Click ME</button>
```

On the click of the button, it will call the method ‘displaynumbers’, which takes in the event and we have consoled the same in the browser as shown above.

We will now check one more event mouseover mouseout.

Example
```js
<html>
   <head>
      <title>VueJs Instance</title>
      <script type = "text/javascript" src = "js/vue.js"></script>
   </head>
   <body>
      <div id = "databinding">
         <div v-bind:style = "styleobj" v-on:mouseover = "changebgcolor" v-on:mouseout = "originalcolor"></div>
      </div>
      <script type = "text/javascript">
         var vm = new Vue({
            el: '#databinding',
            data: {
               num1: 100,
               num2 : 200,
               total : '',
               styleobj : {
                  width:"100px",
                  height:"100px",
                  backgroundColor:"red"
               }
            },
            methods : {
               changebgcolor : function() {
                  this.styleobj.backgroundColor = "green";
               },
               originalcolor : function() {
                  this.styleobj.backgroundColor = "red";
               }
            },
         });
      </script>
   </body>
</html>
```
In the above example, we have created a div with width and height as 100px. It has been given a background color red. On mouseover, we are changing the color to green, and on mouseout we are changing the color back to red.

Hence, during mouseover, a method is called changebgcolor and once we move the mouse out of the div, a method is called originalcolor.

This is done as follows −
```js
<div v-bind:style = "styleobj" v-on:mouseover = "changebgcolor" v-on:mouseout = "originalcolor"></div>
```

Two events - mouseover and mouseout - is assigned to the div as shown above. We have created a styleobj variable and given the required style to be assigned to the div. The same variable is binded to the div using v-bind:style = ”styleobj”

In changebgcolor, we are changing the color to green using the following code.
```js
changebgcolor : function() {
   this.styleobj.backgroundColor = "green";
}
```
Using the stylobj variable, we are changing the color to green.

Similarly, the following code is used to change it back to the original color.
```js
originalcolor : function() {
   this.styleobj.backgroundColor = "red";
}
```