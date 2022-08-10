<!-- List rendering by using arrays and objects  -->
<template>
<!-- name is to refer current item in a loop and names is is our array we bind in mustach syntax 'name' to display -->
 <!-- index is to find the index of names in array -->
 <!--v-for attribute should have :key attribute we can give unique name in these iteration nsme is unique   -->
 <h2 v-for="(name ,index ) in names" :key="name">{{index}} {{name}}</h2>
 
 <!-- because we are using array of objects so we need to access individual property by using name.firstname -->
 <h2 v-for="name in fullNames" :key="name" >{{name.firstname}} {{name.lastname}}</h2>
<!-- div tag is for 'for loop' -->
<div v-for="actor in actors" :key="actor">
<h2>{{actor.name}}</h2>
<h3 v-for="movie in actor.movies" :key="movie">{{movie}}</h3>
</div>
<!-- objects  -->
<h2 v-for="(values ,key ,index)  in info" :key="values">{{key}} {{index}} {{values}}</h2>
<!-- if we need to display names but saperately here <hr/> is for saperator-->
<template v-for="name in names" :key="name">
<h2>{{name}}</h2>
<hr/>    
</template>

</template>

<script>
export default{
    name:'renderingLists',
    data(){
        return{
            names:['Shubi','Dv','Nik'],
            fullNames:[
                {firstname:'Divakar',lastname:'Saravade'},
                {firstname:'Subii',lastname:'Narkhede'},
                {firstname:'Uv',lastname:'Saravade'},
            ],
            //Array of arrays
            actors:[
                {
                    name: 'Tony Stark',
                    movies : ['iron man','Avengers'],
                },
                {
                    name:'Johnny Deep',
                    movies : ['pirates'],
                }
            ],

            info:{
                name:'Divakar',
                desig:'SDE',
                Company:'Encora',
            }
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