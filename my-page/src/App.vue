<template>
  <div id="app">
    <div class="header">
      <div class="header__content">
        <div class="title">
          irk van Bergen
        </div>
        <div class="subtitle">
          Software Engineer
        </div>
      </div>
    </div>
    <div class="content">
      <AboutDirk />
      <HappyDirk />
      <WorkDirk />
      <ContactDirk />
    </div>
  </div>
</template>

<script>
import AboutDirk from './components/AboutDirk.vue'
import HappyDirk from './components/HappyDirk.vue'
import WorkDirk from './components/WorkDirk.vue'
import ContactDirk from './components/ContactDirk.vue'

export default {
  name: 'app',
  components: {
    AboutDirk,HappyDirk,WorkDirk,ContactDirk
  }
}
</script>

<style lang="scss">
@import 'styles/_globals.scss';

html, body {
  margin: 0;
  padding: 0;
  width: 100%;
}
* {
  box-sizing: border-box;
}
#app {
  font-family: 'Comfortaa', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: $color-blue5;
  width: 100%;
  background-color: $color-gray0;
}

.header {
  color: $color-pink3;
  font-size: 32px;
  font-weight: 700;
  position: relative;
  width: 100%;
  padding: 50px 0;
  background-color: $color-blue0;

  &__content {    
    width: 500px;
    margin: 0 auto;
  }

  .title {
    position: relative;
    padding-left: 50px;

    &:before {
      content: 'D';
      font-size: 64px;
      position: absolute;
      top: -3px;
      left: 0px;
    }
  }

  .subtitle {
    color: $color-blue3;
    font-size: 20px;
    padding-left: 50px;
    z-index: 1;
  }
}
.content-block {
  padding: 50px 0;

  &__content {
    width: 500px;
    margin: 0 auto;
    &--title {
      font-size: 32px;
      font-weight: 700;
      color: $color-pink0;
      margin-bottom: 40px;
    }
    &--text {
      color: $color-pink0;
      line-height: 2em;
    }
  }
}
</style>
