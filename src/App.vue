<template>
  <div id="app">
    <div id="the-vue-container">
      <Window/>
      <Pool/>
    </div>
  </div>
</template>

<script>
 import Window from './components/window/window.vue'
 import Pool from './components/pool/pool.vue'


  export default {
    name: 'app',
    components: {   //component must be called here in addition to import
      Window,
      Pool,
    }
  }
</script>


<style src="./app.scss"></style>
