<template>
  <div id="app">
    <div id="the-vue-container">
      <Window/> <!-- component found in component folder -->
      <Pool/>
    </div>
  </div>
</template>

<script>
 import Window from './components/window.vue'
 import Pool from './components/pool/pool.vue'


  export default {
    name: 'app',
    components: {   //component must be called here in addition to import
      Window,
      Pool,
    },
    methods: {

    }
  }
</script>


<style src="./app.scss"></style>
