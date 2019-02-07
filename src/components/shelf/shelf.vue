<template>

  <div id="shelf-area">


    <img id="shelf" :src="shelfImage"/>

    <!-- <img id="watering-can" :src="wateringCanImage"/> -->

  </div>
</template>

<script>
import shelfFile from "./images/shelf.png"
// import wateringCanFile from "./images/watering-can.png"

export default {
  name: 'shelf',
  data(){
    return {
      shelfImage: shelfFile,
      // wateringCanImage: wateringCanFile,
    }
  }
}
</script>
