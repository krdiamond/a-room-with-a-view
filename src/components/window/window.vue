<template>
  <div id="windows">

    <div id="window" v-bind:class="{click_through: windowIsOpened}">

        <img id="closed-window"
              v-on:click="windowIsOpened = !windowIsOpened"
              v-bind:class="{ hide: windowIsOpened}"
              img :src="closedWindowImage">

        <img id="open-window"
             v-on:click="windowIsOpened = !windowIsOpened"
             v-bind:class="{ hide: !windowIsOpened}"
             img :src="openWindowImage"/>
    </div>


     <div id="left-open-window" v-on:click="windowIsOpened = !windowIsOpened" ></div>
     <div id="right-open-window" v-on:click="windowIsOpened = !windowIsOpened"></div>


  </div>

</template>


<script>

import closedWindowFile from "./images/window-closed.png"
import openWindowFile from "./images/window-open.png"
import { serverBus } from '/Users/kristina/Programming/a-room-with-a-vue/src/main.js';




export default {
  name: 'window',
  data(){
    return {
      openWindowImage: openWindowFile,
      closedWindowImage: closedWindowFile,
      windowIsOpened: false,
    }
  },
  // created() {
  //   serverBus.$on('closeWindow', (itsRaining) => {
  //     if (itsRaining == true && this.windowIsOpened == true) {
  //       setTimeout(() => this.windowIsOpened = false, 1000);
  //     }
  //   });
  // }
}
</script>



<!-- rainsFor5Seconds() {

 } -->
