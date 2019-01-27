<template>
  <div id="window">

      <img :src="closedWindowImage"
            v-on:click="windowIsOpened = !windowIsOpened"
            v-bind:class="{ hide: windowIsOpened}"/>

      <img :src="openWindowImage"
            v-on:click="windowIsOpened = !windowIsOpened"
            v-bind:class="{ hide: !windowIsOpened}"/>
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
  }
}
</script>
