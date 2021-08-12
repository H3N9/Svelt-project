# SveltJS

it's smallest bundle lib.

this project is playground for my pratices.
if you require scss type, following this https://codepilotsf.medium.com/svelte-sapper-with-sass-271fff662da9
 or follow this step.

 Install svelte-preprocess autoprefixer node-sass as devDependency
```
 yarn add -D svelte-preprocess autoprefixer node-sass
```
so in file rollup.config.js add
```
import sveltePreprocess from 'svelte-preprocess';
const preprocess = sveltePreprocess({
  scss: {
    includePaths: ['src'],
  },
});
```

so add into plugin
```
export default {
  client: {
    plugins: [
      svelte({
        // ...
        preprocess, // <-- ADD THIS LINE
      }),
  },
  server: {
    plugins: [
      svelte({
       // ...
        preprocess, // <-- HERE TOO
      }),
    ],
  },
};
```
create file svelte.config.js
```
const sveltePreprocess = require('svelte-preprocess');
module.exports = {
  preprocess: sveltePreprocess({
    scss: {
      includePaths: ['src'],
    },
    postcss: {
      plugins: [require('autoprefixer')],
    },
  }),
};
```

but if we need to hightlight syntax
add in preprocess in svelte.config.js and
install this postcss
```
yarn add -D postcss
```
```
postcss: {
    plugins: [require('autoprefixer')],
},
```