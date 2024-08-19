<template>
  <div>
  <!-- A Static hard coded View -->
 <div>Hello Saad!</div> 

 <!-- Binding Text from script block -->
  <div>Hello {{name}}!</div>

   <!-- Binding Multiple Text from script block -->
   <div>{{greet}} {{name}}!</div>

   <!-- Binding Text from script block using Directives -->
  <div v-text="name">Hello</div>
</div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      greet:"Hello",
      name:"Saad"
    }
  }
  
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
