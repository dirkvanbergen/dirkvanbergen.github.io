<template>
    <div class="cube__face">
        <p>{{msg}}</p>
    </div>
</template>

<script>
export default {
  name: 'CubeFace',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">

.cube__face {
    position: absolute;
    width: 100%;
    height: 100%;
    border: 2px solid black;
    border-radius: 6px;
    line-height: $cube-size;
    font-size: 80px;
    font-weight: bold;
    color: white;
    text-align: center;

    p {
        margin: 0;
        padding: 10px;
    }

    &--front {
        transform:rotateY(0deg) translateZ(calc(#{$cube-size} / 2));
        
    }
    &--back {
        transform:rotateY(180deg) translateZ(calc(#{$cube-size} / 2));
    }
    &--top {
        transform:rotateX(90deg) translateZ(calc(#{$cube-size} / 2));
    }
    &--bottom { 
        transform:rotateX(-90deg) translateZ(calc(#{$cube-size} / 2));
    }
    &--left { 
        transform:rotateY(-90deg) translateZ(calc(#{$cube-size} / 2));
    }
    &--right {
        transform:rotateY(90deg) translateZ(calc(#{$cube-size} / 2));
    }
}

.cube__face--front  { background: hsla(  0, 100%, 50%, 0.7); }
.cube__face--right  { background: hsla( 60, 100%, 50%, 0.7); }
.cube__face--back   { background: hsla(120, 100%, 50%, 0.7); }
.cube__face--left   { background: hsla(180, 100%, 50%, 0.7); }
.cube__face--top    { background: hsla(240, 100%, 50%, 0.7); }
.cube__face--bottom { background: hsla(300, 100%, 50%, 0.7); }
</style>
