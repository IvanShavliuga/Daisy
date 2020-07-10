<template>
<main>
  <Header/>
  <Receive/>
  <Expand/>
</main>
</template>
<style>
main {
  margin: 0;
  padding: 0;
}
</style>
<script>
// @ is an alias to /src
import Header from '@/components/Header.vue'
import Receive from '@/components/Receive.vue'
import Expand from '@/components/Expand.vue'
export default {
  name: 'Home',
  components: {
    Header,
    Receive,
    Expand
  }
}
</script>
