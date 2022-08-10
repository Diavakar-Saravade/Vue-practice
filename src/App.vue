<template>
  <HelloWorld />
  <FirstVue />
  <conditionalRendering/>
  <listRendering/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import conditionalRendering from './components/conditionalRendering.vue'
import listRendering from './components/listRendering.vue'


export default {
  name: 'App',
  components: {
    HelloWorld,
    conditionalRendering,
    listRendering,
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
