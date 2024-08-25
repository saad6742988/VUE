<template>
  <div>
    <!--Assigning Static Classes-->
    <h2 class="underlineText">This is static class Assigned</h2>

    <!--Assigning Class by directive-->
    <h2 v-bind:class="headingClass">This is Dynamic class Assigned</h2>

    <!--Assigning Dynamic and Static classes together-->
    <h2 class="underlineText" v-bind:class="headingClass">This is Dynamic and Static class both Assigned</h2>

    <!--Let's have a scenario of promoted and
     not promoted products. We want promoted products to get underlined-->
     <ul>
      <li v-bind:class="!isPromoted && 'underlineText'">Not Promoted 1</li>
      <li v-bind:class="isPromoted && 'underlineText'">Promoted</li>
     </ul>
     <br>
     <br>
     <!--Let's have a scenario of soldout and
     available products. We want soldout products in red and available in green.
     Here comes the concept of conditional binding using ternity operators.-->
     <ul>
      <li v-bind:class="isSoldout ? 'soldout' : 'available'">Soldout Movie</li>
      <li v-bind:class="!isSoldout ? 'soldout' : 'available'">Available Movie</li>
     </ul>
     <br>
     <br>

     <!---Applying multiple dynamic classes Using Arrays-->
     <ul>
     <li v-bind:class="['underlineText' , 'available']">Available & Promoted Movie</li>
     <!--Using Conditions-->
     <li v-bind:class="[!isPromoted && 'underlineText' , !isSoldout ? 'soldout' : 'available']">Available But Not Promoted Movie</li>
     <li v-bind:class="[isPromoted && 'underlineText' , isSoldout ? 'soldout' : 'available']">Not Available But Promoted Movie</li>
    </ul>

    <br>
    <br>
    <!---Applying multiple dynamic classes Using Objects-->
    <ul>
     
     <li v-bind:class="{
      //in object format a class us applied if its corresponding variable is true.
      'underlineText':!isPromoted,
      'available':isAvailable,
      'soldout':!isSoldout,
      
     }">Available But Not Promoted Movie</li>

     <li v-bind:class="{
      'underlineText':isPromoted,
      'available':!isAvailable,
      'soldout':isSoldout,
     }">Not Available But Promoted Movie</li>
    </ul>
  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      // our class variable
      headingClass:"myclass",
      isPromoted:true,
      isSoldout:true,
      isAvailable:true
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
.underlineText{
  text-decoration: underline;
}
.soldout{
  color: red;
}
.available{
  color: green;
}
</style>
