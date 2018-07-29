<template>
  <div class="scene">
    <div class="cube" v-bind:class="currentClass">
      <CubeFace msg="1" class="cube__face--front"></CubeFace>
      <CubeFace msg="2" class="cube__face--right"></CubeFace>
      <CubeFace msg="3" class="cube__face--top"></CubeFace>
      <CubeFace msg="4" class="cube__face--bottom"></CubeFace>
      <CubeFace msg="5" class="cube__face--left"></CubeFace>
      <CubeFace msg="6" class="cube__face--back"></CubeFace>
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
      currentClass: 'cube--show-front'
    };
  },
  props: {
    msg: String
  },
  methods: {
    switchTo: function(face) {
      this.currentClass = 'cube--show-' + face;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
@import 'styles/_globals.scss';

.scene {
  width: $cube-size;
  height: $cube-size;
  perspective: calc(#{$cube-size} * 2.5);
  .cube {  
      width: 100%;
      height: 100%;
      transform-style: preserve-3d;
      position: relative;
      transform-origin: center center;
      transition: transform 1s;

      &--show-front  { transform: translateZ(calc(#{$cube-size} * -0.5)) rotateY(   0deg); }
      &--show-right  { transform: translateZ(calc(#{$cube-size} * -0.5)) rotateY( -90deg); }
      &--show-back   { transform: translateZ(calc(#{$cube-size} * -0.5)) rotateY(-180deg); }
      &--show-left   { transform: translateZ(calc(#{$cube-size} * -0.5)) rotateY(  90deg); }
      &--show-top    { transform: translateZ(calc(#{$cube-size} * -0.5)) rotateX( -90deg); }
      &--show-bottom { transform: translateZ(calc(#{$cube-size} * -0.5)) rotateX(  90deg); }
  }
}
</style>
