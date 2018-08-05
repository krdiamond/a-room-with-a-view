<template>
  <div id="app">

    <!--  <Window/> component found in component folder -->
     <Example/>


  </div>
</template>

<script>
 import Window from './components/window.vue' // to import a component it must be imported here
 import Example from './components/example_component.vue'

  export default {
    name: 'app',
    components: {   //component must be called here in addition to import
      Window,
      Example
    }
  }
</script>

<style>

/* global css that is applied to everything does not have scope */
/* scoped is used when it is specific to only that component */

#app {5
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 48px;
}

</style>
