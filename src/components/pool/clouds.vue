<template>
  <div id="clouds">
    <img :src="cloud" v-on:click="handleCloudClick" id="cloud1" class="cloud" alt="cloud"/>
    <img :src="cloud" v-on:click="handleCloudClick" id="cloud2" class="cloud" alt="cloud"/>
    <img :src="cloud" v-on:click="handleCloudClick" id="cloud3" class="cloud" alt="cloud"/>
  </div>
</template>

<script>
import cloud from "./images/cloud.png"

export default {
  name: 'clouds',
  data(){
    return {
      cloud: cloud,
      raining: false,
    }
  },
  methods: {
    handleCloudClick() {
      raining: !this.raining
      console.log(this.raining)
    }
  }
}
</script>
