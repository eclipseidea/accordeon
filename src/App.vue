<template>
  <div id="app">
    <AccordionView/>
  </div>
</template>

<script>

  import AccordionView from "./components/AccordionView";

  export default {
    name: 'App',
    components: {
      AccordionView
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
  }
</style>

