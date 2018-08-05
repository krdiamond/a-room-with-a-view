<template>
  <div id="window">

    <img :src="windowImageFileToUseAsBackground"/>

  </div>
</template>

<script>

import windowImageFile from "/Users/user/kristina-coding/a-room-with-a-vue/src/assets/window.png"

export default {
  name: 'window',
  data(){
    return {
      windowImageFileToUseAsBackground: windowImageFile,
    }
  }
}
</script>


<style src="./window.css">

</style>
