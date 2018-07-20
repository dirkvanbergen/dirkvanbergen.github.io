<template>
  <div class="hello">
    <TextCube></TextCube>
  </div>
</template>

<script>
import TextCube from './TextCube.vue'
export default {
  name: 'HelloWorld',
  components: { TextCube },
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello {
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
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
