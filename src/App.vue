<template>
  <main id="app">
    <home/>
  </main>
</template>
<script>
import Home from './views/Home.vue'
export default {
  components: {
    Home
  }
}
</script>
<style lang="less">
@import './assets/css/mixins.less';
main {
  margin: 0;
  padding: 0;
  width: 100%;
  border-right: 2px solid blue;
}
</style>
