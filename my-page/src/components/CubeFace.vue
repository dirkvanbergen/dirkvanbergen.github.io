<template>
    <div class="cube_face">
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
.cube_face {
    position: absolute;
    width: 250px;
    height: 250px;
    border: 1px solid black;
    text-align: left;
    background-color: white;

    p {
        margin: 0;
        padding: 10px;
        font-size: 24px;
    }
    &:first-child {
        transform:rotateY(0deg);
    }
    &:last-child {
        transform:rotateY(180deg);
    }
}
</style>
