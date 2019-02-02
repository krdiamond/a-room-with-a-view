<template>
  <div id="app" >
    <div id="the-vue-container" :style="{ fontSize: postFontSize + 'em' }">

      <Window/>
      <theView v-on:enlarge-text="postFontSize += 0.1"/>


    </div>
  </div>
</template>

<script>
 import Window from './components/window/window.vue'
 import theView from './components/the-view/the-view.vue'


  export default {
    name: 'app',
    components: {   //component must be called here in addition to import
      Window,
      theView,
    },
    data(){
      return {
        postFontSize: 1,
      }
    }
  }
</script>


<style src="./app.scss"></style>
