<template>
  <div class="hello">
    <CubeMenu />
    <TextCube />
  </div>
</template>

<script>
import CubeMenu from './CubeMenu.vue'
import TextCube from './TextCube.vue'
export default {
  name: 'HelloWorld',
  components: { TextCube, CubeMenu },
  props: {
    msg: String
  },
  methods: {
    switchTo: function(face) {
      this.$children[1].switchTo(face);
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import 'styles/_globals.scss';

.hello {
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
