# BoilerPlate Theme Component Library
To house often reused component code for building basic theme boilerplates. Still in experimental state.

- build in SvelteKit.
- supports HTML, JQuery, (S)CSS and Svelte in single .svelte files.

**To add components**
- create a new file in 
~~~ 
src/lib/components/{folder of component type}.
~~~ 
- import it into 
~~~ 
src/routes/comp-sandbox.svelte
~~~

## To Install
~~~
$npm install  < make sure to use node v 16.4.2 using nvm >
~~~

## To Run
~~~
$ npm run dev
~~~

## To Close
~~~
ctrl + c
~~~

## Versions
- bootstrap 5.0.2
- Font Awesome 6.1.1 


**using:**
https://github.com/svelte-add/scss
https://github.com/svelte-add/svelte-add#readme


**usefull info on how module scripts work**
https://codechips.me/svelte-module-scripts-explained/

**embedding svelte apps into html**
https://codeandlife.com/2021/03/06/easy-to-embed-svelte-components/
https://www.youtube.com/watch?v=xIYOyiAE-sY


**usefull**
- to convert scss to css: https://www.sassmeister.com/
- to convert css to scss: https://beautifytools.com/css-to-scss-converter.php