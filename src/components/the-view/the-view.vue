<template>
  <div id="the-view">

    <img id="pool" :src="poolImage"/>

    <img id="rain" :src="rainImage" v-if="itsRaining"/>

    <div id="clouds" v-on:click="itsRaining = !itsRaining">
         <img id="cloud1" :src="cloudImage"/>
         <img id="cloud2" :src="cloudImage"/>
         <img id="cloud3" :src="cloudImage"/>
    </div>

      DUMB SENTANCE

    <button v-on:click="$emit('enlarge-text')">
      Enlarge text
    </button>

  </div>
</template>

<script>
import poolFile from "./images/pool.jpg"
import cloudFile from "./images/cloud.png"
import rainFile from "./images/raining.gif"

export default {
  name: 'the-view',
  data(){
    return {
      poolImage: poolFile,
      cloudImage: cloudFile,
      rainImage: rainFile,
      itsRaining: false,
    }
  }
}
</script>
