# Binding HTML
Sometimes we are using form to get data from user that contains a rich text feild where user can make text bold or italic. To render that rich text, we need to render it using `v-html` directive.

`<div v-html="greet + ' '+ name"></div>`

In above code, name is a rich text with bold tag, see App.vue file for more details.

## Warning
While using v-html, we must only render **trusted data**, someone can easily enter some hacking script which will be render on our App and disturbing our users. Example,

`<a href="#" onclick = "alert('You have been hacked!')">Win a Prize!</a>`

Rendering above string sing v-html will generate a clickable text that shows alert boc saying *'You have been hacked!'*.
