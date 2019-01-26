<template>
  <div id="pool">
    <img :src="pool"/>
    <!-- <Clouds/> -->
  </div>
</template>

<script>
import pool from "./images/pool.jpg"
import Clouds from "./clouds.vue"

export default {
  name: 'pool',
  components: {
    Clouds,
  },
  data(){
    return {
      pool: pool,
    }
  }
}
</script>
