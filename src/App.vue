<template>
  <div id="app">

     <Desert/> <!--component found in component folder -->


  </div>
</template>

<script>
 import Desert from './components/Desert.vue' // to import a component it must be imported here

  export default {
    name: 'app',
    components: {   //component must be called here in addition to import
      Desert
    }
  }
</script>

/* <style>

/* global css that is applied to everything does not have scope */
/* scoped is used when it is specific to only that component */

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

</style>
