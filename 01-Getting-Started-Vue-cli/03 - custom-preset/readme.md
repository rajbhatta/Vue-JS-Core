## How to custom preset Vuejs project? ##
- Custom preset allow us to create our own custom project with required file

## 1. How to create custom VueJS project? ##
- goto terminal and type vue create raj-custom
<img src="images/img1.png" />

## 2. Select project manally ##
<img src="images/img2.png" />

## 3. Select the fatures that you need ##
<img src="images/img3.png" />

## 4. Select css processor ##
<img src="images/img4.png" />
-don't forget to select browser history

## 5. Select linter and formatting ##
<img src="images/img5.png" />

-lintter will lint the project on the basis of commit or save
<img src="images/img6.png" />


## Save project for the future ##
<img src="images/img7.png">

- we can extract this preset from CLI later 

# Diagnosis of the project #

## 1. babel.config.js ##
- The babel.config.js allows to use the next generation javascript feature which is not currently supported by some browser.

package.json has

```js
"browserlist": ["
                    > 1%
                    last 2 versions
                    not dead
                "]
```

In this case this file is located inside browserlistrc

