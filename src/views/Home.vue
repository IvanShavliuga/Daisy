<template>
<main>
  <Header/>
  <Receive/>
  <Expand/>
  <Process/>
  <Landing/>
  <Advertising/>
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
import Process from '@/components/Process.vue'
import Landing from '@/components/Landing.vue'
import Advertising from '@/components/Advertising.vue'
export default {
  name: 'Home',
  components: {
    Header,
    Receive,
    Expand,
    Process,
    Landing,
    Advertising
  }
}
</script>
