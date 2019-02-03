<template>
  <div id="the-view">

    <img id="pool" :src="poolImage"/>

    <img id="rain" :src="rainImage" v-if="itsRaining"/>

    <div id="clouds" v-on:click="closeWindow">
         <img id="cloud1" :src="cloudImage" v-on:click="itsRaining = !itsRaining"/>
         <img id="cloud2" :src="cloudImage" v-on:click="itsRaining = !itsRaining"/>
         <img id="cloud3" :src="cloudImage" v-on:click="itsRaining = !itsRaining"/>
    </div>

  </div>
</template>

<script>
import poolFile from "./images/pool.jpg"
import cloudFile from "./images/cloud.png"
import rainFile from "./images/raining.gif"
import { serverBus } from '/Users/kristina/Programming/a-room-with-a-vue/src/main.js';

export default {
  name: 'the-view',
  data(){
    return {
      poolImage: poolFile,
      cloudImage: cloudFile,
      rainImage: rainFile,
      itsRaining: false,
    }
  },
  methods: {
    closeWindow: function () {
      serverBus.$emit('closeWindow', this.itsRaining);
     }
  }
}
</script>
