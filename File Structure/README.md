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
>>>>This is our Apstarting point. In this file, we specify our root component that is App.vue, then this root element is served in our `public/index.html` file.
>>
>>2. App.vue
>>
>>>>It contains html, css and JS corresponding to UI elements that you are going to show on browser.
>>
>>3. Components
>>
>>>>We divide our UI into smaller components that we put in our components folder like we have `HelloWorld.vue` here.
>>
>>4. Assests
>>
>>>>Here, we put our images or icons or any other files that we are using in our App.
>>