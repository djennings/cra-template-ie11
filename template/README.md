# cra-template-ie11

This is an extension of the official base template for the create-react-app to offer base support for IE 11.

Specify the template 'ie11' (for example, `--template @rdjennings/ie11`).

# Polyfills included via package.json"browserslist" spec

## react-app-polyfill/ie11

react-app-polyfill/ie11 includes support for:

<ol>
<li>Promise (for async / await support)</li>
<li>window.fetch (a Promise-based way to make web requests in the browser)</li>
<li>Object.assign (a helper required for Object Spread, i.e. { ...a, ...b })</li>
<li>Symbol (a built-in object used by for...of syntax and friends)</li>
<li>Array.from (a built-in static method used by array spread, i.e. [...arr])</li>
</ol>

## react-app-polyfill/stable

react-app-polyfill/stable includes additional functinoality not supported by IE11 and other browsers. By placing IE 11 in the _browserslist_ section of package.json create-react-app will select the appropriate polyfills as needed.

# ponyfill

## cdn.jsdelivr.net/npm/css-vars-ponyfill@2

cdn.jsdelivr.net/npm/css-vars-ponyfill@2 is a _ponyfill_ injected into the index.html in the _public_ folder of the react app to provide CSS support for variables (all defined at the _:root_ level). As a ponyfill it must be "activated" via call to "cssVars({})" using all of the default parameters. To see all of the options for this call visit:  
https://jhildenbiddle.github.io/css-vars-ponyfill/#/

# core.js

A great deal of the IE 11 support is dereived from core.js. For more information on what is supported visit:  
https://github.com/zloirock/core-js/blob/master/README.md

# NOTE:

CSS min, max (and by extension clamp) are still not supported. Other special handling, such as implicit grid placement, must be handled via the appropriate CSS
