<template>
  <div id="window">

    <img id="closed-window"
          v-on:click="windowIsOpened = !windowIsOpened"
          v-bind:class="{ hide: windowIsOpened}"
          img :src="closedWindowImage">


    <img id="open-window"
         v-on:click="windowIsOpened = !windowIsOpened"
         v-bind:class="{ hide: !windowIsOpened, click_through: windowIsOpened,}"
         img :src="openWindowImage"/>



  </div>
</template>


<script>

import closedWindowFile from "./images/window-closed.png"
import openWindowFile from "./images/window-open.png"

export default {
  name: 'window',
  data(){
    return {
      openWindowImage: openWindowFile,
      closedWindowImage: closedWindowFile,
      windowIsOpened: false,
    }
  },
  computed: {
    classObject: function () {
      return {
        active: this.isActive && !this.error,
        'text-danger': this.error && this.error.type === 'fatal'
      }
    }
  }
}
</script>
