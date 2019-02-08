<template>

  <div id="shelf-area">


    <img id="shelf" :src="shelfImage" class="draggable"/>

    <!-- <img id="watering-can" :src="wateringCanImage"/> -->

  </div>
</template>


<script>
import shelfFile from "./images/shelf.png"
// import VueInteract from '../../drag-n-drop.js';
import interact from 'interact.js';
// import wateringCanFile from "./images/watering-can.png"

export default {
  name: 'shelf',
  data(){
    return {
      shelfImage: shelfFile,
      // wateringCanImage: wateringCanFile,
    }
  },
  mounted() {
    interact('.draggable')
    .draggable({
      onmove: this.dragMoveListener
    });
  },
  methods: {
    dragMoveListener (event) {
    var target = event.target,
        x = (parseFloat(target.getAttribute('data-x')) || 0) + event.dx,
        y = (parseFloat(target.getAttribute('data-y')) || 0) + event.dy;

    // translate the element
    target.style.webkitTransform =
    target.style.transform =
      'translate(' + x + 'px, ' + y + 'px)';

    // update the posiion attributes
    target.setAttribute('data-x', x);
    target.setAttribute('data-y', y);
  }


}
}
</script>
