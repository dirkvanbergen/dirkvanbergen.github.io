<template>
  <div class="scene">
    <div class="cube" @click="flip" v-bind:class="{'show-front' : !flipped, 'show-back': flipped}">
      <CubeFace v-bind:msg="textFront"></CubeFace>
      <CubeFace v-bind:msg="textBack"></CubeFace>
    </div>
  </div>
</template>

<script>
import CubeFace from './CubeFace.vue'

export default {
  name: 'TextCube',
  components: { CubeFace },
  data: function() {
    return {
      flipped: false,
      textFront: "This is the front",
      textBack: "This is the back "
    };
  },
  props: {
    msg: String
  },
  methods: {
    flip: function() {
      this.flipped = !this.flipped;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
.scene {
  width: 250px;
  height: 250px;
  perspective: 750px;
  .cube {  
      width: 100%;
      height: 100%;
      transform-style: preserve-3d;
      position: relative;
      transform-origin: center center;
      transition: transform 1s;
      

      &.show-front {
        transform: rotateY(   0deg);
      }
      &.show-back {
        transform: rotateY(   -180deg);
      }
  }
}
</style>
