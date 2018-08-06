<template>
  <div id="pool" class="the_view">
    <img :src="pool"/>
    <Clouds/>
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
