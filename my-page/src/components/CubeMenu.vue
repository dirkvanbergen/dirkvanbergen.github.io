<template>
  <div class="cube-menu">
    <ul class="cube-menu__list">
      <li @click="switchTo('front')" class="cube-menu__list--front">Front</li>
      <li @click="switchTo('left')" class="cube-menu__list--left">Left</li>
      <li @click="switchTo('back')" class="cube-menu__list--back">Back</li>
      <li @click="switchTo('right')" class="cube-menu__list--right">Right</li>
      <li @click="switchTo('top')" class="cube-menu__list--top">Top</li>
      <li @click="switchTo('bottom')" class="cube-menu__list--bottom">Bottom</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'CubeMenu',
  methods: {
    switchTo: function(face) {
      this.$parent.switchTo(face);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
.cube-menu {

  &__list {
    margin: 0 0 50px 0;
    padding: 0;
    list-style-type: none;
    display: flex;
    flex-direction: row;
    justify-content: center;
    flex-wrap: wrap;
    width: 100%;

    li {
      margin: 0;
      padding: 0;
      line-height: 25px;
      font-size: 16px;
      padding: 10px 20px;
      border: 1px solid black;
      border-radius: 3px;
      margin: 10px;
      cursor: pointer;
      transition: all 0.2s;
      color: white;
      font-weight: bold;
      width: 100px;

      &:hover{
        box-shadow: 0px 10px 50px 0px rgba(0, 0, 0, 0.2);
      }
    }

    &--front  { background: hsla(  0, 100%, 50%, 0.7); }
    &--right  { background: hsla( 60, 100%, 50%, 0.7); }
    &--back   { background: hsla(120, 100%, 50%, 0.7); }
    &--left   { background: hsla(180, 100%, 50%, 0.7); }
    &--top    { background: hsla(240, 100%, 50%, 0.7); }
    &--bottom { background: hsla(300, 100%, 50%, 0.7); }
  }
}
</style>
