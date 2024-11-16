<template>
  <div class="main">
    <HamsterHeader />
    <HamsterReferals />
    <img src="../assets/Footer.png" alt="Footer" class="main__footer"/>
  </div>
</template>

<script setup lang="ts">
import HamsterHeader from './HamsterHeader.vue';
import HamsterReferals from './HamsterReferals.vue';

</script>

<style lang="scss">
.main {
  margin: 0;
  padding: 0;
  height: 100vh;
  overflow: hidden;
  position: relative;

  &__footer {
    position: fixed;
    bottom: -1px;
    width: 100vw;
  }
}
</style>
