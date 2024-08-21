<template>
  <div>
  <!-- Binding headings tag id using Bind directive -->
   <h2 v-bind:id="headingId">This is my Heading</h2>

   <!--Binding button poperty disable-->
   <button v-bind:disabled="disable">My Disable Button</button>
   <!--Spacing between buttons-->
   <br>
   <br>
   <!--Using ! will make disable false-->
   <button v-bind:disabled="!disable">My Enable Button</button>
</div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      greet:"Hello",
      name:"<b>Saad</b>",
      threat:`<a href="#" onclick = "alert('You have been hacked!')">Win a Prizes!</a>`,
      headingId:"MyHead",
      disable:true
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
