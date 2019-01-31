<template>
  <div id="the-view">

    <img :src="poolImage"/>

    <div id="clouds"
         v-on:click="itsRaining = !itsRaining"
         v-bind:class="{ hide: itsRaining}">
         <img :src="cloudImage" id="cloud1"/>
         <img :src="cloudImage" id="cloud2"/>
         <img :src="cloudImage" id="cloud3"/>
    </div>

  </div>
</template>

<script>
import poolFile from "./images/pool.jpg"
import cloudFile from "./images/cloud.png"

export default {
  name: 'the-view',
  data(){
    return {
      poolImage: poolFile,
      cloudImage: cloudFile,
      itsRaining: false,
    }
  }
}
</script>
