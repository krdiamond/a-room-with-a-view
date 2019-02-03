<template>

  <div id="the-view">


    <img id="pool" :src="poolImage" v-if="itsDayTime"/>

    <img id="rain" :src="rainImage" v-if="itsRaining"/>

    <div id="clouds">
         <img id="cloud1" :src="cloudImage" v-on:click="itsRaining = !itsRaining"/>
         <img id="cloud2" :src="cloudImage" v-on:click="itsRaining = !itsRaining"/>
         <img id="cloud3" :src="cloudImage" v-on:click="itsRaining = !itsRaining"/>
    </div>

    {{now}}

  </div>
</template>

<script>
import poolFile from "./images/pool.jpg"
import cloudFile from "./images/cloud.png"
import rainFile from "./images/raining.gif"

setInterval(switchDayOrNight, 500);
function switchDayOrNight() {
  this.itsDayTime = !this.itsDayTime;
}

export default {
  name: 'the-view',
  data(){
    return {
      poolImage: poolFile,
      cloudImage: cloudFile,
      rainImage: rainFile,
      itsRaining: false,
      now: new Date,
      itsDayTime: true,
    }
  },
  created () {
  setInterval(() => this.now = new Date, 500)
}

}
</script>
