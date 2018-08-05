<template>
  <div id="desert">

    <h1>{{desertWelcome}}</h1> <!-- mustache is interpolating from data in the script below-->
    <button v-on:click="hideDesert" v-bind:disabled="btnState"> Hide Desert</button> <!--call a piece of data, if true disabled, if false clickable -->
    {{ displayDesert ? 'display desert' : 'do not display desert' }}

    <div class="holder">
      <ul>
        <li v-for ="(eachDesertInArray,index) in desertsAllOverTheWorld">{{ index }}. {{eachDesertInArray.desert}} </li>
        <!-- index gives access to actual index number. Index not necessary. -->
        <!--desertsAllOverTheWorld is an array found in the data object below -->
        <!-- eachDesertInArray is a variable given to each desert object.
            Once you have this variable you can call each by their key 'desert' -->
      </ul>

      <p v-if="desertsAllOverTheWorld.length >= 5"> You know a lot of different deserts!</p>
      <p v-else> You don't know that many deserts. Pretty sad :( </p>
      <!-- if statement using v-directives. -->
      
    </div>

    <img :src="DesertImageFileToUseAsBackground"/> <!-- no mustache with attribute (source is an attribute) use quotes-->

  </div>
</template>

<script>

import DesertImageFile from "/Users/user/kristina-coding/a-room-with-a-vue/src/assets/desert_background.jpg"

export default {
  name: 'Desert',
  data(){
    return {
      desertWelcome : "I'M THE DESERT I AM SO DRY :(", //text to interpolate in the template
      DesertImageFileToUseAsBackground: DesertImageFile,
      displayDesert: false,
      btnState: true,
      desertsAllOverTheWorld: [
        {desert: 'Death Valley'},
        {desert: 'Saudi Arabia'},
        {desert: 'Arizona'}
      ]
    }
  }
}
</script>


<style>

</style>
