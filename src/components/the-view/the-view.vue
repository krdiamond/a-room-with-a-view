<template>

  <div id="the-view">


    <img id="pool" :src="poolImage" v-if="itsDayTime"/>

    <img id="rain" :src="rainImage" v-if="itsRaining"/>

    <div id="clouds">
         <img id="cloud1" :src="cloudImage" v-on:click="itsRaining = !itsRaining"/>
         <img id="cloud2" :src="cloudImage" v-on:click="itsRaining = !itsRaining"/>
         <img id="cloud3" :src="cloudImage" v-on:click="itsRaining = !itsRaining"/>
    </div>

    {{counter}}

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
      counter: 1,
      itsDayTime: true,
    }
  },
  created () {
    setInterval(() => this.counter += 1, 1000);
  }
}
</script>
