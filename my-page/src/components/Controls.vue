<template>
  <div class="controls">
    <svg viewBox="0 0 400 400" width="400" height="400">
      <g class="menu-button menu-button__contact">
      <path d="M100,250 v100
               A250 250 0 0 0 177.5, 337.5
               L146.5, 242.5
               A150 150 0 0 1 100,250"
            id="button"/>
      </g>
      <g transform="rotate(-24, 100, 100)" class="menu-button menu-button__about">
        <use xlink:href="#button"/>
      </g>
      <g transform="rotate(-48, 100, 100)" class="menu-button menu-button__skills">
        <use xlink:href="#button" />
      </g>
      <g transform="rotate(-72, 100, 100)" class="menu-button menu-button__family">
        <use xlink:href="#button" />
      </g>
    </svg>
  </div>
</template>

<script>
export default {
  name: 'Controls'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
@import '../styles/_globals.scss';

.controls {
  position: absolute;
  bottom: 0; right: 0;
  height: 400px;
  width: 400px;

  .menu-button {
    stroke: $color-gray4;
    fill: transparent;

    &:hover {
      stroke-width: 2px;
    }
  }
}

</style>
