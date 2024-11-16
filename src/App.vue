<template>
  <HamsterMain />
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import HamsterMain from './components/HamsterMain.vue';

export default defineComponent({
  name: 'App',
  components: {
    HamsterMain
  }
});
</script>

<style lang="scss">
@import url('https://fonts.cdnfonts.com/css/movavi-grotesque');
@import url('https://fonts.googleapis.com/css2?family=Lato:ital,wght@0,100;0,300;0,400;0,700;0,900;1,100;1,300;1,400;1,700;1,900&display=swap');

body {
  margin: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  background: var(--main-background-fill, radial-gradient(50% 50% at 50% 50%, #41AEE7 0%, #054BA6 100%));
  height: 100vh;
  margin: 0;
  padding: 0;
}
</style>
