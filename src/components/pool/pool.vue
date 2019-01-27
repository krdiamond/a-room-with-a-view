<template>
  <div id="pool">

    <img :src="poolImage"/>

  </div>
</template>

<script>
import poolFile from "./images/pool.jpg"

export default {
  name: 'pool',
  data(){
    return {
      poolImage: poolFile
    }
  }
}
</script>
