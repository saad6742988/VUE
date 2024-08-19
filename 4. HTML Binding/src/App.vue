<template>
  <div>
  <!-- try Binding Bold String using mustache syntax -->
   <div>{{ greet }} {{ name }}</div>

   <!-- try Binding Bold String using v-text directive -->
   <div v-text="greet + ' '+ name"></div>

   <!-- So, we need a v-html directive, this will bold our name -->
    <div v-html="greet + ' '+ name"></div>

    <!-- Threat example -->
    <div v-html="threat"></div>
     
</div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      greet:"Hello",
      name:"<b>Saad</b>",
      threat:`<a href="#" onclick = "alert('You have been hacked!')">Win a Prize!</a>`
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
