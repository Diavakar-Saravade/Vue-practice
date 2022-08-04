<template>
  <!-- <HelloWorld msg="Hello World!" />
  <HelloWorld msg="Hello Vue!" /> -->
  <FirstVue />
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import FirstVue from './components/FirstVue.vue'


export default {
  name: 'App',
  components: {
    // HelloWorld,
    FirstVue,
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
