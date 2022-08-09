<template>
<!-- using conditional rendering v-if -->
<h2 v-if="num===0">The num is zero</h2>  
<h2 v-else-if="num < 0">The num is negative</h2>
<h2 v-else-if="num > 0">The num is positive</h2>
<!-- we need to write v-else statement below v-if otherwise it will not work -->
<!-- all the v-if ,v-else,v-else-if derictives must be written one after other or it will not work  -->
<h2 v-else>It is not a num </h2>

<div v-if="display">
    <h2>Divakar</h2>
</div>

<!-- v-show directive  -->
<h2 v-show=" displayVShow">Using v-show directive </h2>


</template>

<script>
export default{
    name:'conditionalRendering',
    data() {
        return{
            num:'Hello',
            display:true,
            displayVShow:true,
        }
    },
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