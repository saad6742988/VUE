# Project Structure
## Files
* ### package.json
>>It contains Dependencies and scripts needed to run the App.
* ### package-lock.json
>>Ensures consistent isntallation of dependencies, containing the versions info of the dependencies.
* ### babel.config.js
>>Babel is a tool that transforms modren JS to older syntax that is more cross-browser compatible.
## Folders
* ### Node Modules
>>This is sutomatically geneterated when you run `npm install` after cloning project or when creating new project using `vue create`.
* ### Public
>>* Contains static files that is used when we host our App live.
>>* Inside `public`, there is a `index.html` file that is actually served on browser but we don't make any changes to this file because we are modifying this static page using vue.
* ### src
>> This is our most important folder. We are mostly working in this. It further contains following:
>>
>>1. main.js
>>
>>>>This is our App starting point. In this file, we specify our root component that is App.vue, then this root element is served in our `public/index.html` file.
>>
>>2. App.vue
>>
>>>>It contains html, css and JS corresponding to UI elements that you are going to show on browser.
>>
>>3. Components
>>
>>>>We divide our UI into smaller components(.vue files) that we put in our components folder like we have `HelloWorld.vue` here.
>>
>>4. Assests
>>
>>>>Here, we put our images or icons or any other files that we are using in our App.
>>
## Single File Component(.Vue file)
A .vue file is a custom file format that uses HTML-like syntax to describe a portion of the UI.

Each .vue file contains following top-level blocks:

1. `<template></template>` 
1. `<script></script>` 
1. `<style></style>` 

>The **Template** block is like HTML for UI.

>The **Script** block contains logic and functionality of your App for specified portion of UI. i.e. JavaScript

>The **Style** block specify the style of your HTML in Template. i.e. CSS

So, instead of dividing your App into three seprate codebases for UI(HTML Files), Style(CSS Files) and Logic(JS files), in Vue, your app is divided into components that are responsible for their on UI,Style and Logic.

## More about Vue
While working in Vue, we will be wiring up the logic(Script Block) to the UI(Template Block), i.e. connecting data from script block to the style block. Just, let Vue know how you want to bind you data and it will take care of rest.

