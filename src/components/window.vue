<template>
  <div id="window">
    <img :src="windowImageFileToUseAsBackground"/>
  </div>
</template>

<script>

import windowImageFile from "../../src/assets/window.png"

export default {
  name: 'window',
  data(){
    return {
      windowImageFileToUseAsBackground: windowImageFile,
    }
  }
}
</script>
