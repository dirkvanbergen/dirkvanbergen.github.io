<template>
  <div class="hello">
    <div class="business-card">
      <div class="picture"></div>
      <CardContent />
      <Controls />
    </div>
  </div>
</template>

<script>
import CardContent from './CardContent.vue';
import Controls from './Controls.vue';
export default {
  name: 'HelloWorld',
  components: {
    CardContent, Controls
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
@import '../styles/_globals.scss';

.hello {
  height: 100%;
  display: flex;
  flex-direction: row;
  align-items: center;
  align-content: center;
  justify-content: center;
}

.business-card {
  position: relative;
  width: 1200px;
  height: 600px;
  background-color: $color-gray1;
  box-shadow: 0px 100px 200px 5px $color-gray2;
  border-radius:300px 20px;
  overflow: hidden;
}

.picture {
  filter: grayscale(100%);
  background-image: url('../assets/dirk.jpg');
  background-repeat: no-repeat; 
  background-position: left center;
  background-size: 538px 720px;
  background-position-y: -120px;
  background-position-x: -20px;
  position: absolute;
  left: 0px;
  top: 0px;
  bottom: 0px;
  width: 420px;
}
</style>
