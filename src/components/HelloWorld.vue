<template>
    <!-- data binding by using mustache syntax -->
    <h1>{{localVariable}} {{name}} {{surname}}</h1>
    <!-- attribute binding using v-text text derictive   -->
   <div v-text="course"></div>
    <!-- attribute binding using v-html html derictive   -->
   <div v-html="courseName"></div>
   <!-- binding attribute by using v-bind:id attribute -->
   <h2 v-bind:id="headingID">MIT WPU</h2>
   <!-- binding attribute by using v-bind:disabled(property) -->
   <button v-bind:disabled="isDisabled">BIND</button>
   <!-- css underline class -->
   <h2 class="underline">Encora Digital</h2>
   <!-- class binding and adding css class underline dynamically -->
   <h2  class="underline" v-bind:class="status">Sucessfull</h2>
   <h2 v-bind:class="isPromoted && 'promoted'">Good Vibes</h2>
</template>

<script>
export default {
  name: 'HelloWorld',
    data() {
    return {
      localVariable: 'Hi',
      name: 'Divakar',
      surname: 'Saravade',
      course: 'BCA',
      courseName:'<b>MCA<b>',
      headingID:'idOfHeading',
      isDisabled:true,
      status:'Success',
      isPromoted: true,
    }
  },

}
</script>

<style>
.underline{
  text-decoration: underline;
}

.promoted{
  font-style: italic;
}
</style>

