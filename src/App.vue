<template>
  <div id="app">

    <select v-model="selectedLocation" >
      <option v-for="(option,index) in options" :key="index" v-bind:value="option.value">
        {{ option.text }}
      </option>
    </select>

    <div class="container">
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
    data(){
      return {
        selectedLocation: 'CHOOSE A LOCATION',
        options: [
          { text: 'pool', value: 'pool' },
          { text: 'car', value: 'car' },
        ]
      }
    },
    methods: {

    }
  }
</script>

<style src="./app.css">


</style>
